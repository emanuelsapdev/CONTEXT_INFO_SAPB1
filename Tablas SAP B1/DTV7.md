# DTV7 - Datev Run Attachments

- **Tabla:** DTV7
- **Descripción:** Datev Run Attachments
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DTV7.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RunId` | Run Number | Int | 11 | [ODTV](ODTV.md) |  |  |
| 2 | `LineId` | Row Number | Int | 11 | - |  |  |
| 3 | `Comment` | Remark | Text | 16 | - |  |  |
| 4 | `Created` | Created On | Date | 8 | - |  |  |
| 5 | `CreatedBy` | Created By | nVarChar | 25 | - |  |  |
| 6 | `FileName` | File name | nVarChar | 254 | - |  |  |
| 7 | `Path` | File Path | nVarChar | 254 | - |  |  |
| 8 | `Size` | File Size | Int | 11 | - |  |  |
| 9 | `Title` | Title | nVarChar | 100 | - |  |  |
| 10 | `Type` | File Type | nVarChar | 100 | - |  |  |
| 11 | `Client` | Client Creation | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RunId, LineId |
