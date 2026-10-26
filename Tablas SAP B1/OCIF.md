# OCIF - Configuration of Intrastat Fields

- **Tabla:** OCIF
- **Descripción:** Configuration of Intrastat Fields
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCIF.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | - |  |  |
| 2 | `ISTable` | Intrastat Wizard Table | nVarChar | 4 | - |  |  |
| 3 | `ISField` | Intrastat Wizard Field Alias | nVarChar | 10 | - |  |  |
| 4 | `FieldDesc` | Field Description | nVarChar | 200 | - |  |  |
| 5 | `FlLocation` | Field Location | nVarChar | 200 | - |  |  |
| 6 | `FldSource` | Source of the Field Value | nVarChar | 200 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
