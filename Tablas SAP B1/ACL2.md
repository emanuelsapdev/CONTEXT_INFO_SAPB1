# ACL2 - Activity Multiple Recipients - History

- **Tabla:** ACL2
- **Descripción:** Activity Multiple Recipients - History
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ACL2.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ClgCode` | Activity Number | Int | 11 | [OCLG](OCLG.md) |  |  |
| 2 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 3 | `ObjType` | Object Type | nVarChar | 20 | - | 12 | `12` = User<br>`171` = Employee |
| 4 | `ObjCode` | Object Code | nVarChar | 50 | - |  |  |
| 5 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ClgCode, LineNum, LogInstanc |
