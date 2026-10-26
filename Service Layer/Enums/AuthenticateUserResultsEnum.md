# AuthenticateUserResultsEnum — Resultado de autenticación de usuario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `AuthenticateUserResultsEnum`
- **Descripción (ES):** Resultado de autenticación de usuario
- **Underlying type:** Edm.Int32
- **Members:** 8

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `aturNoUserConnectedToCompany` | 0 | Number User Connected To Company | Ningún usuario conectado a la sociedad |
| `aturUsernamePasswordMatched` | 1 | Username Password Matched | Usuario y contraseña correctos |
| `aturLogOnUserNotAdmin` | 2 | Log On User Not Admin | El usuario conectado no es administrador |
| `aturBadUserOrPassword` | 3 | Bad User Or Password | Usuario o contraseña incorrectos |
| `aturUserHasBeenLocked` | 4 | User Has Been Locked | Usuario bloqueado |
| `aturPasswordExpired` | 5 | Password Expired | Contraseña vencida |
| `aturDBErrors` | 6 | DB Errors | Errores de base de datos |
| `aturWrongDomainName` | 7 | Wrong Domain Name | Nombre de dominio incorrecto |
