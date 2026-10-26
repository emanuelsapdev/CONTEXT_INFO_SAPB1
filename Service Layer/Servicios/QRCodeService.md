# QRCodeService — Servicio de códigos QR

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `QRCodeService`
- **Descripción (ES):** Servicio de códigos QR
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`QRCodeService_AddOrUpdateQRCode`](#qrcodeservice_addorupdateqrcode) | action | — | Add Or Update QR Code | Agregar o actualizar código QR |

## QRCodeService_AddOrUpdateQRCode

- **Descripción (ES):** Agregar o actualizar código QR
- **Request:** `POST /b1s/v2/QRCodeService_AddOrUpdateQRCode`
- **Parameters:** `QRCodeData` ([QRCodeData](../Tipos-Complejos/QRCodeData.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "QRCodeData": {
    "ObjectType": 0,
    "ObjectAbsEntry": "string",
    "FieldName": "string",
    "QRCodeText": "string"
  }
}
```

