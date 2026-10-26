# QRCodeData — Datos del código QR

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `QRCodeData`
- **Descripción (ES):** Datos del código QR
- **Description (EN):** QR Code Data

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ObjectType` | Edm.Int32 | Yes | Object Type | Tipo de objeto |
| 2 | `ObjectAbsEntry` | Edm.String | Yes | Object Abs Entry | Entrada absoluta del objeto |
| 3 | `FieldName` | Edm.String | Yes | Field Name | Nombre del campo |
| 4 | `QRCodeText` | Edm.String | Yes | QR Code Text | Texto del código QR |

## Used by (service operations)

- [`QRCodeService_AddOrUpdateQRCode`](../Servicios/QRCodeService.md#qrcodeservice_addorupdateqrcode)
