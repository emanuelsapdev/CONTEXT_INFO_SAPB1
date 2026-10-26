# OQFD - Query Fields

- **Tabla:** OQFD
- **Descripción:** Query Fields
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OQFD.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IntrnalKey` | Internal Key | Int | 11 | - |  |  |
| 2 | `QryCode` | Query Code | nVarChar | 254 | - |  |  |
| 3 | `CategoryID` | Category ID | Int | 11 | - |  |  |
| 4 | `BaseCode` | Base Code | nVarChar | 254 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | IntrnalKey |
| ALIAS | Yes | QryCode, CategoryID |
