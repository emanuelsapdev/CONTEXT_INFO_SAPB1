# OTAX - VAT Transactions

- **Tabla:** OTAX
- **Descripción:** VAT Transactions
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OTAX.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `SrcObjType` | Source Object Type | nVarChar | 20 | - | -1 | `-1`<br>`13` = A/R Invoice<br>`14` = A/R Credit Memo<br>`165` = Correction A/R Invoice<br>`166` = Correction A/R Invoice Reversals<br>`18` = A/P Invoice<br>`19` = A/P Credit Memo<br>`163` = Correction A/P Invoice<br>`164` = Correction A/P Invoice Reversals<br>`46` = Outgoing Payment<br>`24` = Incoming Payment<br>`57` = Check for Payment<br>`30` = Journal Transaction<br>`67` = Warehouse Transfer<br>`25` = Deposit<br>`321` = Internal Reconciliation<br>`76` = Deposit Temporary<br>`140000010` = Incoming Excise Invoice<br>`140000009` = Outgoing Excise Invoice<br>`69` = Import file |
| 3 | `SrcObjAbs` | Source Object Internal ID | Int | 11 | - | -1 |  |
| 4 | `OrdinLNum` | Ordial Num (BTF & Canceled) | Int | 11 | - | -1 |  |
| 5 | `Cancelled` | Canceled | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| SECONDARY | Yes | SrcObjType, SrcObjAbs, OrdinLNum |
