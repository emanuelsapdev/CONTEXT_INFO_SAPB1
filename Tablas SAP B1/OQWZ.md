# OQWZ - Query Wizard

- **Tabla:** OQWZ
- **Descripción:** Query Wizard
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OQWZ.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Query Code | nVarChar | 8 | - |  |  |
| 2 | `Name` | Query Name | nVarChar | 50 | - |  |  |
| 3 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
| NAME | Yes | Name |
