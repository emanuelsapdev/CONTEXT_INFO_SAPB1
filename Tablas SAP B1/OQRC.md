# OQRC - QR Code

- **Tabla:** OQRC
- **Descripción:** QR Code
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OQRC.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `FileContnt` | QR Code Image Content | Text | 16 | - |  |  |
| 3 | `SrcObjType` | Source Object Type | Int | 11 | - |  |  |
| 4 | `SrcObjAbs` | Source Object Internal ID | nVarChar | 20 | - |  |  |
| 5 | `FieldName` | Field Name | nVarChar | 50 | - |  |  |
| 6 | `ExpAfter` | Expire after defined days | Int | 6 | - |  |  |
| 7 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 8 | `CreateTS` | Creation Time - Incl. Secs | Int | 11 | - |  |  |
| 9 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 10 | `UpdateTS` | Update Time - Incl. Secs | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| SECONDARY | Yes | SrcObjType, SrcObjAbs, FieldName |
