# ITL1 - Srl & Batch Details in Transac

- **Tabla:** ITL1
- **Descripción:** Srl & Batch Details in Transac
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ITL1.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `LogEntry` | Log Internal ID | Int | 11 | [OITL](OITL.md) |  |  |
| 2 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 3 | `SysNumber` | System Number | Int | 11 | - |  |  |
| 4 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 5 | `AllocQty` | Allocated Quantity | Num | 19.6 | - |  |  |
| 6 | `MdAbsEntry` | MD Abs Entry | Int | 11 | - |  |  |
| 7 | `ReleaseQty` | Release Quantity | Num | 19.6 | - |  |  |
| 8 | `PickedQty` | Picked Quantity | Num | 19.6 | - |  |  |
| 9 | `OrderedQty` | Ordered Quantity | Num | 19.6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | LogEntry, ItemCode, SysNumber |
| SNB_SYSID | No | ItemCode, SysNumber |
