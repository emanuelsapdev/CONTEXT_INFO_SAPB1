# HTM1 - Team Members

- **Tabla:** HTM1
- **Descripción:** Team Members
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/HTM1.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `teamID` | Team ID | Int | 11 | [OHTM](OHTM.md) |  |  |
| 2 | `line` | Row | Int | 6 | - |  |  |
| 3 | `empID` | Employee ID | Int | 11 | [OHEM](OHEM.md) |  |  |
| 4 | `role` | Role in Team | VarChar | 1 | - | M | `L` = Leader<br>`M` = Member |
| 5 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | teamID, empID |
