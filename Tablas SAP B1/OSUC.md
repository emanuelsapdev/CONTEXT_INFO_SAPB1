# OSUC - Single User Setup

- **Tabla:** OSUC
- **Descripción:** Single User Setup
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSUC.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `StpCode` | Setup Code | Int | 6 | - |  |  |
| 2 | `StpDes` | Setup Description | nVarChar | 100 | - |  |  |
| 3 | `Action` | Action | VarChar | 1 | - | B | `B` = Block Update<br>`W` = Warning |
| 4 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 5 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 6 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 7 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 8 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | StpCode |
