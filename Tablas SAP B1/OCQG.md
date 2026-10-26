# OCQG - Card Properties

- **Tabla:** OCQG
- **Descripción:** Card Properties
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCQG.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `GroupCode` | Property Group Code | Int | 6 | - |  |  |
| 2 | `GroupName` | Property Name | nVarChar | 50 | - |  |  |
| 3 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 4 | `Filler` | Filler | nVarChar | 10 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | GroupCode |
| GROUP_NAME | Yes | GroupName |
