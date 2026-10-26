# OUNCL - PEPPOL BIS Code Lists

- **Tabla:** OUNCL
- **Descripción:** PEPPOL BIS Code Lists
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OUNCL.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `Codelist` | Code List | Int | 11 | - |  | `1` = Order Type Code<br>`2` = Delivery Type Code<br>`3` = Invoice Type Code<br>`4` = Credit Note Type Code<br>`5` = Standard Item Type Identification Code<br>`6` = Item Commodity Classification Code |
| 3 | `Code` | Code | nVarChar | 20 | - |  |  |
| 4 | `Descrip` | Description | nVarChar | 254 | - |  |  |
| 5 | `SchemaCode` | Schema Code | nVarChar | 20 | - |  |  |
| 6 | `SchemaDesc` | Schema Description | nVarChar | 254 | - |  |  |
| 7 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 8 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 9 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 10 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 11 | `IsDefault` | Is Default | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| Code | Yes | Codelist, Code, SchemaCode |
| IsDefault | No | IsDefault |
