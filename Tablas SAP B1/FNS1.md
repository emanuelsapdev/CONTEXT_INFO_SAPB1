# FNS1 - Folio Numbering - Voided Series

- **Tabla:** FNS1
- **Descripción:** Folio Numbering - Voided Series
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/FNS1.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Series` | Series ID | Int | 11 | [OFNS](OFNS.md) |  |  |
| 2 | `FolNumFrom` | Folio Number From | Int | 11 | - |  |  |
| 3 | `FolNumTo` | Folio Number To | Int | 11 | - |  |  |
| 4 | `Reason` | Reason For Number Skipping | nVarChar | 100 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Series, FolNumFrom |
| To | Yes | Series, FolNumTo |
