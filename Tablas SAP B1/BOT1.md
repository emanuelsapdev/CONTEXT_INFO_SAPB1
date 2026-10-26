# BOT1 - Bill of Exchange Transactions

- **Tabla:** BOT1
- **Descripción:** Bill of Exchange Transactions
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/BOT1.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Transaction No. | Int | 11 | [OBOT](OBOT.md) |  |  |
| 2 | `BOENumber` | Bill of Exchange No. | Int | 11 | - |  |  |
| 3 | `BoeType` | Bill of Exchange Type | VarChar | 1 | - | I | `I` = Incoming<br>`O` = Outgoing |
| 4 | `DueDate` | Bill of Exchange Due Date | Date | 8 | - |  |  |
| 5 | `BPBankCtr` | BP Bank Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 6 | `BPBankCod` | BP Bank Code | nVarChar | 30 | - |  |  |
| 7 | `BPBankAct` | BP Bank Account | nVarChar | 50 | - |  |  |
| 8 | `BPBankBrnc` | BP Bank Branch | nVarChar | 50 | - |  |  |
| 9 | `ExReconNum` | Extra Reconciliation Number | Int | 11 | - |  |  |
| 10 | `BOEAbs` | Bill of Exchange Key | Int | 11 | [OBOE](OBOE.md) |  |  |
| 11 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 12 | `EnBPBnkAct` | Encryption of BP Bank Account | Text | 16 | - |  |  |
| 13 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 14 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, BOENumber, BoeType |
