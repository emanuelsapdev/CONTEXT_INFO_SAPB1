# OTGG - Target Group

- **Tabla:** OTGG
- **Descripción:** Target Group
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OTGG.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TargetCode` | Target Group Code | nVarChar | 20 | - |  |  |
| 2 | `TargetName` | Target Group Name | nVarChar | 100 | - |  |  |
| 3 | `TargetType` | Target Group Type | VarChar | 1 | - | C | `C` = Customer<br>`S` = Vendor |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TargetCode |
