# OTOB - 1099 Opening Balance

- **Tabla:** OTOB
- **Descripción:** 1099 Opening Balance
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OTOB.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `VendCode` | Vendor Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 2 | `Form1099` | 1099 Form | Int | 11 | [OTNN](OTNN.md) |  |  |
| 3 | `Box1099` | 1099 Box | nVarChar | 20 | - |  |  |
| 4 | `PostDate` | Posting Date | Date | 8 | - |  |  |
| 5 | `AmountLC` | Amount (LC) | Num | 19.6 | - |  |  |
| 6 | `Submitted` | Submitted | VarChar | 1 | - | N | `Y` = Yes<br>`N` = New |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | VendCode, Form1099, Box1099 |
