# EWBTransporter_Line — Líneas de transportista EWB

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EWBTransporter_Line`
- **Descripción (ES):** Líneas de transportista EWB
- **Description (EN):** EWB Transporter Line

- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `Mode` | Edm.Int32 | Yes | Mode | Modo |
| 4 | `VehicleType` | Edm.String | Yes | Vehicle Type | Tipo de vehículo |
| 5 | `VehicleNo` | Edm.String | Yes | Vehicle Number | Número de vehículo |

## Used by (properties)

- [EWBTransporter](../Entidades/EWBTransporters.md).`EWBTransporter_Lines`
