# UDV1 - Fields where user-defined values can be automatically refreshed

- **Tabla:** UDV1
- **Descripción:** Fields where user-defined values can be automatically refreshed
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UDV1.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IndexID` | Index | Int | 11 | [CUDV](CUDV.md) |  |  |
| 2 | `FieldID` | Field | nVarChar | 60 | - |  |  |
| 3 | `CreateTS` | Create Time | Int | 11 | - |  |  |
| 4 | `UpdateTS` | Update Time | Int | 11 | - |  |  |
| 5 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 8 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | IndexID, FieldID |
