# GDP3 - General Data Protection Wizard - Processed Documents

- **Tabla:** GDP3
- **Descripción:** General Data Protection Wizard - Processed Documents
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GDP3.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OGDP](OGDP.md) |  |  |
| 2 | `LineNum` | Line | Int | 6 | - |  |  |
| 3 | `RefObjType` | Referenced Object Type | nVarChar | 20 | - |  |  |
| 4 | `RefObjKey1` | Referenced Object Key | nVarChar | 20 | - |  |  |
| 5 | `RefObjKey2` | Referenced Object Subkey | nVarChar | 20 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum |
| NATOBJ_KEY | Yes | AbsEntry, RefObjType, RefObjKey1, RefObjKey2 |
