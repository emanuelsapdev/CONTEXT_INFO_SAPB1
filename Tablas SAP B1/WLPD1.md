# WLPD1 - Fiori Launchpad Groups

- **Tabla:** WLPD1
- **Descripción:** Fiori Launchpad Groups
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WLPD1.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ParentId` | Parent Id | nVarChar | 40 | - |  |  |
| 2 | `Guid` | Guid | nVarChar | 40 | - |  |  |
| 3 | `Order` | Order | Int | 11 | - |  |  |
| 4 | `GroupId` | Group Id | nVarChar | 40 | - |  |  |
| 5 | `GroupName` | Group Name | nVarChar | 100 | - |  |  |
| 6 | `Visible` | Visible | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ParentId, Guid |
