# OSVT - Define Summary VAT Report Type

- **Tabla:** OSVT
- **Descripción:** Define Summary VAT Report Type
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSVT.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | VAT Report Type ID | Int | 11 | - |  |  |
| 2 | `Name` | Summary VAT Report Type | nVarChar | 254 | - |  |  |
| 3 | `Descript` | Description | nVarChar | 254 | - |  |  |
| 4 | `NameDesc` | Name & Desc | nVarChar | 254 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| NAME | Yes | Name |
