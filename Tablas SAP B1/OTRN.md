# OTRN - Multilingual Service Table

- **Tabla:** OTRN
- **Descripción:** Multilingual Service Table
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OTRN.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Doc. Entry | Int | 11 | - |  |  |
| 2 | `Category` | Category | nVarChar | 6 | - |  | `CRRpt` = CR Report<br>`Menu` = Menu Item<br>`EFM` = EFM Item |
| 3 | `PriCode` | Primary Code | nVarChar | 128 | - |  |  |
| 4 | `SecCode` | Secondary Code | nVarChar | 128 | - |  |  |
| 5 | `SourceLang` | Source Language | Int | 11 | - |  |  |
| 6 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 7 | `UpdateDate` | Update Date | Date | 8 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| CATCODE | Yes | Category, PriCode, SecCode |
