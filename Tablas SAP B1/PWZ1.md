# PWZ1 - Payment Wizard - Rows 1

- **Tabla:** PWZ1
- **Descripción:** Payment Wizard - Rows 1
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PWZ1.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IdEntry` | ID Entry | Int | 11 | [OPWZ](OPWZ.md) |  |  |
| 2 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 3 | `CardName` | BP Name | nVarChar | 200 | - |  |  |
| 4 | `CardType` | BP Type | VarChar | 1 | - |  |  |
| 5 | `Checked` | Checked | VarChar | 1 | - |  |  |
| 6 | `BPCurrency` | BP Currency | nVarChar | 3 | - |  |  |
| 7 | `BPSingleP` | BP Single Payment | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 8 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | IdEntry, CardCode |
