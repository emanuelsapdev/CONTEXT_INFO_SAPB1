# OROC - Retorno Operation Codes

- **Tabla:** OROC
- **Descripción:** Retorno Operation Codes
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OROC.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `OccurCode` | Occurrence Code | Int | 11 | - |  |  |
| 3 | `MovemnCode` | Movement Code | Int | 6 | - |  |  |
| 4 | `BoeStatus` | BoE Status | VarChar | 1 | - |  | `G` = Generated<br>`S` = Sent<br>`D` = Deposited<br>`P` = Paid<br>`C` = Canceled<br>`L` = Closed<br>`F` = Failed<br>`V` = BoE to Vendor |
| 5 | `Descript` | Description | nVarChar | 254 | - |  |  |
| 6 | `Color` | Color | Int | 11 | - |  |  |
| 7 | `FileFormat` | File Format | nVarChar | 100 | - |  |  |
| 8 | `BankCode` | Bank Code | nVarChar | 30 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
