# TPS2 - Tax Parameter - Return Values

- **Tabla:** TPS2
- **Descripción:** Tax Parameter - Return Values
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TPS2.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TpsId` | Tax Parameter Set | Int | 11 | [OTPS](OTPS.md) |  |  |
| 2 | `DispOrder` | Display Order | Int | 11 | - |  |  |
| 3 | `TprId` | ID of Return Values Mapping | Int | 11 | [OTPR](OTPR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TpsId, TprId |
| ORDER | Yes | TpsId, DispOrder |
