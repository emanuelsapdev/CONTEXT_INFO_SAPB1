# AOA2 - Blanket Agreement - Details

- **Tabla:** AOA2
- **Descripción:** Blanket Agreement - Details
- **Cantidad de campos:** 15
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AOA2.html

## Campos (15)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AgrNo` | Agreement No. | Int | 11 | [AOAT](AOAT.md) |  |  |
| 2 | `AgrLnNum` | Agreement Item Row Number | Int | 11 | - |  |  |
| 3 | `AgrEfctNum` | Agreement Effective Row No. | Int | 11 | - |  |  |
| 4 | `DatePeriod` | Frequency | VarChar | 1 | - | M | `D` = Daily<br>`W` = Weekly<br>`M` = Monthly<br>`Q` = Quarterly<br>`S` = Semi-Annually<br>`A` = Annually<br>`O` = One Time |
| 5 | `FromDate` | From Date | Date | 8 | - |  |  |
| 6 | `ToDate` | To Date | Date | 8 | - |  |  |
| 7 | `CallUp` | Release Information | nVarChar | 100 | - |  |  |
| 8 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) | -1 |  |
| 9 | `Quantity` | Item Quantity | Num | 19.6 | - |  |  |
| 10 | `ConsumeFCT` | Consumer Sales Forecast | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 11 | `FreeTxt` | Free Text | nVarChar | 100 | - |  |  |
| 12 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 13 | `AmountLC` | Planned Amount (LC) | Num | 19.6 | - |  |  |
| 14 | `AmountFC` | Planned Amount (FC) | Num | 19.6 | - |  |  |
| 15 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AgrNo, AgrLnNum, AgrEfctNum, LogInstanc |
