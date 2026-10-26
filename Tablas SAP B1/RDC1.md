# RDC1 - Multilingual Report

- **Tabla:** RDC1
- **Descripción:** Multilingual Report
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RDC1.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocCode` | Doc. Code | nVarChar | 8 | [RDOC](RDOC.md) |  |  |
| 2 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 3 | `DocName` | Doc. Name | nVarChar | 64 | - |  |  |
| 4 | `LangCode` | Language Code | Int | 11 | - |  |  |
| 5 | `Template` | Report Template Data | Text | 16 | - |  |  |
| 6 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 7 | `CreateTime` | Create Time | Int | 11 | - |  |  |
| 8 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 9 | `UpdateTime` | Update Time | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocCode, LineNum |
| UniqueIdx | Yes | DocCode, LangCode |
