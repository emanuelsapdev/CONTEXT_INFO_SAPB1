# SalesTaxCodes — Códigos del impuesto sobre ventas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `SalesTaxCodes`
- **Descripción (ES):** Códigos del impuesto sobre ventas
- **Entity type:** `SalesTaxCode` (open type: accepts dynamic/UDF properties)
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [OSTC](../../Tablas%20SAP%20B1/OSTC.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 11 · **Navigation properties:** 6 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/SalesTaxCodes?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/SalesTaxCodes/$count` | Contar |
| Get by key | `GET /b1s/v2/SalesTaxCodes('value')` | Obtener por clave |
| Create | `POST /b1s/v2/SalesTaxCodes` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/SalesTaxCodes('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/SalesTaxCodes('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/SalesTaxCodes('value')` (only if the B1 object allows removal) | Borrar |

## Properties (11)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ValidForAR` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Valid For AR | Válido para ventas |
| 2 | `ValidForAP` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Valid For AP | Válido para compras |
| 3 | `UserSignature` | Edm.Int32 | Yes | User Signature | Firma del usuario |
| 4 | `Rate` | Edm.Double | Yes | Rate | Tasa / tipo de cambio |
| 5 | `Name` | Edm.String | Yes | Name | Nombre |
| 6 | `Freight` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Freight | Flete |
| 7 | `Code` 🔑 | Edm.String | No | Code | Código |
| 8 | `IsItemLevel` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Item Level | Es a nivel de artículo |
| 9 | `Inactive` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Inactive | Inactivo |
| 10 | `FADebit` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | FA Debit | Debe de activo fijo |
| 11 | `SalesTaxCodes_Lines` | Collection([SalesTaxCodes_Line](../Tipos-Complejos/SalesTaxCodes_Line.md)) | Yes | Sales Tax Codes Lines | Líneas de códigos del impuesto sobre ventas |

## Navigation properties (6)

Use `GET /b1s/v2/SalesTaxCodes('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `UserDefaultGroups` | Collection([UserDefaultGroup](../Entidades/UserDefaultGroups.md)) | [UserDefaultGroups](UserDefaultGroups.md) |  | Grupos de valores predeterminados de usuario |
| `Warehouses` | Collection([Warehouse](../Entidades/Warehouses.md)) | [Warehouses](Warehouses.md) |  | Almacenes |
| `Items` | Collection([Item](../Entidades/Items.md)) | [Items](Items.md) |  | Artículos |
| `BusinessPartners` | Collection([BusinessPartner](../Entidades/BusinessPartners.md)) | [BusinessPartners](BusinessPartners.md) |  | Socios de negocios |
| `User` | [User](../Entidades/Users.md) | [Users](Users.md) | UserSignature → InternalKey | Usuario |
| `ExpenseTypes` | Collection([ExpenseTypeData](../Entidades/ExpenseTypes.md)) | [ExpenseTypes](ExpenseTypes.md) |  | Tipos de gastos |
