# BPBranchAssignmentItem — Asignación de sucursal al socio de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BPBranchAssignmentItem`
- **Descripción (ES):** Asignación de sucursal al socio de negocios
- **Description (EN):** Business Partner Branch Assignment Item
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `BPCode` | Edm.String | Yes | Business Partner Code | Código del socio de negocios |
| 2 | `BPLID` | Edm.Int32 | Yes | BPLID | ID de sucursal |
| 3 | `DisabledForBP` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Disabled For Business Partner | Deshabilitado para el socio de negocios |

## Used by (properties)

- [BusinessPartner](../Entidades/BusinessPartners.md).`BPBranchAssignment`
