# OSRQ - Serial No. Quantities

- **Tabla:** OSRQ
- **Descripción:** Serial No. Quantities
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSRQ.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 2 | `SysNumber` | System Number | Int | 11 | [OSRN](OSRN.md) |  |  |
| 3 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 4 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 5 | `CommitQty` | Committed Quantity | Num | 19.6 | - |  |  |
| 6 | `CountQty` | Counted Quantity | Num | 19.6 | - |  |  |
| 7 | `AbsEntry` | abs entry | Int | 11 | - |  |  |
| 8 | `MdAbsEntry` | MD Abs Entry | Int | 11 | [OSRN](OSRN.md) |  |  |
| 9 | `TrackingNt` | CCD Tracking Note | Int | 11 | [OTCN](OTCN.md) |  |  |
| 10 | `TrackiNtLn` | CCD Tracking Note Line | Int | 11 | [TCN1](TCN1.md) |  |  |
| 11 | `CCDQuant` | CCD Quantity | Num | 19.6 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| SYSTEM_KEY | Yes | ItemCode, SysNumber, WhsCode |
| MDABS_KEY | No | MdAbsEntry |
