# Payments_ApprovalRequest — Solicitudes de autorización del pago

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `Payments_ApprovalRequest`
- **Descripción (ES):** Solicitudes de autorización del pago
- **Description (EN):** Payments Approval Request

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ApprovalTemplatesID` | Edm.Int32 | Yes | Approval Templates ID | ID del modelo de autorización |
| 2 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 3 | `ApprovalTemplatesName` | Edm.String | Yes | Approval Templates Name | Nombre del modelo de autorización |
| 4 | `ActiveForUpdate` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Active For Update | Activo para actualización |

## Used by (properties)

- [Payment](../Entidades/VendorPayments.md).`Payments_ApprovalRequests`
