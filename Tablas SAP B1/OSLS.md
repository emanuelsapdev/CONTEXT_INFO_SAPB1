# OSLS - Short Link Mapping

- **Tabla:** OSLS
- **Descripción:** Short Link Mapping
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSLS.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Guid` | GUID for short link | nVarChar | 40 | - |  |  |
| 2 | `Origin` | The origin of source link | nVarChar | 128 | - |  |  |
| 3 | `SrcLink` | The source link URL | Text | 16 | - |  |  |
| 4 | `OwnerCode` | The creator user code | nVarChar | 50 | - |  |  |
| 5 | `CreateDate` | Date | Date | 8 | - |  |  |
| 6 | `CreateTime` | Time | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Guid |
