# AIS2 - Input Service Distribution - Row Detail

- **Tabla:** AIS2
- **Descripción:** Input Service Distribution - Row Detail
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AIS2.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [OISD](OISD.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `TargetLoc` | Target Location Code | Int | 11 | - |  |  |
| 4 | `TarLocName` | Target Location Name | nVarChar | 100 | - |  |  |
| 5 | `TarStaType` | Target GST Tax Type | Int | 11 | - |  | `-100` = CGST<br>`-110` = SGST<br>`-120` = IGST<br>`-130` = Cess GST<br>`-150` = UTGST |
| 6 | `TarTaxAcct` | Target Tax Account Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 7 | `AllocAmnt` | Allocated Amount | Num | 19.6 | - |  |  |
| 8 | `ITCType` | ITC Type | VarChar | 1 | - | E | `E` = Eligible<br>`I` = Ineligible |
| 9 | `SubLineNum` | Sub Row Number | Int | 11 | - | -1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum, TargetLoc, TarTaxAcct, TarStaType, SubLineNum |
