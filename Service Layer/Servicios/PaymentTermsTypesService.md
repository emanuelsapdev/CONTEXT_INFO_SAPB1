# PaymentTermsTypesService — Servicio de condiciones de pago

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `PaymentTermsTypesService`
- **Descripción (ES):** Servicio de condiciones de pago
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`PaymentTermsTypesService_UpdateWithBPs`](#paymenttermstypesservice_updatewithbps) | action | — | Update With B Ps | Actualizar con socios de negocios |

## PaymentTermsTypesService_UpdateWithBPs

- **Descripción (ES):** Actualizar con socios de negocios
- **Request:** `POST /b1s/v2/PaymentTermsTypesService_UpdateWithBPs`
- **Parameters:** `PaymentTermsType` ([PaymentTermsType](../Entidades/PaymentTermsTypes.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PaymentTermsType": {
    "GroupNumber": 0,
    "PaymentTermsGroupName": "string",
    "NumberOfAdditionalMonths": 0,
    "NumberOfAdditionalDays": 0,
    ...
  }
}
```

