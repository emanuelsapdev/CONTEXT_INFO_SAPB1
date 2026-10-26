# GovPayCodeAuthority — Autoridad del código de pago gubernamental

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `GovPayCodeAuthority`
- **Descripción (ES):** Autoridad del código de pago gubernamental
- **Description (EN):** Gov Pay Code Authority

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsId` | Edm.Int32 | Yes | Abs ID | ID absoluto |
| 2 | `BPLId` | Edm.Int32 | Yes | Branch ID | ID de sucursal |
| 3 | `State` | Edm.String | Yes | State | Estado/provincia |
| 4 | `CardCode` | Edm.String | Yes | Card Code | Código del socio de negocios |

## Used by (properties)

- [GovPayCode](../Entidades/GovPayCodes.md).`GovPayCodeAuthorities`
