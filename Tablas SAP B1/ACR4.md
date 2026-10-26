# ACR4 - Allowed WTax Codes for BP - History

- **Tabla:** ACR4
- **Descripción:** Allowed WTax Codes for BP - History
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ACR4.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CardCode` | BP Code | nVarChar | 15 | - |  |  |
| 2 | `WTCode` | WTax Code | nVarChar | 4 | - |  |  |
| 3 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CardCode, WTCode, LogInstanc |
