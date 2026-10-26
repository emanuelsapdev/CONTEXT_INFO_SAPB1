# AddressService — Servicio de direcciones

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `AddressService`
- **Descripción (ES):** Servicio de direcciones
- **Operations:** 2

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`AddressService_GetAddressFormat`](#addressservice_getaddressformat) | action | [AddressFormat](../Tipos-Complejos/AddressFormat.md) | Get Address Format | Obtener formato de dirección |
| [`AddressService_GetFullAddress`](#addressservice_getfulladdress) | action | [AddressReturnParams](../Tipos-Complejos/AddressReturnParams.md) | Get Full Address | Obtener dirección completa |

## AddressService_GetAddressFormat

- **Descripción (ES):** Obtener formato de dirección
- **Request:** `POST /b1s/v2/AddressService_GetAddressFormat`
- **Parameters:** `AddressFormatParams` ([AddressFormatParams](../Tipos-Complejos/AddressFormatParams.md))
- **Returns:** [AddressFormat](../Tipos-Complejos/AddressFormat.md)

```json
{
  "AddressFormatParams": {
    "Code": 0,
    "Name": "string"
  }
}
```

## AddressService_GetFullAddress

- **Descripción (ES):** Obtener dirección completa
- **Request:** `POST /b1s/v2/AddressService_GetFullAddress`
- **Parameters:** `AddressParams` ([AddressParams](../Tipos-Complejos/AddressParams.md))
- **Returns:** [AddressReturnParams](../Tipos-Complejos/AddressReturnParams.md)

```json
{
  "AddressParams": {
    "Country": "string",
    "State": "string",
    "County": "string",
    "ZipCode": "string",
    ...
  }
}
```

