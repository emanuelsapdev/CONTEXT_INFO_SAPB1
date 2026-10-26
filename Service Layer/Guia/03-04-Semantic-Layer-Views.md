# 3.7 SAP Business One Semantic Layer View Exposure (HANA only)

> Source: *Working with SAP Business One Service Layer* v1.29, section 3.7 (paraphrased technical reference).
>
> **Resumen (ES):** exponer y consultar como OData las vistas de cálculo del Semantic Layer de SAP HANA (vistas del sistema y personalizadas), autorizaciones, parámetros (placeholders), agregaciones y autenticación básica.

Applies to **SAP Business One, version for SAP HANA**, from 9.3 PL02. SL discovers the Semantic Layer views deployed with *SAP Business One analytics powered by SAP HANA* and exposes them as an OData service.

## 3.7.1 Deployment

| View category | How to deploy | Despliegue (ES) |
|---|---|---|
| System built-in (by SAP) | After installing Analytics Service: open the analytics home page (e.g. `https://dbserver:40000/Enablement/`) → **Company** tab → **Initialize**. Views appear in the *Content* package in SAP HANA Studio | Vistas del sistema: inicializar en la página de analytics |
| Customized | Package them with the SAP HANA Model Package Tool and deploy them from the B1 client (see 3.7.8) | Vistas personalizadas |

## 3.7.2 Exposure scope

- **Built-in views** are eligible only if they are **calculation views** and their name ends with **`Query`** (e.g. `SalesOrderDetailQuery`, `BalanceSheetQuery`).
- **Customized views** are eligible if they are calculation views.
- Eligible views are **not exposed by default**. To expose: B1 client → **SAP HANA Model Management** → tick **Service Layer Expose** → **restart Service Layer**.

## 3.7.3 OData version

The Semantic Layer service is exposed in **OData v4 by default**. To use OData v3, send header `OData-MaxVersion: 3.0` or `MaxDataServiceVersion: 3.0`.

## 3.7.4–3.7.5 Service root and metadata

| Item | URL | Elemento (ES) |
|---|---|---|
| Service root (list of views) | `GET /b1s/v1/sml.svc` | Raíz del servicio |
| Metadata | `GET /b1s/v1/sml.svc/$metadata` | Metadatos |

Root response: `{"@odata.context": ".../sml.svc/$metadata", "value": [ {"name": "PurchaseOrderFulfillmentCycleTimeQuery", "kind": "EntitySet", "url": "..."}, ... ]}`.

Modeling rules:

- Every view is exposed as an **entity** (OData only queries entities).
- Views have no DB key, so SL adds a **virtual key property `id__`** (Edm.Int32, generated with `row_number()`).
- Views **with placeholders** (input parameters, e.g. `BalanceSheetQuery` needs `$$P_FinancialPeriod$$` and `$$P_AddVoucher$$`) are split into two entity types:
  - `BalanceSheetQuery` — the data;
  - `BalanceSheetQueryParameter` (entity set `BalanceSheetQueryParameters`) — key = the parameters, with a navigation property to the data.

```xml
<EntityType Name="BalanceSheetQueryParameter">
  <Key><PropertyRef Name="P_FinancialPeriod"/><PropertyRef Name="P_AddVoucher"/></Key>
  <Property MaxLength="20" Name="P_FinancialPeriod" Nullable="false" Type="Edm.String"/>
  <Property DefaultValue="N" MaxLength="1" Name="P_AddVoucher" Nullable="false" Type="Edm.String"/>
  <NavigationProperty Name="BalanceSheetQuery" Partner="BalanceSheetQueryParameters" Type="Collection(SAPB1.BalanceSheetQuery)"/>
</EntityType>
<EntitySet EntityType="SAPB1.BalanceSheetQueryParameter" Name="BalanceSheetQueryParameters">
  <NavigationPropertyBinding Path="BalanceSheetQuery" Target="BalanceSheetQuery"/>
</EntitySet>
```

Query a placeholder view by navigating from its parameter entity:

```http
GET /b1s/v1/sml.svc/BalanceSheetQueryParameters(P_FinancialPeriod='2017',P_AddVoucher='N')/BalanceSheetQuery
```

Accessing `BalanceSheetQuery` or `BalanceSheetQueryParameters` directly without keys fails.

## 3.7.6 Authorization

- Normal users have **no access** to views by default → `401 Unauthorized`, `"No permission to access this view 'BalanceSheetQuery' for the current user 'user1'"`.
- Grant access: log in to the B1 client as superuser → **Administration > System Initialization > Authorizations > General Authorizations**.
- **Superusers** can access every exposed view.
- Changes take effect after the user logs off/on to the service, or after restarting SL.

