# WitholdingTaxDefinition — Definición de retención de impuestos (localización)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `WitholdingTaxDefinition`
- **Descripción (ES):** Definición de retención de impuestos (localización)
- **Entity type:** `WTDCode` (open type: accepts dynamic/UDF properties)
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 28 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/WitholdingTaxDefinition?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/WitholdingTaxDefinition/$count` | Contar |
| Get by key | `GET /b1s/v2/WitholdingTaxDefinition(1)` | Obtener por clave |
| Create | `POST /b1s/v2/WitholdingTaxDefinition` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/WitholdingTaxDefinition(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/WitholdingTaxDefinition(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/WitholdingTaxDefinition(1)` (only if the B1 object allows removal) | Borrar |

## Properties (28)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `WTaxCode` | Edm.String | Yes | W Tax Code | Código de retención |
| 3 | `WTaxName` | Edm.String | Yes | W Tax Name | Nombre de la retención |
| 4 | `FormulaID` | Edm.Int32 | Yes | Formula ID | ID de fórmula |
| 5 | `Inactive` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Inactive | Inactivo |
| 6 | `OfficialCode` | Edm.String | Yes | Official Code | Código oficial |
| 7 | `Category` | [WithholdingTaxCodeCategoryEnum](../Enums/WithholdingTaxCodeCategoryEnum.md) | Yes | Category | Categoría |
| 8 | `BaseType` | [WithholdingTaxCodeBaseTypeEnum](../Enums/WithholdingTaxCodeBaseTypeEnum.md) | Yes | Base Type | Tipo base (tipo de objeto del documento base) |
| 9 | `Type` | Edm.Int32 | Yes | Type | Tipo |
| 10 | `MinAmount` | Edm.Double | Yes | Min Amount | Importe mínimo |
| 11 | `BaseAmountPrct` | Edm.Double | Yes | Base Amount Percent | Porcentaje del importe base |
| 12 | `SlidingScaleProgressiveTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Sliding Scale Progressive Tax | Impuesto progresivo por escala |
| 13 | `CalculateInAutomaticCM` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Calculate In Automatic CM | Calcular en nota de crédito automática |
| 14 | `U_B1SYS_B1Company` | Edm.String | Yes | [AR localization] B 1 Company | [Loc. AR] Sociedad SAP Business One |
| 15 | `U_B1SYS_Relevance` | Edm.String | Yes | [AR localization] Relevance | [Loc. AR] Relevancia |
| 16 | `U_B1SYS_Installments` | Edm.String | Yes | [AR localization] Installments | [Loc. AR] Aplica por cuotas |
| 17 | `U_B1SYS_ReproWeb` | Edm.String | Yes | [AR localization] Repro Web | [Loc. AR] Relevante para ReproWeb |
| 18 | `U_B1SYS_ResultMin` | Edm.Double | Yes | [AR localization] Result Min | [Loc. AR] Resultado mínimo (importe mínimo de retención) |
| 19 | `U_B1SYS_CreditMemo` | Edm.String | Yes | [AR localization] Credit Memo | [Loc. AR] Aplica a notas de crédito |
| 20 | `U_B1SYS_WhtType` | Edm.String | Yes | [AR localization] Wht Type | [Loc. AR] Tipo de retención/percepción |
| 21 | `U_B1SYS_JurisFrom` | Edm.String | Yes | [AR localization] Juris From | [Loc. AR] Jurisdicción desde |
| 22 | `U_B1SYS_JurisTo` | Edm.String | Yes | [AR localization] Juris To | [Loc. AR] Jurisdicción hasta |
| 23 | `U_B1SYS_AccumGroup` | Edm.String | Yes | [AR localization] Accum Group | [Loc. AR] Grupo de acumulación de retenciones |
| 24 | `U_B1SYS_WTCSeries` | Edm.Int32 | No | [AR localization] WTC Series | [Loc. AR] Serie de certificados de retención |
| 25 | `WTDEffectiveDateCollection` | Collection([WTDEffectiveDate](../Tipos-Complejos/WTDEffectiveDate.md)) | Yes | WTD Effective Date Collection | [Loc. AR] Colección de fechas de vigencia de la definición de retención |
| 26 | `WTDBPCollection` | Collection([WTDBP](../Tipos-Complejos/WTDBP.md)) | Yes | WTDBP Collection | [Loc. AR] Colección de socios de negocios de la definición de retención |
| 27 | `WTDItemCollection` | Collection([WTDItem](../Tipos-Complejos/WTDItem.md)) | Yes | WTD Item Collection | [Loc. AR] Colección de artículos de la definición de retención |
| 28 | `WTDFreightCollection` | Collection([WTDFreight](../Tipos-Complejos/WTDFreight.md)) | Yes | WTD Freight Collection | [Loc. AR] Colección de gastos adicionales de la definición de retención |
