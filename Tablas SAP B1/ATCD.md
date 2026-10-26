# ATCD - Tax Code Determination - History

- **Tabla:** ATCD
- **Descripción:** Tax Code Determination - History
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ATCD.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | - |  |  |
| 2 | `TcdType` | Determination Type | nVarChar | 2 | - | MI | `MI` = Material Item<br>`SI` = Service Item<br>`SD` = Service Document<br>`WT` = Withholding Tax |
| 3 | `DftArCode` | Default Sales Tax Code | nVarChar | 8 | - |  |  |
| 4 | `DftApCode` | Default Purchase Tax Code | nVarChar | 8 | - |  |  |
| 5 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |
| 6 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 7 | `UserSign2` | Update User | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId, LogInstanc |
| TCD_TYPE | Yes | TcdType, LogInstanc |
