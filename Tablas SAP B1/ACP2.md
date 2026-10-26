# ACP2 - Campaign - Items

- **Tabla:** ACP2
- **Descripción:** Campaign - Items
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ACP2.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CpnNo` | Campaign No. | Int | 11 | [OCPN](OCPN.md) |  |  |
| 2 | `CpnLineNum` | Campaign Line Number | Int | 11 | - |  |  |
| 3 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 4 | `ItemName` | Item Description | nVarChar | 200 | - |  |  |
| 5 | `ItemType` | Item Type | VarChar | 1 | - |  | `I` = Items<br>`L` = Labor<br>`T` = Travel |
| 6 | `ItemGrp` | Item Group | nVarChar | 100 | - |  |  |
| 7 | `LogIns` | Log Instance - History | Int | 11 | - |  |  |
| 8 | `VisOrder` | Visual Order | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CpnNo, CpnLineNum, LogIns |
