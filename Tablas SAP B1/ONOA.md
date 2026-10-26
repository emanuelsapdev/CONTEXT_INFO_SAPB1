# ONOA - Nature of Assessee

- **Tabla:** ONOA
- **Descripción:** Nature of Assessee
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ONOA.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | - |  |  |
| 2 | `Code` | Code | nVarChar | 4 | - |  |  |
| 3 | `Descr` | Description | nVarChar | 100 | - |  |  |
| 4 | `AsseType` | Assessee Type | VarChar | 1 | - | C | `C` = Company<br>`P` = Others |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
| CODE | Yes | Code |
