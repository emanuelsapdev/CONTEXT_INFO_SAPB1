# WarehouseLocations — Ubicaciones de almacenes

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `WarehouseLocations`
- **Descripción (ES):** Ubicaciones de almacenes
- **Entity type:** `WarehouseLocation` (open type: accepts dynamic/UDF properties)
- **Key:** `Code` (Edm.Int32)
- **DB tables (main / lines):** [OLCT](../../Tablas%20SAP%20B1/OLCT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 32 · **Navigation properties:** 9 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/WarehouseLocations?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/WarehouseLocations/$count` | Contar |
| Get by key | `GET /b1s/v2/WarehouseLocations(1)` | Obtener por clave |
| Create | `POST /b1s/v2/WarehouseLocations` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/WarehouseLocations(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/WarehouseLocations(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/WarehouseLocations(1)` (only if the B1 object allows removal) | Borrar |

## Properties (32)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.Int32 | No | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `LSTVATNumber` | Edm.String | Yes | LSTVAT Number | Número de IVA LST (India) |
| 4 | `CSTNumber` | Edm.String | Yes | CST Number | Número CST |
| 5 | `ExemptionNumber` | Edm.String | Yes | Exemption Number | Número de exención |
| 6 | `TANNumber` | Edm.String | Yes | TAN Number | Número TAN (India) |
| 7 | `ServiceTaxNumber` | Edm.String | Yes | Service Tax Number | Número de impuesto de servicios |
| 8 | `AssesseeType` | Edm.String | Yes | Assessee Type | Tipo de contribuyente |
| 9 | `CompanyType` | Edm.String | Yes | Company Type | Tipo de sociedad |
| 10 | `NatureOfBusiness` | Edm.String | Yes | Nature Of Business | Naturaleza del negocio |
| 11 | `TINNumber` | Edm.String | Yes | TIN Number | Número TIN |
| 12 | `RegistrationType` | Edm.String | Yes | Registration Type | Tipo de registro |
| 13 | `EccNumber` | Edm.String | Yes | Ecc Number | Número ECC |
| 14 | `CERange` | Edm.String | Yes | CE Range | Rango de impuestos especiales (India) |
| 15 | `CEDivision` | Edm.String | Yes | CE Division | División de impuestos especiales (India) |
| 16 | `CECommissionerate` | Edm.String | Yes | CE Commissionerate | Comisionado de impuestos especiales (India) |
| 17 | `ManufacturerCode` | Edm.String | Yes | Manufacturer Code | Código de fabricante |
| 18 | `Jurisdiction` | Edm.String | Yes | Jurisdiction | Jurisdicción |
| 19 | `Street` | Edm.String | Yes | Street | Calle |
| 20 | `Block` | Edm.String | Yes | Block | Barrio/bloque |
| 21 | `ZipCode` | Edm.String | Yes | Zip Code | Código postal |
| 22 | `City` | Edm.String | Yes | City | Ciudad |
| 23 | `County` | Edm.String | Yes | County | Condado |
| 24 | `Country` | Edm.String | Yes | Country | País |
| 25 | `State` | Edm.String | Yes | State | Estado/provincia |
| 26 | `PANNumber` | Edm.String | Yes | PAN Number | Número PAN (India) |
| 27 | `CERegisterNumber` | Edm.String | Yes | CE Register Number | Número de registro de impuestos especiales (India) |
| 28 | `BuildingFloorRoom` | Edm.String | Yes | Building Floor Room | Edificio/piso/oficina |
| 29 | `GSTIN` | Edm.String | Yes | GSTIN | GSTIN (India) |
| 30 | `GstType` | [BoGSTRegnTypeEnum](../Enums/BoGSTRegnTypeEnum.md) | Yes | Gst Type | Tipo de GST |
| 31 | `GSTTDS` | Edm.String | Yes | GSTTDS | GST TDS |
| 32 | `GSTISD` | Edm.String | Yes | GSTISD | GST ISD |

## Navigation properties (9)

Use `GET /b1s/v2/WarehouseLocations(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Warehouses` | Collection([Warehouse](../Entidades/Warehouses.md)) | [Warehouses](Warehouses.md) |  | Almacenes |
| `VendorPayments` | Collection([Payment](../Entidades/VendorPayments.md)) | [VendorPayments](VendorPayments.md) |  | Pagos efectuados |
| `WithholdingTaxCodes` | Collection([WithholdingTaxCode](../Entidades/WithholdingTaxCodes.md)) | [WithholdingTaxCodes](WithholdingTaxCodes.md) |  | Códigos de retención de impuestos |
| `JournalEntries` | Collection([JournalEntry](../Entidades/JournalEntries.md)) | [JournalEntries](JournalEntries.md) |  | Asientos contables |
| `Country2` | [Country](../Entidades/Countries.md) | [Countries](Countries.md) | Country → Code | Países/Regiones |
| `Items` | Collection([Item](../Entidades/Items.md)) | [Items](Items.md) |  | Artículos |
| `CertificateSeries` | Collection([CertificateSeries](../Entidades/CertificateSeries.md)) | [CertificateSeries](CertificateSeries.md) |  | Series de certificados |
| `PaymentDrafts` | Collection([Payment](../Entidades/VendorPayments.md)) | [PaymentDrafts](PaymentDrafts.md) |  | Borradores de pagos |
| `IncomingPayments` | Collection([Payment](../Entidades/VendorPayments.md)) | [IncomingPayments](IncomingPayments.md) |  | Pagos recibidos |