## 3.7.7 Querying views

| Query | Request | Equivalent SQL / notes | Consulta (ES) |
|---|---|---|---|
| All records | `GET /b1s/v1/sml.svc/AveragePurchasingPriceQuery` | `SELECT *, row_number() over() as "id__" FROM "_SYS_BIC"."sap.SBODEMOUS.ap.case/AveragePurchasingPriceQuery"` | Todos los registros |
| With options | `...AveragePurchasingPriceQuery?$select=PostingYear,BusinessPartnerCode&$skip=1&$filter=PostingYear eq '2017' and startswith(BusinessPartnerCode,'1')&$orderby=PostingYear` | Standard options | Con opciones |
| By key | `...AveragePurchasingPriceQuery(1)` and `...(1)?$select=PostingYear,BusinessPartnerCode` | Uses `LIMIT 1 OFFSET n` | Por clave virtual |
| Parameter entity by key | `...BalanceSheetQueryParameters(P_FinancialPeriod='2017',P_AddVoucher='N')` | Without key → `400`, `"View parameters is not allowed to directly access."` | Entidad de parámetros |
| Placeholder view | `...BalanceSheetQueryParameters(...)/BalanceSheetQuery?$select=FiscalYear, AccountCode` | `SELECT ... FROM "_SYS_BIC"."...BalanceSheetQuery"('PLACEHOLDER'=('$$P_AddVoucher$$','N'),'PLACEHOLDER'=('$$P_FinancialPeriod$$','2017'))`; paging via `@odata.nextLink` | Vista con parámetros |
| Placeholder view by key | `...BalanceSheetQueryParameters(...)/BalanceSheetQuery(1)` | | Vista con parámetros por clave |
| Aggregation | `...AveragePurchasingPriceQuery?$apply=groupby((PostingYear, PostingMonth), aggregate($count as ItemCode_COUNT, AverageUnitPriceLC with sum as AverageUnitPriceLC_SUM))&$orderby=PostingYear asc,PostingMonth asc` | Similar to HANA Studio data preview (not fully equivalent) | Agregación |
| Count | `.../AveragePurchasingPriceQuery/$count`, `.../ItemRecommendationQueryParameters(CurrentUserCode=1)/ItemRecommendationQuery/$count` | Plain number (e.g. `14`) | Conteo |

`id__` has built-in limitations — don't rely on it for complex queries.

## 3.7.8 Customized views exposure

1. Export your models from SAP HANA Studio.
2. Build a model package with the latest **SAP HANA Model Package Tool** (SAP Note 2008991). The packaging wizard has an **Enable for Service Layer** column:
   - only enabled for calculation views; unchecked by default;
   - when checked, `SLEnable="Y"` is written to `Info.XML`, e.g. `<Model name="xxxx" type="CalculationView" menu="mymenu" IAEnable="N" SLEnable="Y" SLExpose="Y" />`;
   - `SLEnable="N"` or missing → view disabled in Model Management; old packages remain compatible.
3. In the B1 client open **SAP HANA Model Management**, import the package and **Deploy**.

Notes: a customized view **can't have the same name** as a built-in view (even in another package); authorizations apply as well; customized views are the recommended **alternative to DI API `Recordset`**, which is not exposed in SL for security/compatibility reasons.

## 3.7.9 Customized views query

Same capabilities as built-in views:

```http
GET https://dbserver:50000/b1s/v1/sml.svc/MyItem
GET https://dbserver:50000/b1s/v1/sml.svc/MyItem(2)
GET .../sml.svc/MyItem?$select=ItemGroup,ItemCode&$filter=ItemCode ne 'FA10004'&$orderby=ItemCode desc,ItemGroup
GET .../sml.svc/MyItem?$apply=aggregate(ItemCode with countdistinct as CountDistinctItemCode)
GET .../sml.svc/MyItem?$apply=filter(IsPurchaseItem eq 'N')/groupby((ItemGroup), aggregate(ItemCode with max as MaxItemCode))
```

## 3.7.10 Basic authentication (browser)

The Semantic Layer accepts HTTP **Basic authentication** from a browser. Because Basic auth has no field for the company DB, the **user name is a JSON string** combining user and company, e.g. `{"UserName":"manager","CompanyDB":"SBODEMOUS"}`, and the password is the B1 password. A session authenticated this way **can't be reused** for regular SL resources (BusinessPartners, Orders, …).
