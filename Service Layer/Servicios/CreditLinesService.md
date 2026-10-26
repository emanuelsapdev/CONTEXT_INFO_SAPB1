# CreditLinesService — Servicio de líneas de tarjetas de crédito

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `CreditLinesService`
- **Descripción (ES):** Servicio de líneas de tarjetas de crédito
- **Operations:** 2

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`CreditLinesService_GetCreditLine`](#creditlinesservice_getcreditline) | action | [CreditLine](../Tipos-Complejos/CreditLine.md) | Get Credit Line | Obtener línea de tarjeta de crédito |
| [`CreditLinesService_GetValidCreditLineList`](#creditlinesservice_getvalidcreditlinelist) | action | Collection([CreditLineParams](../Tipos-Complejos/CreditLineParams.md)) | Get Valid Credit Line List | Obtener lista de líneas de tarjeta válidas |

## CreditLinesService_GetCreditLine

- **Descripción (ES):** Obtener línea de tarjeta de crédito
- **Request:** `POST /b1s/v2/CreditLinesService_GetCreditLine`
- **Parameters:** `CreditLineParams` ([CreditLineParams](../Tipos-Complejos/CreditLineParams.md))
- **Returns:** [CreditLine](../Tipos-Complejos/CreditLine.md)

```json
{
  "CreditLineParams": {
    "AbsId": 0
  }
}
```

## CreditLinesService_GetValidCreditLineList

- **Descripción (ES):** Obtener lista de líneas de tarjeta válidas
- **Request:** `POST /b1s/v2/CreditLinesService_GetValidCreditLineList`
- **Parameters:** none
- **Returns:** Collection([CreditLineParams](../Tipos-Complejos/CreditLineParams.md))

