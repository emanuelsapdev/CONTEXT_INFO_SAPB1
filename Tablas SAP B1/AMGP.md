# AMGP - Material Group

- **Tabla:** AMGP
- **Descripción:** Material Group
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AMGP.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | ID | Int | 11 | - |  |  |
| 2 | `MatGrp` | Material Group | nVarChar | 3 | - |  |  |
| 3 | `Descrip` | Description | nVarChar | 70 | - |  |  |
| 4 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |
| 5 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `UpdateDate` | Update Date | Date | 8 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LogInstanc |
| CODE | Yes | MatGrp, LogInstanc |
