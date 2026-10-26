# OTCX - Tax Code Determination

- **Tabla:** OTCX
- **Descripción:** Tax Code Determination
- **Cantidad de campos:** 42
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OTCX.html

## Campos (42)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Document ID | Int | 11 | - |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `DocType` | Document Type | Int | 11 | - |  | `0` = Item<br>`1` = Service<br>`2` = Item & Service |
| 4 | `BusArea` | Business Area | Int | 11 | - |  | `0` = Sales<br>`1` = Purchase<br>`2` = Sales & Purchase |
| 5 | `Cond1` | Condition 1 | Int | 11 | - |  | `0`<br>`1` = Federal Tax ID<br>`2` = Ship-To Address<br>`3` = Ship-To Street / PO Box<br>`4` = Ship-To City<br>`5` = Ship-To ZIP Code<br>`6` = Ship-To County<br>`7` = Ship-To State<br>`8` = Ship-to Country/Region<br>`9` = Item<br>`10` = Item Group<br>`11` = Business Partner<br>`12` = Customer Group<br>`13` = Vendor Group<br>`14` = Warehouse<br>`15` = G/L Account<br>`16` = Customer Equalization tax<br>`17` = Tax Status<br>`18` = Freight<br>`19` = UDF<br>`20` = Branch<br>`21` = Type of Business |
| 6 | `UDFTable1` | UDF Table Name | nVarChar | 20 | - |  |  |
| 7 | `NumVal1` | Numeric Value | Int | 11 | - |  |  |
| 8 | `StrVal1` | String Value | nVarChar | 100 | - |  |  |
| 9 | `MnyVal1` | Monetary Value | Num | 19.6 | - |  |  |
| 10 | `Cond2` | Condition 2 | Int | 11 | - |  | `0`<br>`1` = Federal Tax ID<br>`2` = Ship-To Address<br>`3` = Ship-To Street / PO Box<br>`4` = Ship-To City<br>`5` = Ship-To ZIP Code<br>`6` = Ship-To County<br>`7` = Ship-To State<br>`8` = Ship-to Country/Region<br>`9` = Item<br>`10` = Item Group<br>`11` = Business Partner<br>`12` = Customer Group<br>`13` = Vendor Group<br>`14` = Warehouse<br>`15` = G/L Account<br>`16` = Customer Equalization tax<br>`17` = Tax Status<br>`18` = Freight<br>`19` = UDF<br>`20` = Branch<br>`21` = Type of Business |
| 11 | `UDFTable2` | UDF Table Name | nVarChar | 20 | - |  |  |
| 12 | `NumVal2` | Numeric Value | Int | 11 | - |  |  |
| 13 | `StrVal2` | String Value | nVarChar | 100 | - |  |  |
| 14 | `MnyVal2` | Monetary Value | Num | 19.6 | - |  |  |
| 15 | `Cond3` | Condition 3 | Int | 11 | - |  | `0`<br>`1` = Federal Tax ID<br>`2` = Ship-To Address<br>`3` = Ship-To Street / PO Box<br>`4` = Ship-To City<br>`5` = Ship-To ZIP Code<br>`6` = Ship-To County<br>`7` = Ship-To State<br>`8` = Ship-to Country/Region<br>`9` = Item<br>`10` = Item Group<br>`11` = Business Partner<br>`12` = Customer Group<br>`13` = Vendor Group<br>`14` = Warehouse<br>`15` = G/L Account<br>`16` = Customer Equalization tax<br>`17` = Tax Status<br>`18` = Freight<br>`19` = UDF<br>`20` = Branch<br>`21` = Type of Business |
| 16 | `UdfTable3` | UDF Table Name | nVarChar | 20 | - |  |  |
| 17 | `NumVal3` | Numeric Value | Int | 11 | - |  |  |
| 18 | `StrVal3` | String Value | nVarChar | 100 | - |  |  |
| 19 | `MnyVal3` | Monetary Value | Num | 19.6 | - |  |  |
| 20 | `Cond4` | Condition 4 | Int | 11 | - |  | `0`<br>`1` = Federal Tax ID<br>`2` = Ship-To Address<br>`3` = Ship-To Street / PO Box<br>`4` = Ship-To City<br>`5` = Ship-To ZIP Code<br>`6` = Ship-To County<br>`7` = Ship-To State<br>`8` = Ship-to Country/Region<br>`9` = Item<br>`10` = Item Group<br>`11` = Business Partner<br>`12` = Customer Group<br>`13` = Vendor Group<br>`14` = Warehouse<br>`15` = G/L Account<br>`16` = Customer Equalization tax<br>`17` = Tax Status<br>`18` = Freight<br>`19` = UDF<br>`20` = Branch<br>`21` = Type of Business |
| 21 | `UdfTable4` | UDF Table Name | nVarChar | 20 | - |  |  |
| 22 | `NumVal4` | Numeric Value | Int | 11 | - |  |  |
| 23 | `StrVal4` | String Value | nVarChar | 100 | - |  |  |
| 24 | `MnyVal4` | Monetary Value | Num | 19.6 | - |  |  |
| 25 | `Cond5` | Condition 5 | Int | 11 | - |  | `0`<br>`1` = Federal Tax ID<br>`2` = Ship-To Address<br>`3` = Ship-To Street / PO Box<br>`4` = Ship-To City<br>`5` = Ship-To ZIP Code<br>`6` = Ship-To County<br>`7` = Ship-To State<br>`8` = Ship-to Country/Region<br>`9` = Item<br>`10` = Item Group<br>`11` = Business Partner<br>`12` = Customer Group<br>`13` = Vendor Group<br>`14` = Warehouse<br>`15` = G/L Account<br>`16` = Customer Equalization tax<br>`17` = Tax Status<br>`18` = Freight<br>`19` = UDF<br>`20` = Branch<br>`21` = Type of Business |
| 26 | `UdfTable5` | UDF Table Name | nVarChar | 20 | - |  |  |
| 27 | `NumVal5` | Numeric Value | Int | 11 | - |  |  |
| 28 | `StrVal5` | String Value | nVarChar | 100 | - |  |  |
| 29 | `MnyVal5` | Monetary Value | Num | 19.6 | - |  |  |
| 30 | `Descr` | Description | nVarChar | 250 | - |  |  |
| 31 | `LnTaxCode` | Line Tax Code | nVarChar | 8 | - |  |  |
| 32 | `FrLnTax` | Line Freight Tax | nVarChar | 8 | - |  |  |
| 33 | `FrHdrTax` | Header Freight Tax | nVarChar | 8 | - |  |  |
| 34 | `UDFAlias1` | UDF Field Alias | nVarChar | 18 | - |  |  |
| 35 | `UDFAlias2` | UDF Field Alias | nVarChar | 18 | - |  |  |
| 36 | `UDFAlias3` | UDF Field Alias | nVarChar | 18 | - |  |  |
| 37 | `UDFAlias4` | UDF Field Alias | nVarChar | 18 | - |  |  |
| 38 | `UDFAlias5` | UDF Field Alias | nVarChar | 18 | - |  |  |
| 39 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |
| 40 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 41 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 42 | `UserSign2` | Update User | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry |
