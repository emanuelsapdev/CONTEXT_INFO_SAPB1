# ValueMappingService — Servicio de mapeo de valores

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `ValueMappingService`
- **Descripción (ES):** Servicio de mapeo de valores
- **Operations:** 3

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`ValueMappingService_GetMappedB1Value`](#valuemappingservice_getmappedb1value) | action | Collection([VM_B1ValuesData](../Entidades/ValueMapping.md)) | Get Mapped B 1 Value | Obtener valor de B1 mapeado |
| [`ValueMappingService_GetThirdPartyValuesForB1Value`](#valuemappingservice_getthirdpartyvaluesforb1value) | action | Collection([VM_ThirdPartyValuesData](../Tipos-Complejos/VM_ThirdPartyValuesData.md)) | Get Third Party Values For B 1 Value | Obtener valores de terceros para un valor de B1 |
| [`ValueMappingService_RemoveMappedValue`](#valuemappingservice_removemappedvalue) | action | — | Remove Mapped Value | Eliminar valor mapeado |

## ValueMappingService_GetMappedB1Value

- **Descripción (ES):** Obtener valor de B1 mapeado
- **Request:** `POST /b1s/v2/ValueMappingService_GetMappedB1Value`
- **Parameters:** `VM_B1ValuesData` ([VM_B1ValuesData](../Entidades/ValueMapping.md))
- **Returns:** Collection([VM_B1ValuesData](../Entidades/ValueMapping.md))

```json
{
  "VM_B1ValuesData": {
    "AbsEntry": 0,
    "ObjectId": 0,
    "ObjectAbsEntry": "string",
    ...
  }
}
```

## ValueMappingService_GetThirdPartyValuesForB1Value

- **Descripción (ES):** Obtener valores de terceros para un valor de B1
- **Request:** `POST /b1s/v2/ValueMappingService_GetThirdPartyValuesForB1Value`
- **Parameters:** `VM_B1ValuesData` ([VM_B1ValuesData](../Entidades/ValueMapping.md))
- **Returns:** Collection([VM_ThirdPartyValuesData](../Tipos-Complejos/VM_ThirdPartyValuesData.md))

```json
{
  "VM_B1ValuesData": {
    "AbsEntry": 0,
    "ObjectId": 0,
    "ObjectAbsEntry": "string",
    ...
  }
}
```

## ValueMappingService_RemoveMappedValue

- **Descripción (ES):** Eliminar valor mapeado
- **Request:** `POST /b1s/v2/ValueMappingService_RemoveMappedValue`
- **Parameters:** `VM_ThirdPartyValuesData` ([VM_ThirdPartyValuesData](../Tipos-Complejos/VM_ThirdPartyValuesData.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "VM_ThirdPartyValuesData": {
    "AbsEntry": 0,
    "LineId": 0,
    "ThirdPartySystemId": 0,
    "ThirdPartyValue": "string"
  }
}
```

