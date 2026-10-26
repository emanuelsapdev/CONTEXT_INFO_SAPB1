# WVT2 - Variant -- group by

- **Tabla:** WVT2
- **Descripción:** Variant -- group by
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WVT2.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ParentId` | Parent Id | nVarChar | 40 | - |  |  |
| 2 | `Guid` | Guid | nVarChar | 40 | - |  |  |
| 3 | `Order` | Order | Int | 11 | - |  |  |
| 4 | `ColName` | Column Name | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ParentId, Guid |
