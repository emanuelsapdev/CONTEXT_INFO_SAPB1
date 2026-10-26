# GPA3 - Gross Profit Adjustment - JE Details

- **Tabla:** GPA3
- **Descripción:** Gross Profit Adjustment - JE Details
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GPA3.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | [OGPA](OGPA.md) |  |  |
| 2 | `PostDate` | Posting Date | Date | 8 | - |  |  |
| 3 | `DocDate` | Document Date | Date | 8 | - |  |  |
| 4 | `DueDate` | Due Date | Date | 8 | - |  |  |
| 5 | `Series` | Series | Int | 11 | - | 0 |  |
| 6 | `JERemarks` | Journal Remarks | nVarChar | 254 | - |  |  |
| 7 | `TransCode` | Transaction Code | nVarChar | 4 | - |  |  |
| 8 | `Ref1` | Reference 1 | nVarChar | 200 | - |  |  |
| 9 | `Ref2` | Reference 2 | nVarChar | 200 | - |  |  |
| 10 | `JERef` | Journal Entry Reference | nVarChar | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
