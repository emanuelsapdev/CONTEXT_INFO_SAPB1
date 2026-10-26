# Attachments2 — Anexos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `Attachments2`
- **Descripción (ES):** Anexos
- **Entity type:** `Attachments2` (open type: accepts dynamic/UDF properties)
- **Key:** `AbsoluteEntry` (Edm.Int32)
- **DB tables (main / lines):** [OATC](../../Tablas%20SAP%20B1/OATC.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 2 · **Navigation properties:** 18 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/Attachments2?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/Attachments2/$count` | Contar |
| Get by key | `GET /b1s/v2/Attachments2(1)` | Obtener por clave |
| Create | `POST /b1s/v2/Attachments2` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/Attachments2(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/Attachments2(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/Attachments2(1)` (only if the B1 object allows removal) | Borrar |

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsoluteEntry` 🔑 | Edm.Int32 | No | Absolute Entry | Entrada absoluta (ID interno) |
| 2 | `Attachments2_Lines` | Collection([Attachments2_Line](../Tipos-Complejos/Attachments2_Line.md)) | Yes | Attachments 2 Lines | Líneas de anexos |

## Navigation properties (18)

Use `GET /b1s/v2/Attachments2(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ProductTrees` | Collection([ProductTree](../Entidades/ProductTrees.md)) | [ProductTrees](ProductTrees.md) |  | Listas de materiales (árbol de producto) |
| `ChecksforPayment` | Collection([ChecksforPayment](../Entidades/ChecksforPayment.md)) | [ChecksforPayment](ChecksforPayment.md) |  | Cheques para pago |
| `VendorPayments` | Collection([Payment](../Entidades/VendorPayments.md)) | [VendorPayments](VendorPayments.md) |  | Pagos efectuados |
| `CustomerEquipmentCards` | Collection([CustomerEquipmentCard](../Entidades/CustomerEquipmentCards.md)) | [CustomerEquipmentCards](CustomerEquipmentCards.md) |  | Tarjetas de equipo del cliente |
| `JournalEntries` | Collection([JournalEntry](../Entidades/JournalEntries.md)) | [JournalEntries](JournalEntries.md) |  | Asientos contables |
| `InventoryCountingDrafts` | Collection([InventoryCountingDraft](../Entidades/InventoryCountingDrafts.md)) | [InventoryCountingDrafts](InventoryCountingDrafts.md) |  | Borradores de recuento de inventario |
| `ServiceContracts` | Collection([ServiceContract](../Entidades/ServiceContracts.md)) | [ServiceContracts](ServiceContracts.md) |  | Contratos de servicio |
| `InventoryCountings` | Collection([InventoryCounting](../Entidades/InventoryCountings.md)) | [InventoryCountings](InventoryCountings.md) |  | Recuentos de inventario |
| `InventoryOpeningBalances` | Collection([InventoryOpeningBalance](../Entidades/InventoryOpeningBalances.md)) | [InventoryOpeningBalances](InventoryOpeningBalances.md) |  | Saldos iniciales de inventario |
| `InventoryPostings` | Collection([InventoryPosting](../Entidades/InventoryPostings.md)) | [InventoryPostings](InventoryPostings.md) |  | Contabilizaciones de inventario |
| `BlanketAgreements` | Collection([BlanketAgreement](../Entidades/BlanketAgreements.md)) | [BlanketAgreements](BlanketAgreements.md) |  | Acuerdos globales |
| `Campaigns` | Collection([Campaign](../Entidades/Campaigns.md)) | [Campaigns](Campaigns.md) |  | Campañas |
| `PaymentDrafts` | Collection([Payment](../Entidades/VendorPayments.md)) | [PaymentDrafts](PaymentDrafts.md) |  | Borradores de pagos |
| `ProductionOrders` | Collection([ProductionOrder](../Entidades/ProductionOrders.md)) | [ProductionOrders](ProductionOrders.md) |  | Órdenes de fabricación |
| `ProjectManagementTimeSheet` | Collection([PM_TimeSheetData](../Entidades/ProjectManagementTimeSheet.md)) | [ProjectManagementTimeSheet](ProjectManagementTimeSheet.md) |  | Hojas de horas de gestión de proyectos |
| `ProjectManagements` | Collection([PM_ProjectDocumentData](../Entidades/ProjectManagements.md)) | [ProjectManagements](ProjectManagements.md) |  | Gestión de proyectos |
| `IncomingPayments` | Collection([Payment](../Entidades/VendorPayments.md)) | [IncomingPayments](IncomingPayments.md) |  | Pagos recibidos |
| `Deposits` | Collection([Deposit](../Entidades/Deposits.md)) | [Deposits](Deposits.md) |  | Depósitos |
