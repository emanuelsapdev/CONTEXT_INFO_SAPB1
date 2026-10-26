# EBUSR - EBUSR

- **Tabla:** EBUSR
- **Descripción:** EBUSR
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/EBUSR.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `B1Company` | B1 Company DB name | nVarChar | 200 | - |  |  |
| 2 | `B1User` | B1 user name (from OUSR) | nVarChar | 30 | - |  |  |
| 3 | `Pwd` | encrypted password | Text | 16 | - |  |  |
| 4 | `Pwd2` | encrypted password (backup) | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | B1Company |
