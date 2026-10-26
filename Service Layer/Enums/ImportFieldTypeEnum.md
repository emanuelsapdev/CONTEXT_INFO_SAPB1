# ImportFieldTypeEnum — Tipo de campo de importación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ImportFieldTypeEnum`
- **Descripción (ES):** Tipo de campo de importación
- **Underlying type:** Edm.Int32
- **Members:** 8

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `iftInvalid` | 0 | Invalid | Inválido |
| `iftFederalTaxID` | 1 | Federal Tax ID | ID fiscal federal |
| `iftAdditionalID` | 2 | Additional ID | ID adicional |
| `iftUnifiedFederalTaxID` | 3 | Unified Federal Tax ID | ID fiscal federal unificado |
| `iftCNPJ` | 4 | CNPJ | CNPJ |
| `iftAliasName` | 5 | Alias Name | Alias |
| `iftIBAN` | 6 | IBAN | IBAN |
| `iftBPName` | 7 | Business Partner Name | Nombre del socio de negocios |

## Used by (1 properties)

- [ImportDetermination](../Entidades/ImportDeterminations.md).`FieldType`
