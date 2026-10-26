# OEI18 - Outgoing Excise Invoice - Export Process

- **Tabla:** OEI18
- **Descripción:** Outgoing Excise Invoice - Export Process
- **Cantidad de campos:** 18
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OEI18.html

## Campos (18)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [OOEI](OOEI.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 4 | `ObjectType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 140000009 |  |
| 5 | `ExpDocType` | Type of Exportation Document | Int | 11 | [OBNI](OBNI.md) | -1 |  |
| 6 | `ExpDeclNum` | Exportation Declaration Number | Int | 11 | - |  |  |
| 7 | `ExpDeclDat` | Exportation Declaration Date | Date | 8 | - |  |  |
| 8 | `ExpNature` | Nature of Exportation | Int | 11 | [OBNI](OBNI.md) | -1 |  |
| 9 | `ExpRegNum` | Number of Exportation Registry | Int | 11 | - |  |  |
| 10 | `ExpRegDate` | Date of Exportation Registry | Date | 8 | - |  |  |
| 11 | `LadBillNum` | Bill of Lading Number | nVarChar | 19 | - |  |  |
| 12 | `LadBillDat` | Date of Bill of Lading | Date | 8 | - |  |  |
| 13 | `MerchLeftD` | Date Merchandise Left Customs | Date | 8 | - |  |  |
| 14 | `LadBillTyp` | Type of Bill of Lading | Int | 11 | [OBNI](OBNI.md) | -1 |  |
| 15 | `DrawSReg` | Drawback - Suspension Regime | nVarChar | 11 | - |  |  |
| 16 | `NatureExp` | Nature of Export | nVarChar | 44 | - |  |  |
| 17 | `QultExpItm` | Quantity of Exported Items | Num | 19.6 | - |  |  |
| 18 | `nSeqAdic` | Additional Item Sequential Number | Int | 6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
