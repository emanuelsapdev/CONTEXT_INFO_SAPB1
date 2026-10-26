# GPA7 - Product Cost Adjustment - Journal Entry Details

- **Tabla:** GPA7
- **Descripción:** Product Cost Adjustment - Journal Entry Details
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GPA7.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | [OGPA](OGPA.md) |  |  |
| 2 | `PostDate` | Posting Date | Date | 8 | - |  |  |
| 3 | `DocDate` | Document Date | Date | 8 | - |  |  |
| 4 | `Series` | Series | Int | 11 | - | 0 |  |
| 5 | `Ref2` | Reference 2 | nVarChar | 100 | - |  |  |
| 6 | `JERemarks` | Journal Remarks | nVarChar | 254 | - |  |  |
| 7 | `MRVRef` | MRV Entry Reference | nVarChar | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
