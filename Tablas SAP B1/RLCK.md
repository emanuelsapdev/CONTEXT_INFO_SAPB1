# RLCK - resource locks table

- **Tabla:** RLCK
- **Descripción:** resource locks table
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RLCK.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `resType` | Resource Type | Int | 11 | - | 1 | `1` = form resource<br>`3` = Grid resource<br>`5` = String list resource<br>`18` = Report |
| 2 | `masterKey` | Master Key | nVarChar | 64 | - |  |  |
| 3 | `wrkstation` | Work Station | nVarChar | 250 | - |  |  |
| 4 | `userSign` | User Sign | Int | 11 | - |  |  |
| 5 | `date` | Date | Date | 8 | - |  |  |
| 6 | `time` | Time | Int | 11 | - |  |  |
| 7 | `count` | Locks Count | Int | 11 | - | 1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | resType, masterKey |
