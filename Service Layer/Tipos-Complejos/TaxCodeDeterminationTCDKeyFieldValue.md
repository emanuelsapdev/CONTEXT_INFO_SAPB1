# TaxCodeDeterminationTCDKeyFieldValue — Valores de campos clave TCD

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `TaxCodeDeterminationTCDKeyFieldValue`
- **Descripción (ES):** Valores de campos clave TCD
- **Description (EN):** Tax Code Determination TCD Key Field Value

- **Properties:** 9

## Properties (9)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsId` | Edm.Int32 | Yes | Abs ID | ID absoluto |
| 2 | `DispOrder` | Edm.Int32 | Yes | Disp Order | Orden de visualización |
| 3 | `KeyFld_1_V` | Edm.String | Yes | Key Fld 1 V | Valor del campo clave 1 |
| 4 | `KeyFld_2_V` | Edm.String | Yes | Key Fld 2 V | Valor del campo clave 2 |
| 5 | `KeyFld_3_V` | Edm.String | Yes | Key Fld 3 V | Valor del campo clave 3 |
| 6 | `KeyFld_4_V` | Edm.String | Yes | Key Fld 4 V | Valor del campo clave 4 |
| 7 | `KeyFld_5_V` | Edm.String | Yes | Key Fld 5 V | Valor del campo clave 5 |
| 8 | `TaxCodeDeterminationTCDKeyFieldValuePeriods` | Collection([TaxCodeDeterminationTCDKeyFieldValuePeriod](../Tipos-Complejos/TaxCodeDeterminationTCDKeyFieldValuePeriod.md)) | Yes | Tax Code Determination TCD Key Field Value Periods | Períodos del valor de campo clave TCD |
| 9 | `TaxCodeDeterminationTCDKeyFieldValueDefaultWTs` | Collection([TaxCodeDeterminationTCDKeyFieldValueDefaultWT](../Tipos-Complejos/TaxCodeDeterminationTCDKeyFieldValueDefaultWT.md)) | Yes | Tax Code Determination TCD Key Field Value Default W Ts | Retenciones predeterminadas por valor de campo clave TCD |

## Used by (properties)

- [TaxCodeDeterminationTCDKeyField](TaxCodeDeterminationTCDKeyField.md).`TaxCodeDeterminationTCDKeyFieldValues`
