# TaxCodeDeterminations — Determinación de indicadores de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `TaxCodeDeterminations`
- **Descripción (ES):** Determinación de indicadores de impuestos
- **Entity type:** `TaxCodeDetermination`
- **Key:** `DocEntry` (Edm.Int32)
- **DB tables (main / lines):** [OTCD](../../Tablas%20SAP%20B1/OTCD.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 38 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/TaxCodeDeterminations?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/TaxCodeDeterminations/$count` | Contar |
| Get by key | `GET /b1s/v2/TaxCodeDeterminations(1)` | Obtener por clave |
| Create | `POST /b1s/v2/TaxCodeDeterminations` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/TaxCodeDeterminations(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/TaxCodeDeterminations(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/TaxCodeDeterminations(1)` (only if the B1 object allows removal) | Borrar |

## Properties (38)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` 🔑 | Edm.Int32 | No | Document Entry | DocEntry (clave interna del documento) |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `DocumentType` | [BoTCDDocumentTypeEnum](../Enums/BoTCDDocumentTypeEnum.md) | Yes | Document Type | Tipo de documento |
| 4 | `BusinessArea` | [BoBusinessAreaEnum](../Enums/BoBusinessAreaEnum.md) | Yes | Business Area | Área de negocio |
| 5 | `Condition1` | [BoTCDConditionEnum](../Enums/BoTCDConditionEnum.md) | Yes | Condition 1 | Condición 1 |
| 6 | `UDFTable1` | Edm.String | Yes | UDF Table 1 | Tabla de UDF 1 |
| 7 | `NumberValue1` | Edm.Int32 | Yes | Number Value 1 | Valor numérico 1 |
| 8 | `StringValue1` | Edm.String | Yes | String Value 1 | Valor de cadena 1 |
| 9 | `MoneyValue1` | Edm.Double | Yes | Money Value 1 | Valor monetario 1 |
| 10 | `Condition2` | [BoTCDConditionEnum](../Enums/BoTCDConditionEnum.md) | Yes | Condition 2 | Condición 2 |
| 11 | `UDFTable2` | Edm.String | Yes | UDF Table 2 | Tabla de UDF 2 |
| 12 | `NumberValue2` | Edm.Int32 | Yes | Number Value 2 | Valor numérico 2 |
| 13 | `StringValue2` | Edm.String | Yes | String Value 2 | Valor de cadena 2 |
| 14 | `MoneyValue2` | Edm.Double | Yes | Money Value 2 | Valor monetario 2 |
| 15 | `Condition3` | [BoTCDConditionEnum](../Enums/BoTCDConditionEnum.md) | Yes | Condition 3 | Condición 3 |
| 16 | `UDFTable3` | Edm.String | Yes | UDF Table 3 | Tabla de UDF 3 |
| 17 | `NumberValue3` | Edm.Int32 | Yes | Number Value 3 | Valor numérico 3 |
| 18 | `StringValue3` | Edm.String | Yes | String Value 3 | Valor de cadena 3 |
| 19 | `MoneyValue3` | Edm.Double | Yes | Money Value 3 | Valor monetario 3 |
| 20 | `Condition4` | [BoTCDConditionEnum](../Enums/BoTCDConditionEnum.md) | Yes | Condition 4 | Condición 4 |
| 21 | `UDFTable4` | Edm.String | Yes | UDF Table 4 | Tabla de UDF 4 |
| 22 | `NumberValue4` | Edm.Int32 | Yes | Number Value 4 | Valor numérico 4 |
| 23 | `StringValue4` | Edm.String | Yes | String Value 4 | Valor de cadena 4 |
| 24 | `MoneyValue4` | Edm.Double | Yes | Money Value 4 | Valor monetario 4 |
| 25 | `Condition5` | [BoTCDConditionEnum](../Enums/BoTCDConditionEnum.md) | Yes | Condition 5 | Condición 5 |
| 26 | `UDFTable5` | Edm.String | Yes | UDF Table 5 | Tabla de UDF 5 |
| 27 | `NumberValue5` | Edm.Int32 | Yes | Number Value 5 | Valor numérico 5 |
| 28 | `StringValue5` | Edm.String | Yes | String Value 5 | Valor de cadena 5 |
| 29 | `MoneyValue5` | Edm.Double | Yes | Money Value 5 | Valor monetario 5 |
| 30 | `Description` | Edm.String | Yes | Description | Descripción |
| 31 | `TaxCode` | Edm.String | Yes | Tax Code | Indicador de impuesto |
| 32 | `FreightRowTax` | Edm.String | Yes | Freight Row Tax | Impuesto de gastos adicionales de línea |
| 33 | `FreightHeaderTax` | Edm.String | Yes | Freight Header Tax | Impuesto de gastos adicionales de cabecera |
| 34 | `UDFAlias1` | Edm.String | Yes | UDF Alias 1 | Alias de UDF 1 |
| 35 | `UDFAlias2` | Edm.String | Yes | UDF Alias 2 | Alias de UDF 2 |
| 36 | `UDFAlias3` | Edm.String | Yes | UDF Alias 3 | Alias de UDF 3 |
| 37 | `UDFAlias4` | Edm.String | Yes | UDF Alias 4 | Alias de UDF 4 |
| 38 | `UDFAlias5` | Edm.String | Yes | UDF Alias 5 | Alias de UDF 5 |
