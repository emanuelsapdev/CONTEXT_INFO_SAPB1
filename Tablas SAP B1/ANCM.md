# ANCM - NCM Code

- **Tabla:** ANCM
- **Descripción:** NCM Code
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ANCM.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | ID | Int | 11 | - |  |  |
| 2 | `NcmCode` | NCM Code | nVarChar | 15 | - |  |  |
| 3 | `Descrip` | Description | nVarChar | 254 | - |  |  |
| 4 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 5 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 7 | `GroupCode` | Group Code | VarChar | 1 | - | 0 |  |
| 8 | `Group` | NCM Group | Int | 6 | [ONCG](ONCG.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LogInstanc |
| CODE | Yes | NcmCode, GroupCode, LogInstanc |
