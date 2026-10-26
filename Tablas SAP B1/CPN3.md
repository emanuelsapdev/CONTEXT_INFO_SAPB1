# CPN3 - Campaign - Partners

- **Tabla:** CPN3
- **Descripción:** Campaign - Partners
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CPN3.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CpnNo` | Campaign No. | Int | 11 | [OCPN](OCPN.md) |  |  |
| 2 | `CpnLineNum` | Campaign Line Number | Int | 11 | - |  |  |
| 3 | `ParterId` | Partners | Int | 11 | [OPRT](OPRT.md) |  |  |
| 4 | `OrlCode` | Relationship Code | Int | 11 | [OORL](OORL.md) |  |  |
| 5 | `RelatCard` | Related BP | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 6 | `Memo` | Details | nVarChar | 50 | - |  |  |
| 7 | `LogIns` | Log Instance - History | Int | 11 | - |  |  |
| 8 | `VisOrder` | Visual Order | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CpnNo, CpnLineNum |
