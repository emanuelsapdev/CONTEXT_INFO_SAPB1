# PRQ18 - Purchase Request - Export Process

- **Tabla:** PRQ18
- **Descripción:** Purchase Request - Export Process
- **Cantidad de campos:** 18
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PRQ18.html

## Campos (18)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [OPRQ](OPRQ.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 4 | `ObjectType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 1470000113 |  |
| 5 | `ExpDocType` | Exportation Document Type | Int | 11 | [OBNI](OBNI.md) | -1 |  |
| 6 | `ExpDeclNum` | Exportation Declaration Number | Int | 11 | - |  |  |
| 7 | `ExpDeclDat` | Exportation Declaration Date | Date | 8 | - |  |  |
| 8 | `ExpNature` | Exportation Nature | Int | 11 | [OBNI](OBNI.md) | -1 |  |
| 9 | `ExpRegNum` | Exportation Registry Number | Int | 11 | - |  |  |
| 10 | `ExpRegDate` | Exportation Registry Date | Date | 8 | - |  |  |
| 11 | `LadBillNum` | Bill of Lading Number | nVarChar | 19 | - |  |  |
| 12 | `LadBillDat` | Bill of Lading Date | Date | 8 | - |  |  |
| 13 | `MerchLeftD` | Date Merchandise Left Customs | Date | 8 | - |  |  |
| 14 | `LadBillTyp` | Bill of Lading Type | Int | 11 | [OBNI](OBNI.md) | -1 |  |
| 15 | `DrawSReg` | Drawback - Suspension Regime | nVarChar | 11 | - |  |  |
| 16 | `NatureExp` | Nature of Export | nVarChar | 44 | - |  |  |
| 17 | `QultExpItm` | Quantity of Exported Items | Num | 19.6 | - |  |  |
| 18 | `nSeqAdic` | Additional Item Sequential Number | Int | 6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
