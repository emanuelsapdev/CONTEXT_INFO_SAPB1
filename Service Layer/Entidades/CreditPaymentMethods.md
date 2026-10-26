# CreditPaymentMethods — Vías de pago con tarjeta de crédito

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `CreditPaymentMethods`
- **Descripción (ES):** Vías de pago con tarjeta de crédito
- **Entity type:** `CreditPaymentMethod` (open type: accepts dynamic/UDF properties)
- **Key:** `PaymentMethodCode` (Edm.Int32)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 8 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/CreditPaymentMethods?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/CreditPaymentMethods/$count` | Contar |
| Get by key | `GET /b1s/v2/CreditPaymentMethods(1)` | Obtener por clave |
| Create | `POST /b1s/v2/CreditPaymentMethods` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/CreditPaymentMethods(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/CreditPaymentMethods(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/CreditPaymentMethods(1)` (only if the B1 object allows removal) | Borrar |

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `PaymentMethodCode` 🔑 | Edm.Int32 | No | Payment Method Code | Código de vía de pago |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `AssignedtoCreditCard` | Edm.Int32 | Yes | Assignedto Credit Card | Asignado a tarjeta de crédito |
| 4 | `PaymentCode` | Edm.String | Yes | Payment Code | Código de pago |
| 5 | `MinimumCreditAmount` | Edm.Double | Yes | Minimum Credit Amount | Importe mínimo de crédito |
| 6 | `MinimumPaymentAmount` | Edm.Double | Yes | Minimum Payment Amount | Importe mínimo de pago |
| 7 | `MaxQtyWithoutApproval` | Edm.Double | Yes | Max Quantity Without Approval | Cantidad máxima sin autorización |
| 8 | `InstallmentPaymentsPossible` | [InstallmentPaymentsPossiblityEnum](../Enums/InstallmentPaymentsPossiblityEnum.md) | Yes | Installment Payments Possible | Pagos en cuotas posibles |

## Navigation properties (2)

Use `GET /b1s/v2/CreditPaymentMethods(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `CreditCard` | [CreditCard](../Entidades/CreditCards.md) | [CreditCards](CreditCards.md) | AssignedtoCreditCard → CreditCardCode | Tarjeta de crédito |
| `CreditCardPayment` | [CreditCardPayment](../Entidades/CreditCardPayments.md) | [CreditCardPayments](CreditCardPayments.md) | PaymentCode → DueDateCode | Pagos con tarjeta de crédito |
