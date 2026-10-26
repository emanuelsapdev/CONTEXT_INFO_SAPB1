# OAGP - Agent Name

- **Tabla:** OAGP
- **Descripción:** Agent Name
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OAGP.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AgentCode` | Agents | nVarChar | 32 | - |  |  |
| 2 | `AgentName` | Agent Name | nVarChar | 50 | - |  |  |
| 3 | `Memo` | Description | nVarChar | 50 | - |  |  |
| 4 | `Locked` | Locked | VarChar | 1 | - |  |  |
| 5 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AgentCode |
| AGENT_NAME | Yes | AgentName |
