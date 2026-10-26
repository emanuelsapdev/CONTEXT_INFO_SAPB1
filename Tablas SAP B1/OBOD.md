# OBOD - BIOD Master Data

- **Tabla:** OBOD
- **Descripción:** BIOD Master Data
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBOD.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `BIOD_ENTRY` | BIOD Key | Int | 11 | - |  |  |
| 2 | `BIOD_UID` | User ID | Int | 6 | - |  |  |
| 3 | `BIOD_QID` | Query Internal Key | Int | 11 | - |  |  |
| 4 | `BIOD_QN` | Query Name | nVarChar | 100 | - |  |  |
| 5 | `BIOD_QLD` | Last Upload Date | Date | 8 | - |  |  |
| 6 | `BIOD_QLT` | Last Upload Time | Int | 6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | BIOD_ENTRY |
| USERID | No | BIOD_UID |
