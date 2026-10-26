# UDG4 - User Defaults - Default POI for Folio Numbering Documents

- **Tabla:** UDG4
- **Descripción:** User Defaults - Default POI for Folio Numbering Documents
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UDG4.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | POI Code | nVarChar | 8 | - |  |  |
| 2 | `FNDAbs` | Folio Numbering Document Abs Entry | Int | 11 | [OFND](OFND.md) |  |  |
| 3 | `ObjectCode` | Document | nVarChar | 20 | - |  |  |
| 4 | `DocSubtype` | Subdocument | nVarChar | 2 | - | -- | `--`<br>`DM` = A/P Debit Memo<br>`DN` = A/R Debit Memo<br>`IB` = A/R Bill |
| 5 | `DflPTICode` | Default POI Code | nVarChar | 5 | [OPTI](OPTI.md) |  |  |
| 6 | `DflPtiFCE` | Default POI Code for FCE | nVarChar | 5 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, FNDAbs |
