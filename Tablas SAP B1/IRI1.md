# IRI1 - ISD Recipient Invoice Lines

- **Tabla:** IRI1
- **Descripción:** ISD Recipient Invoice Lines
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/IRI1.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [OIRI](OIRI.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `StaType` | GST Tax Type | Int | 11 | - |  | `-100` = CGST<br>`-110` = SGST<br>`-120` = IGST<br>`-130` = Cess GST<br>`-150` = UTGST |
| 4 | `TaxAcct` | Tax Account | nVarChar | 15 | - |  |  |
| 5 | `RecAmnt` | Received Amount | Num | 19.6 | - |  |  |
| 6 | `ElgAmnt` | Eligible Amount | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
