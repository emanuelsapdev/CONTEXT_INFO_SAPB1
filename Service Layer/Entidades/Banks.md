# Banks — Bancos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `Banks`
- **Descripción (ES):** Bancos
- **Entity type:** `Bank` (open type: accepts dynamic/UDF properties)
- **Key:** `AbsoluteEntry` (Edm.Int32)
- **DB tables (main / lines):** [ODSC](../../Tablas%20SAP%20B1/ODSC.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 12 · **Navigation properties:** 3 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/Banks?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/Banks/$count` | Contar |
| Get by key | `GET /b1s/v2/Banks(1)` | Obtener por clave |
| Create | `POST /b1s/v2/Banks` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/Banks(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/Banks(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/Banks(1)` (only if the B1 object allows removal) | Borrar |

## Properties (12)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `BankCode` | Edm.String | Yes | Bank Code | Código del banco |
| 2 | `BankName` | Edm.String | Yes | Bank Name | Nombre del banco |
| 3 | `AccountforOutgoingChecks` | Edm.String | Yes | Accountfor Outgoing Checks | Cuenta para cheques emitidos |
| 4 | `BranchforOutgoingChecks` | Edm.String | Yes | Branchfor Outgoing Checks | Sucursal para cheques emitidos |
| 5 | `NextCheckNumber` | Edm.Int32 | Yes | Next Check Number | Siguiente número de cheque |
| 6 | `SwiftNo` | Edm.String | Yes | Swift Number | Número SWIFT |
| 7 | `IBAN` | Edm.String | Yes | IBAN | IBAN |
| 8 | `CountryCode` | Edm.String | Yes | Country Code | Código de país |
| 9 | `PostOffice` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Post Office | Oficina postal |
| 10 | `AbsoluteEntry` 🔑 | Edm.Int32 | No | Absolute Entry | Entrada absoluta (ID interno) |
| 11 | `DefaultBankAccountKey` | Edm.Int32 | Yes | Default Bank Account Key | Clave de cuenta bancaria predeterminada |
| 12 | `DigitalPayments` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Digital Payments | Pagos digitales |

## Navigation properties (3)

Use `GET /b1s/v2/Banks(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `EmployeesInfo` | Collection([EmployeeInfo](../Entidades/EmployeesInfo.md)) | [EmployeesInfo](EmployeesInfo.md) |  | Empleados |
| `Country` | [Country](../Entidades/Countries.md) | [Countries](Countries.md) | CountryCode → Code | País |
| `HouseBankAccounts` | Collection([HouseBankAccount](../Entidades/HouseBankAccounts.md)) | [HouseBankAccounts](HouseBankAccounts.md) |  | Cuentas bancarias propias |
