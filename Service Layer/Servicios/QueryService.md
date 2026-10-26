# QueryService — Servicio de consultas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `QueryService`
- **Descripción (ES):** Servicio de consultas
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`QueryService_PostQuery`](#queryservice_postquery) | action | Edm.String | Post Query | Ejecutar consulta |

## QueryService_PostQuery

- **Descripción (ES):** Ejecutar consulta
- **Request:** `POST /b1s/v2/QueryService_PostQuery`
- **Parameters:** `QueryPath` (Edm.String), `QueryOption` (Edm.String)
- **Returns:** Edm.String

```json
{
  "QueryPath": "string",
  "QueryOption": "string"
}
```

