# 3.8 SQL View Exposure (Microsoft SQL Server only)

> Source: *Working with SAP Business One Service Layer* v1.29, section 3.8 (paraphrased technical reference).
>
> **Resumen (ES):** exponer vistas SQL propias de la base de la sociedad (SQL Server) como servicio OData `view.svc`, consultarlas (clave, paginación, filtros, agregaciones) y autorizarlas.

Since **SAP Business One 10.0 PL02**, SL on **SQL Server** discovers regular customized SQL views and exposes them over OData v3/v4. (On HANA, the equivalent is the Semantic Layer — see [03-04](03-04-Semantic-Layer-Views.md).)

## 3.8.1 Create the view

Requirements for the view to be recognized:

| Requirement | Detail | Requisito (ES) |
|---|---|---|
| Schema | Must be in `dbo` | Esquema `dbo` |
| Name | Must end with **`B1SLQuery`** | Nombre terminado en `B1SLQuery` |
| Database | The company database | Base de la sociedad |

Example (SSMS, company DB `SBODEMOUS`):

```sql
USE [SBODEMOUS]
GO
CREATE VIEW [dbo].[B1_ItemPriceB1SLQuery] AS
  SELECT T0.[ItemCode], T0.[PriceList], T0.[UomEntry], T0.[Price], T0.[Currency], T0.[PriceType] FROM [dbo].[ITM1] T0
  UNION ALL
  SELECT T0.[ItemCode], T0.[PriceList], T0.[UomEntry], T0.[Price], T0.[Currency], T0.[PriceType] FROM [dbo].[ITM9] T0
GO
```

## 3.8.2 Expose / unexpose (entity `SQLViews`)

Views are **not exposed by default**. Use the bound actions of entity set `SQLViews` (no body):

| Action | Request | Acción (ES) |
|---|---|---|
| Expose one view | `POST /b1s/v1/SQLViews('B1_ItemPriceB1SLQuery')/Expose` → `204` | Exponer una vista |
| Unexpose one view | `POST /b1s/v1/SQLViews('B1_ItemPriceB1SLQuery')/Unexpose` | Dejar de exponer |
| Expose all | `POST /b1s/v1/SQLViews('*')/Expose` | Exponer todas |
| Unexpose all | `POST /b1s/v1/SQLViews('*')/Unexpose` | Dejar de exponer todas |
| View info | `GET /b1s/v1/SQLViews('B1_ItemPriceB1SLQuery')` → `{"Name": "...", "DBType": "MSSQL", "SchemaName": "dbo", "CreateDate": "2020-02-14"}` | Datos de la vista |

`SQLView` entity: key `Name`; properties `DBType`, `SchemaName`, `CreateDate`; bindable actions `Expose` / `Unexpose` (parameter `SQLViewParams` of type `SAPB1.SQLView`).

## 3.8.3 View service endpoint

| Purpose | OData v3 | OData v4 | Propósito (ES) |
|---|---|---|---|
| Service root | `GET /b1s/v1/view.svc` | `GET /b1s/v2/view.svc` | Raíz del servicio de vistas |
| Metadata | `GET /b1s/v1/view.svc/$metadata` | `GET /b1s/v2/view.svc/$metadata` | Metadatos |

Each view becomes an entity type with the view columns plus a virtual key **`id__`** (Edm.Int32); container name `B1SView`. Column types are mapped (e.g. `Price` → `Edm.Decimal` precision 19 scale 6).

## 3.8.4 Querying a view

| Query | Request | Notes | Consulta (ES) |
|---|---|---|---|
| By key | `GET /b1s/v1/view.svc/B1_ItemPriceB1SLQuery(1)` | Uses `row_number() OVER (order by getdate()) as [id__]` + `OFFSET/FETCH`; only for OData compliance, not a production pattern | Por clave virtual |
| By key with select | `.../B1_ItemPriceB1SLQuery(1)?$select=ItemCode,PriceList` | | Con selección |
| Paging | `GET .../B1_ItemPriceB1SLQuery` → 20 rows + `odata.nextLink: "B1_ItemPriceB1SLQuery?$skip=20"` | Paging is on by default; change with `Prefer: odata.maxpagesize=40` | Paginación |
| Query options | `.../B1_ItemPriceB1SLQuery?$select=ItemCode,PriceType&$filter=PriceType eq 'M'` | | Opciones de consulta |
| Count | `.../B1_ItemPriceB1SLQuery/$count` → `text/plain` number | | Conteo |
| Aggregate | `...?$apply=aggregate(ItemCode with max as MaxItemCode)` → `SELECT MAX(T0.[ItemCode]) AS 'MaxItemCode' ...` | | Agregación |
| Group + aggregate | `...?$apply=groupby((ItemCode, PriceType), aggregate($count as ItemCode_COUNT, Price with sum as SumPrice))&$orderby=ItemCode asc,PriceType asc` | | Agrupación |

`id__` has limitations; avoid complex queries that depend on it.

## 3.8.5 Authorization

- Normal users have no access by default: `403 Forbidden`, error code `804`, "No permission to access this view 'B1_ItemPriceB1SLQuery' for the current user."
- Grant: B1 client as superuser → **System Initialization > Authorizations** → change the view from *No Authorization* to *Full Authorization*.
- Superusers have full access to all exposed views.
- Permission changes may take ~1 minute (internal permission cache).
- **Unexposing a view resets its authorization to *No Authorization*.**
