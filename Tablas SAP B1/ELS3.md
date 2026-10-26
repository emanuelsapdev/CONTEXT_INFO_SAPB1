# ELS3 - VAT Declaration Boxes

- **Tabla:** ELS3
- **Descripción:** VAT Declaration Boxes
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ELS3.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RunId` | Run Number | Int | 11 | - |  |  |
| 2 | `BoxCode` | Code | nVarChar | 30 | - |  |  |
| 3 | `BoxMember` | Box Code | nVarChar | 30 | - |  |  |
| 4 | `VATMember` | VAT Group | nVarChar | 8 | - |  |  |
| 5 | `SeqNum` | Sequence Number | Int | 11 | - |  |  |
| 6 | `FormulSign` | Formula Sign | VarChar | 1 | - |  |  |
| 7 | `BoxType` | Type | VarChar | 1 | - |  |  |
| 8 | `SummayFld` | Summary Field | VarChar | 1 | - |  |  |
| 9 | `SortOrder` | Sort Order | Int | 11 | - |  |  |
| 10 | `EffecDate` | Effective From | Date | 8 | - |  |  |
| 11 | `BosCode` | Box Set Code | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RunId, BoxCode, SeqNum, BosCode |
