# SEULA - SEULA

- **Tabla:** SEULA
- **Descripción:** SEULA
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SEULA.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Locale` | Localization | nVarChar | 100 | - |  |  |
| 2 | `EULAType` | EULA type | VarChar | 1 | - | P | `P` = Productive<br>`E` = Evaluation |
| 3 | `EULADoc` | EULA doc | Text | 16 | - |  |  |
| 4 | `Format` | format | nVarChar | 50 | - | TXT | `TXT` = Text Format<br>`PDF` = PDF Format |
| 5 | `CheckSum` | checksum | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Locale, EULAType |
