# OWTX - WTax Transactions

- **Tabla:** OWTX
- **Descripción:** WTax Transactions
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWTX.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `SrcObjType` | Source Object Type | nVarChar | 20 | - | -1 | `-1`<br>`13` = A/R Invoice<br>`14` = A/R Credit Memo<br>`18` = A/P Invoice<br>`19` = A/P Credit Memo<br>`46` = Outgoing Payment<br>`24` = Incoming Payment |
| 3 | `SrcObjAbs` | Source Object Internal ID | Int | 11 | - | -1 |  |
| 4 | `Cancelled` | Canceled | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 5 | `FullCopied` | Fully Copied | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| SECONDARY | Yes | SrcObjType, SrcObjAbs |
