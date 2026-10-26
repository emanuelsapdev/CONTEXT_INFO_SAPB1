# OJSON - JSON Content Repository

- **Tabla:** OJSON
- **Descripción:** JSON Content Repository
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OJSON.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Guid` | Guid | nVarChar | 40 | - |  |  |
| 2 | `Type` | Type | VarChar | 1 | - |  | `F` = Form Preference |
| 3 | `Index1` | User-Defined Indexes | nVarChar | 254 | - |  |  |
| 4 | `Content` | JSON Content | Text | 16 | - |  |  |
| 5 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Guid |
| INDEX1 | Yes | Type, Index1 |
