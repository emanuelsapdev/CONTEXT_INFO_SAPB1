# BOX1 - Box Definition - Rows

- **Tabla:** BOX1
- **Descripción:** Box Definition - Rows
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/BOX1.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `BoxCode` | Group Code | nVarChar | 30 | - |  |  |
| 2 | `BoxMember` | Box Code | nVarChar | 30 | [OBOX](OBOX.md) |  |  |
| 3 | `VATMember` | VAT Group | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 4 | `SeqNum` | Sequence Number | Int | 11 | - |  |  |
| 5 | `FormulSign` | Formula Sign | VarChar | 1 | - | P | `P` = +<br>`M` = - |
| 6 | `ReportType` | Report Type | VarChar | 1 | - | B | `B` = Box Declaration<br>`S` = BAS Reporting |
| 7 | `EffecDate` | Effective From | Date | 8 | - |  |  |
| 8 | `TaxType` | Acquisition / Reverse Tax Type | VarChar | 1 | - | B | `I` = Input Tax<br>`O` = Output Tax<br>`B` = Input Tax and Output Tax |
| 9 | `BosCode` | Box Set Code | Int | 11 | [OBOS](OBOS.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | BoxCode, ReportType, BosCode, SeqNum |
