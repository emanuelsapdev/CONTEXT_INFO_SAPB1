# 3.16–3.18 Attachments, Stream Entity Upload, Item and Employee Images

> Source: *Working with SAP Business One Service Layer* v1.29, sections 3.16–3.18 (paraphrased technical reference).
>
> **Resumen (ES):** configurar la carpeta de anexos (Windows y Linux/CIFS), subir anexos (ruta local o multipart), descargarlos, actualizarlos, subir streams con `Slug`, y manejar imágenes de artículos y empleados.

## 3.16 Attachments (`Attachments2`)

Supported since 9.1 PL12 (HANA). Allowed file types: **pdf, doc, docx, jpg, jpeg, png, txt, xls, ppt**. Max upload size **50 MB** (larger → `413 Request Entity Too Large`). Attachments and attachment lines **can't be deleted** (business rule).

### 3.16.1 Attachment folder setup

The attachment folder is normally a Windows shared folder configured in **Administration > System Initialization > General Settings** (path tab).

| SL platform | Requirement | Requisito (ES) |
|---|---|---|
| Windows | SL runs as **Network Service** by default → grant that account read/write on the share, otherwise SL may not even see the folder | Permisos para Network Service |
| Linux (HANA) | Direct access to the Windows share isn't possible → mount it with **CIFS** | Montar la carpeta con CIFS |

Linux steps:

1. Create the Windows share with read/write (e.g. `\\windows_server\SharedFolder\Attachment`) and set it as attachment folder in General Settings.
2. Create the mount point: `sudo mkdir -p /mnt/attachment`
3. Mount (note forward slashes in the share path; SL on Linux runs as user/group **`b1service0`**):

   ```bash
   mount -t cifs -o username=<windows_user>,password=<windows_password>,sec=ntlmssp,file_mode=0644,dir_mode=0755,uid=b1service0,gid=b1service0 '//windows_server/SharedFolder/Attachment' /mnt/attachment
   ```

   - Domain users: add `domain=<windows_domain>`.
   - Escape special characters in user/password (e.g. `Initial\$1234`).
   - Choose the security mode per corporate policy (kernels < 3.8 default `sec=ntlm`; ≥ 3.8 default `sec=ntlmssp`; see `man mount.cifs`).
4. `sudo chown -R b1service0:b1service0 /mnt/attachment`
5. `sudo find /mnt/attachment -type d -exec chmod 0755 {} \;` and `sudo find /mnt/attachment -type f -exec chmod 0644 {} \;`

Remove EXIF metadata from images before uploading (privacy).

**Auto-mount at boot** (`/etc/fstab`):

1. As root create `/etc/samba/credentials` with `username=`, `password=`, `domain=` and `chmod 600` it.
2. Append to `/etc/fstab`:
   `//windows_server/SharedFolder/Attachment /mnt/attachment cifs credentials=/etc/samba/credentials,file_mode=0644,dir_mode=0755,uid=b1service0,gid=b1service0,sec=ntlmssp 0 0`
3. `sudo mount -a`, then reboot to verify.

### 3.16.2 Uploading

| Case | How | Caso (ES) |
|---|---|---|
| Source file on the **same machine** as SL (HANA and SQL) | JSON with source path | Archivo en la misma máquina que el SL |
| Source file on **another machine** (typical web scenario) | `multipart/form-data` POST | Archivo en otra máquina |

Local source:

```http
POST /b1s/v1/Attachments2
{ "Attachments2_Lines": [ { "SourcePath": "/home/builder/src_attachment", "FileName": "my_attach_1", "FileExtension": "dat" } ] }
```

→ `201 Created` with `AbsoluteEntry` and the lines (`AttachmentDate`, `UserID`, `Override: tNO`). The file is copied into the attachment folder (visible on both the Linux mount and the Windows share).

Remote source (two files in one attachment):

