# OCRW - BP for IIS Annual

- **Tabla:** OCRW
- **Descripción:** BP for IIS Annual
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCRW.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `CardCode` | BP Code | nVarChar | 15 | - |  |  |
| 3 | `Year` | Report Year | Int | 6 | - |  |  |
| 4 | `SentMeth` | Method of Sending | VarChar | 1 | - |  | `D` = Doc. Date<br>`T` = Tax Date |
| 5 | `SentValue` | Sent Value | Num | 19.6 | - |  |  |
| 6 | `LastAMeth` | Last Accepted Method | VarChar | 1 | - |  | `D` = Doc. Date<br>`T` = Tax Date |
| 7 | `LastAValue` | Last Accepted Value | Num | 19.6 | - |  |  |
| 8 | `ReportID` | Report ID | nVarChar | 50 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| BP_YEAR | Yes | CardCode, Year |
