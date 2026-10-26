# OKRT - Tax Report Type

- **Tabla:** OKRT
- **Descripción:** Tax Report Type
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OKRT.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Tax Report Type ID | Int | 11 | - |  |  |
| 2 | `TaxRepType` | Tax Report Type Name | nVarChar | 254 | - |  |  |
| 3 | `Descrip` | Tax Report Type Description | nVarChar | 254 | - |  |  |
| 4 | `SumRepType` | Summary VAT Report Type | Int | 11 | [OSVT](OSVT.md) |  |  |
| 5 | `NameDesc` | Tax Report Type Name + Desc | nVarChar | 254 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| TAX_REP_TY | Yes | TaxRepType |
