# OKPF - KPI Factor

- **Tabla:** OKPF
- **Descripción:** KPI Factor
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OKPF.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `FactorId` | KPI Factor No. | nVarChar | 3 | - |  |  |
| 2 | `FactorName` | KPI Factor Name | nVarChar | 100 | - |  |  |
| 3 | `CatId` | Numerator | Int | 6 | - |  |  |
| 4 | `TemplateId` | Template | Int | 11 | - |  |  |
| 5 | `IsSys` | Is System | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | FactorId |
