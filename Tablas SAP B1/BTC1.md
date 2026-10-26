# BTC1 - Internal Bank Operation Codes - Accounts

- **Tabla:** BTC1
- **Descripción:** Internal Bank Operation Codes - Accounts
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/BTC1.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `LineId` | Row | Int | 6 | - |  |  |
| 3 | `GLAct` | G/L Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 4 | `Project` | Project | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 5 | `PrftCenter` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 6 | `VatCode` | VAT Code | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 7 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 8 | `PrftCent2` | Distribution Rule2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 9 | `PrftCent3` | Distribution Rule3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 10 | `PrftCent4` | Distribution Rule4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 11 | `PrftCent5` | Distribution Rule5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineId |
