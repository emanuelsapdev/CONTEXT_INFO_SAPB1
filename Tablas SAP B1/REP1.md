# REP1 - Translation Metadata for Web Client Reports

- **Tabla:** REP1
- **Descripción:** Translation Metadata for Web Client Reports
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/REP1.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Guid` | Report Guid | nVarChar | 32 | [OREP](OREP.md) |  |  |
| 2 | `Name` | Report Name | nVarChar | 250 | - |  |  |
| 3 | `Language` | Language Code | Int | 11 | [OLNG](OLNG.md) |  |  |
| 4 | `Property` | Translate Property | Text | 16 | - |  |  |
| 5 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 6 | `UpdateDate` | Update Date | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Guid, Language |
