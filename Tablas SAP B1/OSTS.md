# OSTS - Service App Technician settings

- **Tabla:** OSTS
- **Descripción:** Service App Technician settings
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSTS.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | Int | 11 | - |  |  |
| 2 | `Technician` | Technician | Int | 11 | [OHEM](OHEM.md) |  |  |
| 3 | `Choice` | Choice | VarChar | 1 | - | C | `G` = Group<br>`C` = Customize |
| 4 | `GroupCode` | Group Code | Int | 11 | [OSSG](OSSG.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
