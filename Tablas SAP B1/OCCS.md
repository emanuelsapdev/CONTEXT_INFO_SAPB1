# OCCS - Cycle Count Determination

- **Tabla:** OCCS
- **Descripción:** Cycle Count Determination
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCCS.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WhsCode` | Warehouse Code | nVarChar | 8 | - |  |  |
| 2 | `CycleType` | Cycle Type | VarChar | 1 | - | G | `G` = Item Group<br>`S` = Sublevel |
| 3 | `CycleBy` | Cycle By | Int | 6 | - | 0 | `0` = Item Group<br>`1` = Warehouse Sublevel 1<br>`2` = Warehouse Sublevel 2<br>`3` = Warehouse Sublevel 3<br>`4` = Warehouse Sublevel 4 |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WhsCode |
