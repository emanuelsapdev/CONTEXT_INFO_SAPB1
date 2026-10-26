# Global — Operaciones globales (sin servicio)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `Global`
- **Descripción (ES):** Operaciones globales (sin servicio)
- **Operations:** 2

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`Login`](#login) | action | [B1Session](../Entidades/B1Sessions.md) | Login | Iniciar sesión |
| [`Logout`](#logout) | action | — | Logout | Cerrar sesión |

## Login

- **Descripción (ES):** Iniciar sesión
- **Request:** `POST /b1s/v2/Login`
- **Parameters:** `CompanyDB` (Edm.String), `UserName` (Edm.String), `Password` (Edm.String), `Language` (Edm.String)
- **Returns:** [B1Session](../Entidades/B1Sessions.md)

```json
{
  "CompanyDB": "string",
  "UserName": "string",
  "Password": "string",
  "Language": "string"
}
```

## Logout

- **Descripción (ES):** Cerrar sesión
- **Request:** `POST /b1s/v2/Logout`
- **Parameters:** none
- **Returns:** nothing (`204 No Content`)

