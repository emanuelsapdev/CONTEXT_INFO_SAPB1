# MAP2 - Mapping Input and Output Relation

- **Tabla:** MAP2
- **Descripción:** Mapping Input and Output Relation
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MAP2.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `MapID` | Mapping ID | Int | 11 | [OMAP](OMAP.md) |  |  |
| 2 | `CodeIn` | Input Code | Int | 11 | - |  |  |
| 3 | `CodeOut` | Output Code | Int | 11 | - |  |  |
| 4 | `Sequence` | Run Sequence | Int | 11 | - |  |  |
| 5 | `Name` | Parameter Name | nVarChar | 20 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | MapID, CodeIn, CodeOut |
