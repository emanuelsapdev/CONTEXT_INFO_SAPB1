# OASC - Account Segmentation Categories

- **Tabla:** OASC
- **Descripción:** Account Segmentation Categories
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OASC.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SegmentId` | Segment ID | Int | 6 | [OASG](OASG.md) |  |  |
| 2 | `Code` | Code | nVarChar | 20 | - |  |  |
| 3 | `Name` | Name | nVarChar | 100 | - |  |  |
| 4 | `ShortName` | Short Name | nVarChar | 10 | - |  |  |
| 5 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SegmentId, Code |
