# OMIV - A/P Monthly Invoice

- **Tabla:** OMIV
- **Descripción:** A/P Monthly Invoice
- **Cantidad de campos:** 19
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OMIV.html

## Campos (19)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Entry` | Internal Key | Int | 11 | - |  |  |
| 2 | `Number` | Monthly Invoice Number | Int | 11 | - |  |  |
| 3 | `Date` | Issued Date | Date | 8 | - |  |  |
| 4 | `BPCode` | Vendor Code | nVarChar | 15 | - |  |  |
| 5 | `BPName` | Vendor Name | nVarChar | 200 | - |  |  |
| 6 | `Currency` | Currency | nVarChar | 3 | - |  |  |
| 7 | `LastBilled` | Last Billed | Num | 19.6 | - |  |  |
| 8 | `Paid` | Paid in the Period | Num | 19.6 | - |  |  |
| 9 | `CarryForw` | Carry Forward | Num | 19.6 | - |  |  |
| 10 | `CurAmount` | Current Amount | Num | 19.6 | - |  |  |
| 11 | `BillAmount` | Billing Amount | Num | 19.6 | - |  |  |
| 12 | `OBPaid` | OB Paid in this Period | Num | 19.6 | - |  |  |
| 13 | `OBLstJENum` | OB Last JE Num in the Period | Int | 11 | - |  |  |
| 14 | `Predeces` | The Former MI Num | Int | 11 | - |  |  |
| 15 | `Successor` | The Latter MI Num | Int | 11 | - |  |  |
| 16 | `Series` | Series | Int | 11 | - |  |  |
| 17 | `Cancelled` | Is Canceled | VarChar | 1 | - | N | `N`<br>`Y` |
| 18 | `Address` | Bill To | nVarChar | 254 | - |  |  |
| 19 | `BPLId` | Branch | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Entry |
| Number | Yes | Number |
