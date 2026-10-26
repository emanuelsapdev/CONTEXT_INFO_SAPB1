# ATCD2 - Key Field Values

- **Tabla:** ATCD2
- **Descripción:** Key Field Values
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ATCD2.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | - |  |  |
| 2 | `Tcd1Id` | Tax Determination ID | Int | 11 | [TCD1](TCD1.md) |  |  |
| 3 | `DispOrder` | Display Order | Int | 11 | - |  |  |
| 4 | `KeyFld_1_V` | Key Fields 1 Value | nVarChar | 50 | - |  |  |
| 5 | `KeyFld_2_V` | Key Fields 2 Value | nVarChar | 50 | - |  |  |
| 6 | `KeyFld_3_V` | Key Fields 3 Value | nVarChar | 50 | - |  |  |
| 7 | `KeyFld_4_V` | Key Fields 4 Value | nVarChar | 50 | - |  |  |
| 8 | `KeyFld_5_V` | Key Fields 5 Value | nVarChar | 50 | - |  |  |
| 9 | `TcdId` | Tax Determination Code | Int | 11 | [OTCD](OTCD.md) |  |  |
| 10 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId, LogInstanc |
| TCD2_UNI | Yes | Tcd1Id, DispOrder, LogInstanc |
