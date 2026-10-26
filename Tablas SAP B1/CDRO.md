# CDRO - Drag & Relate - Output Fields

- **Tabla:** CDRO
- **Descripción:** Drag & Relate - Output Fields
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CDRO.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ObjectId` | Object ID | nVarChar | 4 | - |  |  |
| 2 | `FieldId` | Field ID | Int | 6 | - |  |  |
| 3 | `DescStr` | Description | nVarChar | 30 | - |  |  |
| 4 | `VisOrder` | Visual Order | Int | 6 | - | 0 |  |
| 5 | `UserSign` | User Form | Int | 6 | [OUSR](OUSR.md) | -1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ObjectId, FieldId, UserSign |
