# RetornoCodeParams — Parámetros de códigos de retorno

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `RetornoCodeParams`
- **Descripción (ES):** Parámetros de códigos de retorno
- **Description (EN):** Retorno Code Parameters

- **Properties:** 8

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `OccurenceCode` | Edm.Int32 | Yes | Occurence Code | Código de ocurrencia |
| 3 | `MovementCode` | Edm.Int32 | Yes | Movement Code | Código de movimiento |
| 4 | `BoeStatus` | [BoBoeStatus](../Enums/BoBoeStatus.md) | Yes | Boe Status | Estado de letra de cambio |
| 5 | `Description` | Edm.String | Yes | Description | Descripción |
| 6 | `Color` | Edm.Int32 | Yes | Color | Color |
| 7 | `FileFormat` | Edm.String | Yes | File Format | Formato de archivo |
| 8 | `BankCode` | Edm.String | Yes | Bank Code | Código del banco |

## Used by (service operations)

- [`RetornoCodesService_GetList`](../Servicios/RetornoCodesService.md#retornocodesservice_getlist)
