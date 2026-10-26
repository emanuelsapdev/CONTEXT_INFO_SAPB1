# OTRX - Transformation Documents

- **Tabla:** OTRX
- **Descripción:** Transformation Documents
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OTRX.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Identity | 11 | - |  |  |
| 2 | `Code` | Code | nVarChar | 20 | - |  |  |
| 3 | `Descr` | Description | nVarChar | 250 | - |  |  |
| 4 | `Type` | Type | nVarChar | 8 | - | XSLT | `XSLT` = XSLT Document |
| 5 | `Data` | Data | Text | 16 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| CODE | Yes | Code |
