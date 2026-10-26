# OPRA - Payroll G/L accounts Setup

- **Tabla:** OPRA
- **Descripción:** Payroll G/L accounts Setup
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPRA.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `CateType` | Category Type | VarChar | 1 | - |  | `P` = Perception<br>`D` = Deduction<br>`N` = Payroll Payable<br>`R` = Rounding<br>`O` = Other Payments |
| 3 | `CateCode` | Category Code | nVarChar | 8 | - |  |  |
| 4 | `Category` | Category of Payroll | nVarChar | 254 | - |  |  |
| 5 | `Account` | G/L Account | nVarChar | 15 | [OACT](OACT.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| CATE_CODE | Yes | CateType, CateCode |
