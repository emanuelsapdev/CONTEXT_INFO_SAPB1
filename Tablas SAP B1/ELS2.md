# ELS2 - Vat Report Declaration Output

- **Tabla:** ELS2
- **Descripción:** Vat Report Declaration Output
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ELS2.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RunId` | Run Number | Int | 11 | - |  |  |
| 2 | `Code` | Code | nVarChar | 8 | - |  |  |
| 3 | `Name` | Name | nVarChar | 50 | - |  |  |
| 4 | `BaseAmnt` | Base Amount | Num | 19.6 | - |  |  |
| 5 | `VatAmnt` | Tax Amount | Num | 19.6 | - |  |  |
| 6 | `VatPercent` | VAT Percent | Num | 19.6 | - |  |  |
| 7 | `Category` | Category | VarChar | 1 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RunId, Code, Category |
