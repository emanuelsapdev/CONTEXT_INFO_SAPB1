# ITW1 - Item Count Alert

- **Tabla:** ITW1
- **Descripción:** Item Count Alert
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ITW1.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 2 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 3 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 4 | `CycleCode` | Cycle Code | Int | 6 | [OCYC](OCYC.md) |  |  |
| 5 | `Alert` | Alert | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 6 | `NextDate` | Next Counting Date | Date | 8 | - |  |  |
| 7 | `Time` | Alert Time | Int | 6 | - |  |  |
| 8 | `DestUser` | Destination User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 9 | `Alerted` | Alerted | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `BinAbs` | Bin Internal Number | Int | 11 | [OBIN](OBIN.md) | -1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ItemCode, WhsCode, BinAbs |
