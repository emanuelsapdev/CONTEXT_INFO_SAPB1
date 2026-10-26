# APM3 - Project Management - Stages - Attachments - History

- **Tabla:** APM3
- **Descripción:** Project Management - Stages - Attachments - History
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/APM3.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | [PMG1](PMG1.md) |  |  |
| 2 | `LineID` | Row No. | Int | 11 | - |  |  |
| 3 | `StageID` | Stage ID | Int | 11 | [PMG1](PMG1.md) |  |  |
| 4 | `PATH` | Document Path | Text | 16 | - |  |  |
| 5 | `FILE` | File Name | nVarChar | 100 | - |  |  |
| 6 | `DATE` | Date | Date | 8 | - |  |  |
| 7 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineID, LogInstanc |
