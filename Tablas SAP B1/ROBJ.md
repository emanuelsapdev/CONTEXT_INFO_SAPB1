# ROBJ - TM Import/Export Obj

- **Tabla:** ROBJ
- **Descripción:** TM Import/Export Obj
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ROBJ.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsKey` | Absolute Key | Int | 11 | - |  |  |
| 2 | `Name` | Name | nVarChar | 100 | - |  |  |
| 3 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 4 | `UpdateTime` | Update Time | Int | 6 | - | 0 |  |
| 5 | `SentDate` | Date Sent For Trans | Date | 8 | - |  |  |
| 6 | `SentTime` | Time Sent For Trans | Int | 6 | - | 0 |  |
| 7 | `Localztion` | Localization relevance of obj | nVarChar | 2 | - | XX |  |
| 8 | `SntStrCont` | Send Strings Count | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsKey |
| NAME | Yes | Name |
