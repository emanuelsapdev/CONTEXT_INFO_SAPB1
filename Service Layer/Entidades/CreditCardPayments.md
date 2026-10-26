# CreditCardPayments — Pagos con tarjeta de crédito

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `CreditCardPayments`
- **Descripción (ES):** Pagos con tarjeta de crédito
- **Entity type:** `CreditCardPayment` (open type: accepts dynamic/UDF properties)
- **Key:** `DueDateCode` (Edm.String)
- **DB tables (main / lines):** [OCDT](../../Tablas%20SAP%20B1/OCDT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 21 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/CreditCardPayments?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/CreditCardPayments/$count` | Contar |
| Get by key | `GET /b1s/v2/CreditCardPayments('value')` | Obtener por clave |
| Create | `POST /b1s/v2/CreditCardPayments` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/CreditCardPayments('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/CreditCardPayments('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/CreditCardPayments('value')` (only if the B1 object allows removal) | Borrar |

## Properties (21)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DueDateCode` 🔑 | Edm.String | No | Due Date Code | Código de fecha de vencimiento |
| 2 | `DueDateName` | Edm.String | Yes | Due Date Name | Nombre de la fecha de vencimiento |
| 3 | `DueDatesType` | [DueDateTypesEnum](../Enums/DueDateTypesEnum.md) | Yes | Due Dates Type | Tipo de fechas de vencimiento |
| 4 | `PaymentAfterDays` | Edm.Int32 | Yes | Payment After Days | Pago después de días |
| 5 | `PaymentAfterMonths` | Edm.Int32 | Yes | Payment After Months | Pago después de meses |
| 6 | `FromDay1` | Edm.Int32 | Yes | From Day 1 | Desde el día 1 |
| 7 | `ToDay1` | Edm.Int32 | Yes | To Day 1 | Hasta el día 1 |
| 8 | `PaymentDay1` | Edm.Int32 | Yes | Payment Day 1 | Día de pago 1 |
| 9 | `NoOfMonths1` | Edm.Int32 | Yes | Number Of Months 1 | Cantidad de meses 1 |
| 10 | `FromDay2` | Edm.Int32 | Yes | From Day 2 | Desde el día 2 |
| 11 | `ToDay2` | Edm.Int32 | Yes | To Day 2 | Hasta el día 2 |
| 12 | `PaymentDay2` | Edm.Int32 | Yes | Payment Day 2 | Día de pago 2 |
| 13 | `NoOfMonths2` | Edm.Int32 | Yes | Number Of Months 2 | Cantidad de meses 2 |
| 14 | `FromDay3` | Edm.Int32 | Yes | From Day 3 | Desde el día 3 |
| 15 | `ToDay3` | Edm.Int32 | Yes | To Day 3 | Hasta el día 3 |
| 16 | `PaymentDay3` | Edm.Int32 | Yes | Payment Day 3 | Día de pago 3 |
| 17 | `NoOfMonths3` | Edm.Int32 | Yes | Number Of Months 3 | Cantidad de meses 3 |
| 18 | `FromDay4` | Edm.Int32 | Yes | From Day 4 | Desde el día 4 |
| 19 | `ToDay4` | Edm.Int32 | Yes | To Day 4 | Hasta el día 4 |
| 20 | `PaymentDay4` | Edm.Int32 | Yes | Payment Day 4 | Día de pago 4 |
| 21 | `NoOfMonths4` | Edm.Int32 | Yes | Number Of Months 4 | Cantidad de meses 4 |

## Navigation properties (1)

Use `GET /b1s/v2/CreditCardPayments('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `CreditPaymentMethods` | Collection([CreditPaymentMethod](../Entidades/CreditPaymentMethods.md)) | [CreditPaymentMethods](CreditPaymentMethods.md) |  | Vías de pago con tarjeta de crédito |
