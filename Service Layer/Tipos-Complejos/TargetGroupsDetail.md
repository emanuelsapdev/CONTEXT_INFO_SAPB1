# TargetGroupsDetail — Detalles de grupos objetivo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `TargetGroupsDetail`
- **Descripción (ES):** Detalles de grupos objetivo
- **Description (EN):** Target Groups Detail

- **Properties:** 22

## Properties (22)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TargetGroupCode` | Edm.String | Yes | Target Group Code | Código de grupo objetivo |
| 2 | `BusinessPartnerCode` | Edm.String | Yes | Business Partner Code | Código del socio de negocios |
| 3 | `BusinessPartnerName` | Edm.String | Yes | Business Partner Name | Nombre del socio de negocios |
| 4 | `GroupCode` | Edm.String | Yes | Group Code | Código de grupo |
| 5 | `Industry` | Edm.String | Yes | Industry | Ramo (industria) |
| 6 | `ActiveStatus` | [TargetGroupsDetailStatusEnum](../Enums/TargetGroupsDetailStatusEnum.md) | Yes | Active Status | Estado activo |
| 7 | `ContactPerson` | Edm.String | Yes | Contact Person | Persona de contacto |
| 8 | `Title` | Edm.String | Yes | Title | Título |
| 9 | `Position` | Edm.String | Yes | Position | Posición/cargo |
| 10 | `E_Mail` | Edm.String | Yes | E Mail | Correo electrónico |
| 11 | `Telephone` | Edm.String | Yes | Telephone | Teléfono |
| 12 | `MobilePhone` | Edm.String | Yes | Mobile Phone | Teléfono celular |
| 13 | `Fax` | Edm.String | Yes | Fax | Fax |
| 14 | `Address` | Edm.String | Yes | Address | Dirección |
| 15 | `Street` | Edm.String | Yes | Street | Calle |
| 16 | `Block` | Edm.String | Yes | Block | Barrio/bloque |
| 17 | `City` | Edm.String | Yes | City | Ciudad |
| 18 | `ZipCode` | Edm.String | Yes | Zip Code | Código postal |
| 19 | `County` | Edm.String | Yes | County | Condado |
| 20 | `State` | Edm.String | Yes | State | Estado/provincia |
| 21 | `Country` | Edm.String | Yes | Country | País |
| 22 | `Building` | Edm.String | Yes | Building | Edificio |

## Used by (properties)

- [TargetGroup](../Entidades/TargetGroups.md).`TargetGroupsDetails`
