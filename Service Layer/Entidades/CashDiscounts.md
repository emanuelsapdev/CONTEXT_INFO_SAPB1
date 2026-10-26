# CashDiscounts — Descuentos por pronto pago

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `CashDiscounts`
- **Descripción (ES):** Descuentos por pronto pago
- **Entity type:** `CashDiscount`
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [OCDC](../../Tablas%20SAP%20B1/OCDC.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 6 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/CashDiscounts?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/CashDiscounts/$count` | Contar |
| Get by key | `GET /b1s/v2/CashDiscounts('value')` | Obtener por clave |
| Create | `POST /b1s/v2/CashDiscounts` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/CashDiscounts('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/CashDiscounts('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/CashDiscounts('value')` (only if the B1 object allows removal) | Borrar |

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `ByDate` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | By Date | Por fecha |
| 4 | `Freight` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Freight | Flete |
| 5 | `Tax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Tax | Impuesto |
| 6 | `DiscountLines` | Collection([DiscountLine](../Tipos-Complejos/DiscountLine.md)) | Yes | Discount Lines | Líneas de descuento |

## Navigation properties (1)

Use `GET /b1s/v2/CashDiscounts('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `PaymentTermsTypes` | Collection([PaymentTermsType](../Entidades/PaymentTermsTypes.md)) | [PaymentTermsTypes](PaymentTermsTypes.md) |  | Condiciones de pago |
