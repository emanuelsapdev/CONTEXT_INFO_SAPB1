# WVT7 - Variant -- embedded chart size

- **Tabla:** WVT7
- **Descripción:** Variant -- embedded chart size
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WVT7.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RootId` | Root Guid | nVarChar | 40 | - |  |  |
| 2 | `ParentId` | Parent Id | nVarChar | 40 | - |  |  |
| 3 | `Guid` | Guid | nVarChar | 40 | - |  |  |
| 4 | `Order` | Order | Int | 11 | - |  |  |
| 5 | `ColName` | Column Name | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RootId, ParentId, Guid |
