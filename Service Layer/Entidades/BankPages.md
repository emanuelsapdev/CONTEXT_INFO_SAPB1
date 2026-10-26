# BankPages — Páginas de extracto bancario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BankPages`
- **Descripción (ES):** Páginas de extracto bancario
- **Entity type:** `BankPage` (open type: accepts dynamic/UDF properties)
- **Key:** `AccountCode` (Edm.String), `Sequence` (Edm.Int32)
- **DB tables (main / lines):** [OBNK](../../Tablas%20SAP%20B1/OBNK.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 22 · **Navigation properties:** 3 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BankPages?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BankPages/$count` | Contar |
| Get by key | `GET /b1s/v2/BankPages(AccountCode='value',Sequence=1)` | Obtener por clave |
| Create | `POST /b1s/v2/BankPages` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BankPages(AccountCode='value',Sequence=1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BankPages(AccountCode='value',Sequence=1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/BankPages(AccountCode='value',Sequence=1)` (only if the B1 object allows removal) | Borrar |

## Properties (22)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AccountCode` 🔑 | Edm.String | No | Account Code | Código de cuenta |
| 2 | `Sequence` 🔑 | Edm.Int32 | No | Sequence | Secuencia |
| 3 | `AccountName` | Edm.String | Yes | Account Name | Nombre de cuenta |
| 4 | `Reference` | Edm.String | Yes | Reference | Referencia |
| 5 | `DueDate` | Edm.DateTimeOffset | Yes | Due Date | Fecha de vencimiento |
| 6 | `Memo` | Edm.String | Yes | Memo | Comentario |
| 7 | `DebitAmount` | Edm.Double | Yes | Debit Amount | Importe del debe |
| 8 | `CreditAmount` | Edm.Double | Yes | Credit Amount | Importe del haber |
| 9 | `BankMatch` | Edm.Int32 | Yes | Bank Match | Conciliación bancaria |
| 10 | `DataSource` | Edm.String | Yes | Data Source | Origen de datos |
| 11 | `UserSignature` | Edm.Int32 | Yes | User Signature | Firma del usuario |
| 12 | `ExternalCode` | Edm.String | Yes | External Code | Código externo |
| 13 | `CardCode` | Edm.String | Yes | Card Code | Código del socio de negocios |
| 14 | `CardName` | Edm.String | Yes | Card Name | Nombre del socio de negocios |
| 15 | `StatementNumber` | Edm.Int32 | Yes | Statement Number | Número del extracto |
| 16 | `InvoiceNumber` | Edm.String | Yes | Invoice Number | Número de factura |
| 17 | `PaymentCreated` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Payment Created | Pago creado |
| 18 | `VisualOrder` | Edm.Int32 | Yes | Visual Order | Orden visual |
| 19 | `DocNumberType` | [BoBpsDocTypes](../Enums/BoBpsDocTypes.md) | Yes | Document Number Type | Tipo de numeración del documento |
| 20 | `PaymentReference` | Edm.String | Yes | Payment Reference | Referencia del pago |
| 21 | `InvoiceNumberEx` | Edm.String | Yes | Invoice Number Ex | Número de factura (ampliado) |
| 22 | `BICSwiftCode` | Edm.String | Yes | BIC Swift Code | Código BIC/SWIFT |

## Navigation properties (3)

Use `GET /b1s/v2/BankPages(AccountCode='value',Sequence=1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ChartOfAccount` | [ChartOfAccount](../Entidades/ChartOfAccounts.md) | [ChartOfAccounts](ChartOfAccounts.md) | AccountCode → Code | Plan de cuentas (cuentas de mayor) |
| `User` | [User](../Entidades/Users.md) | [Users](Users.md) | UserSignature → InternalKey | Usuario |
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | CardCode → CardCode | Socio de negocios |
