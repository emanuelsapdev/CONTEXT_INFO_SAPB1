# OSRC - Service App Report Configuration

- **Tabla:** OSRC
- **Descripción:** Service App Report Configuration
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSRC.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | Int | 11 | - |  |  |
| 2 | `SysRptName` | System Report Name | nVarChar | 120 | - |  |  |
| 3 | `SysRptTemp` | System Report Template | Text | 16 | - |  |  |
| 4 | `CusRptName` | Customized Report Name | nVarChar | 120 | - |  |  |
| 5 | `CusRptTemp` | Customized Report Template | Text | 16 | - |  |  |
| 6 | `RptChoice` | Report Choice | VarChar | 1 | - |  | `S` = System<br>`C` = Customized |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