```http
POST /b1s/v1/Attachments2
Content-Type: multipart/form-data; boundary=WebKitFormBoundaryUmZoXOtOBNCTLyxT

--WebKitFormBoundaryUmZoXOtOBNCTLyxT
Content-Disposition: form-data; name="files"; filename="line1.txt"
Content-Type: text/plain

<text content>
--WebKitFormBoundaryUmZoXOtOBNCTLyxT
Content-Disposition: form-data; name="files"; filename="line2.jpg"
Content-Type: image/jpeg

<binary data>
--WebKitFormBoundaryUmZoXOtOBNCTLyxT--
```

- Each boundary in the body starts with `--`; the last one also ends with `--`.
- The form field name is **`files`**.
- On Linux, a "creating file error" means the temp folder permissions changed; fix with `sudo chown -R b1service0:b1service0 /tmp/sap_b1_b1service0` and `sudo chmod -R 755 /tmp/sap_b1_b1service0`.

### 3.16.3 Downloading

| Request | Result | Petición (ES) |
|---|---|---|
| `GET /b1s/v1/Attachments2(3)/$value` | First line's file | Primer archivo |
| `GET /b1s/v1/Attachments2(3)/$value?filename='line2.png'` | A specific line (full name with extension) | Archivo específico |

### 3.16.4 Updating

`PATCH /b1s/v1/Attachments2(3)` with a `multipart/form-data` body:

- If a file with the same name already exists in a line → that line is **replaced**.
- Otherwise → a **new line is appended**.

Both return `204 No Content`.

## 3.17 Stream entity upload with `Slug` (FP 2202+)

Media entities (`HasStream="true"`) — **`Attachments2`** and **`Pictures`** — accept a raw binary POST where the HTTP **`Slug`** header carries the file name.

```http
POST https://slhost:50000/b1s/v2/Attachments2
Slug: SAP.jpg
OData-Version: 4.0
Content-Type: image/jpeg
Cookie: B1SESSION=...

<binary image content>
```

- **.NET OData Client:** `slContext.AddToAttachments2(attachment); slContext.SetSaveStream(attachment, fileStream, true, "image/jpeg", "SAP.jpg"); slContext.SaveChanges();` then read the new `AbsoluteEntry` from the entity descriptor's `EditLink` (`/b1s/v2/attachments2(<entry>)`).
- **SAPUI5:** `sap.ui.unified.FileUploader` with `uploadUrl="/b1s/v2/Attachments2"`, `setSendXHR(true)`, `setUseMultipart(false)` and a header parameter `Slug` with the file name.

## 3.18 Item images and employee images

| Entity | Since | Key | Notes | Entidad (ES) |
|---|---|---|---|---|
| `ItemImages` (`ItemImage`, `HasStream`) | 9.1 PL12 (HANA) | `ItemCode` | Property `Picture` = file name | Imágenes de artículos |
| `EmployeeImages` | 9.3 PL12 (HANA) | Employee ID | | Imágenes de empleados |

Image folder setup: same as attachments (Windows share configured as the *pictures* folder in General Settings, network path; on Linux mount with CIFS, e.g. `'//windows_server/SharedFolder/Images' /mnt/images`).

| Operation | Request | Notes | Operación (ES) |
|---|---|---|---|
| Get item image | `GET /b1s/v1/ItemImages('i001')/$value` | Without `$value` you get JSON with `odata.mediaReadLink`, `odata.mediaContentType`, `ItemCode`, `Picture` | Obtener imagen |
| Get employee image | `GET /b1s/v1/EmployeeImages('<EmployeeID>')` | | Imagen de empleado |
| Upload / replace | `PATCH /b1s/v1/ItemImages('i001')` with `multipart/form-data`, field `files`, e.g. `filename="sap_2.jpg"` | Item must exist; replaces existing image → `204` | Subir/reemplazar |
| Delete | `DELETE /b1s/v1/ItemImages('i001')` → `204` | | Borrar |
| Create with POST | Not allowed → use PATCH | | No se permite POST |
| Query images | Not allowed → query `Items` with `$select=ItemCode,Picture` | | No se permite consultar |
