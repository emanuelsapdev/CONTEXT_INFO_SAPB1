# OFUS - Microsoft 365 Integration User Settings

- **Tabla:** OFUS
- **Descripción:** Microsoft 365 Integration User Settings
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OFUS.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ID` | ID | nVarChar | 254 | - |  |  |
| 2 | `USER_ID` | User Id | nVarChar | 254 | - |  |  |
| 3 | `FOLDERNAME` | Office Folder Name Map | Text | 16 | - |  |  |
| 4 | `LOCALE` | Locale | nVarChar | 254 | - |  |  |
| 5 | `PROFPHOTO` | Profile Photo | Text | 16 | - |  |  |
| 6 | `EM_USER_ID` | Sending email using the MS365 account which bind to this user Id | Int | 6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ID |
