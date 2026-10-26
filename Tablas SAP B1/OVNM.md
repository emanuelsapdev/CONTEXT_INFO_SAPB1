# OVNM - VAT Report Numbering

- **Tabla:** OVNM
- **Descripción:** VAT Report Numbering
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OVNM.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `NumId` | Numbering ID | Int | 11 | - |  |  |
| 2 | `NumName` | Numbering Name | nVarChar | 10 | - |  |  |
| 3 | `First` | First Number | nVarChar | 9 | - |  |  |
| 4 | `Next` | Next Number | nVarChar | 9 | - |  |  |
| 5 | `Last` | Last Number | nVarChar | 9 | - |  |  |
| 6 | `YrDepend` | Year-Dependent | VarChar | 1 | - | N | `Y` = Year-Dependent<br>`N` = Year-Indepedent |
| 7 | `DefaultNum` | Default Numbering | VarChar | 1 | - | N | `Y` = Default Numbering<br>`N` = No Default Numbering |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | NumId |
