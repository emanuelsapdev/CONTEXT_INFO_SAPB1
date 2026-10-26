# OTPL - Import Template

- **Tabla:** OTPL
- **Descripción:** Import Template
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OTPL.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TplNum` | Template Number | Int | 11 | - |  |  |
| 2 | `TplName` | Template Name | nVarChar | 100 | - |  |  |
| 3 | `TplType` | Template Type | nVarChar | 5 | - |  | `T` = Target BPs<br>`B` = BP<br>`I` = Items<br>`F` = Fixed Asset<br>`WB` = WebClient BP<br>`WBCP` = WebClient BP Contact Person<br>`WBAD` = WebClient BP Address<br>`WBPM` = WebClient BP Payment Method<br>`WBCA` = WebClient BP Control Accounts<br>`WJ` = WebClient Journal Entry<br>`WJE1` = WebClient JE line1<br>`WJE2` = WebClient JE line2<br>`WI` = WebClient Items<br>`WIP` = WebClient Items Prices<br>`WIW` = WebClient Items Warehouses |
| 4 | `TplCode` | Template Code | nVarChar | 20 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TplNum |
| CODE | Yes | TplCode, TplType |
