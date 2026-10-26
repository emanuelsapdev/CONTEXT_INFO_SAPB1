# VM_ThirdPartyValuesData — Valores de terceros (mapeo de valores)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `VM_ThirdPartyValuesData`
- **Descripción (ES):** Valores de terceros (mapeo de valores)
- **Description (EN):** VM Third Party Values Data

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `LineId` | Edm.Int32 | Yes | Line ID | ID de línea |
| 3 | `ThirdPartySystemId` | Edm.Int32 | Yes | Third Party System ID | ID del sistema de terceros |
| 4 | `ThirdPartyValue` | Edm.String | Yes | Third Party Value | Valor de terceros |

## Used by (properties)

- [VM_B1ValuesData](../Entidades/ValueMapping.md).`VM_ThirdPartyValuesCollection`

## Used by (service operations)

- [`ValueMappingService_GetThirdPartyValuesForB1Value`](../Servicios/ValueMappingService.md#valuemappingservice_getthirdpartyvaluesforb1value)
- [`ValueMappingService_RemoveMappedValue`](../Servicios/ValueMappingService.md#valuemappingservice_removemappedvalue)
