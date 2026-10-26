# GDP2 - General Data Protection Wizard - Natural Persons

- **Tabla:** GDP2
- **Descripción:** General Data Protection Wizard - Natural Persons
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GDP2.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OGDP](OGDP.md) |  |  |
| 2 | `LineNum` | Line | Int | 6 | - |  |  |
| 3 | `NatObjType` | Natural Person Object Type | nVarChar | 20 | - |  |  |
| 4 | `NatObjArr` | Natural Person Object Array | Int | 11 | - |  |  |
| 5 | `NatObjKey1` | Natural Person Object Key | nVarChar | 20 | - |  |  |
| 6 | `NatObjKey2` | Natural Person Object Subkey | nVarChar | 20 | - |  |  |
| 7 | `Result` | Result | Int | 11 | - |  |  |
| 8 | `ErrorStr` | Error String | nVarChar | 254 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum |
| NATOBJ_KEY | Yes | AbsEntry, NatObjType, NatObjArr, NatObjKey1, NatObjKey2 |
