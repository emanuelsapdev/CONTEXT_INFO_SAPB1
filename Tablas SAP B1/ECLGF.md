# ECLGF - ECLGF

- **Tabla:** ECLGF
- **Descripción:** ECLGF
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ECLGF.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Id` | Transaction Id | nVarChar | 100 | - |  |  |
| 2 | `FileName` | The configuration file name | nVarChar | 254 | - |  |  |
| 3 | `FileHash` | The file hash code | nVarChar | 100 | - |  |  |
| 4 | `XmlFile` | The file saved as Xml | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Id, FileName |
