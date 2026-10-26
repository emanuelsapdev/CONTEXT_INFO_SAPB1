# TCD1 - Key Fields for Determination

- **Tabla:** TCD1
- **Descripción:** Key Fields for Determination
- **Cantidad de campos:** 21
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TCD1.html

## Campos (21)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | - |  |  |
| 2 | `TcdId` | Tax Determination Code | Int | 11 | [OTCD](OTCD.md) |  |  |
| 3 | `KeyFld_1` | Key Fields 1 | Int | 11 | - | 0 |  |
| 4 | `KeyFld_2` | Key Fields 2 | Int | 11 | - | 0 |  |
| 5 | `KeyFld_3` | Key Fields 3 | Int | 11 | - | 0 |  |
| 6 | `Priority` | Priority | Int | 11 | - | 0 |  |
| 7 | `Descr` | Description | nVarChar | 100 | - |  |  |
| 8 | `KeyFld_4` | Key Fields 4 | Int | 11 | - | 0 |  |
| 9 | `UDFTable_1` | UDF Table Name 1 | nVarChar | 20 | - |  |  |
| 10 | `UDFAlias_1` | UDF Field Alias 1 | nVarChar | 18 | - |  |  |
| 11 | `UDFTable_2` | UDF Table Name 2 | nVarChar | 20 | - |  |  |
| 12 | `UDFAlias_2` | UDF Field Alias 2 | nVarChar | 18 | - |  |  |
| 13 | `UDFTable_3` | UDF Table Name 3 | nVarChar | 20 | - |  |  |
| 14 | `UDFAlias_3` | UDF Field Alias 3 | nVarChar | 18 | - |  |  |
| 15 | `UDFTable_4` | UDF Table Name 4 | nVarChar | 20 | - |  |  |
| 16 | `UDFAlias_4` | UDF Field Alias 4 | nVarChar | 18 | - |  |  |
| 17 | `KeyFld_5` | Key Fields 5 | Int | 11 | - | 0 |  |
| 18 | `UDFTable_5` | UDF Table Name 5 | nVarChar | 20 | - |  |  |
| 19 | `UDFAlias_5` | UDF Field Alias 5 | nVarChar | 18 | - |  |  |
| 20 | `LegalText` | Legal Text | nVarChar | 250 | - |  |  |
| 21 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
| TCD1_UNI | Yes | TcdId, Priority |
