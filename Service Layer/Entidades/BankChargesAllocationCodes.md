# BankChargesAllocationCodes — Códigos de imputación de comisiones bancarias

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BankChargesAllocationCodes`
- **Descripción (ES):** Códigos de imputación de comisiones bancarias
- **Entity type:** `BankChargesAllocationCode`
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [OBCA](../../Tablas%20SAP%20B1/OBCA.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 2 · **Navigation properties:** 2 · **Bound actions:** 1

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BankChargesAllocationCodes?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BankChargesAllocationCodes/$count` | Contar |
| Get by key | `GET /b1s/v2/BankChargesAllocationCodes('value')` | Obtener por clave |
| Create | `POST /b1s/v2/BankChargesAllocationCodes` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BankChargesAllocationCodes('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BankChargesAllocationCodes('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/BankChargesAllocationCodes('value')` (only if the B1 object allows removal) | Borrar |
| Action `SetDefaultBankChargesAllocationCode` | `POST /b1s/v2/BankChargesAllocationCodes('value')/SetDefaultBankChargesAllocationCode` | Establecer código de imputación de comisiones predeterminado |

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |

## Navigation properties (2)

Use `GET /b1s/v2/BankChargesAllocationCodes('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `PaymentRunExport` | Collection([PaymentRunExport](../Entidades/PaymentRunExport.md)) | [PaymentRunExport](PaymentRunExport.md) |  | Exportación de ejecución de pagos |
| `BusinessPartners` | Collection([BusinessPartner](../Entidades/BusinessPartners.md)) | [BusinessPartners](BusinessPartners.md) |  | Socios de negocios |

## Bound actions (1)

### SetDefaultBankChargesAllocationCode

- **Descripción (ES):** Establecer código de imputación de comisiones predeterminado
- **Request:** `POST /b1s/v2/BankChargesAllocationCodes('value')/SetDefaultBankChargesAllocationCode`

