# BusinessPartnersService — Servicio de socios de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `BusinessPartnersService`
- **Descripción (ES):** Servicio de socios de negocios
- **Operations:** 2

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`BusinessPartnersService_CreateOpenBalance`](#businesspartnersservice_createopenbalance) | action | — | Create Open Balance | Crear saldo inicial |
| [`BusinessPartnersService_InitData`](#businesspartnersservice_initdata) | action | [BusinessPartner](../Entidades/BusinessPartners.md) | Init Data | Inicializar datos |

## BusinessPartnersService_CreateOpenBalance

- **Descripción (ES):** Crear saldo inicial
- **Request:** `POST /b1s/v2/BusinessPartnersService_CreateOpenBalance`
- **Parameters:** `OpenningBalanceAccount` ([OpenningBalanceAccount](../Tipos-Complejos/OpenningBalanceAccount.md)), `BPCodes` (Collection([BPCode](../Tipos-Complejos/BPCode.md)))
- **Returns:** nothing (`204 No Content`)

```json
{
  "OpenningBalanceAccount": {
    "OpenBalanceAccount": "string",
    "Date": "2026-01-31",
    "Ref1": "string",
    "Ref2": "string",
    ...
  },
  "BPCodes": [ {
    "Code": "string",
    "DueDate": "2026-01-31",
    "Debit": 0.0,
    "Credit": 0.0,
    ...
  } ]
}
```

## BusinessPartnersService_InitData

- **Descripción (ES):** Inicializar datos
- **Request:** `POST /b1s/v2/BusinessPartnersService_InitData`
- **Parameters:** none
- **Returns:** [BusinessPartner](../Entidades/BusinessPartners.md)

