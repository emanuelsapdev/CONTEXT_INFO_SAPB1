# ElectronicDocumentEntryLogTypeEnum — Tipo de registro del documento electrónico

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ElectronicDocumentEntryLogTypeEnum`
- **Descripción (ES):** Tipo de registro del documento electrónico
- **Underlying type:** Edm.Int32
- **Members:** 10

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `edeltNone` | 0 | None | Ninguno |
| `edeltSend` | 1 | Send | Envío |
| `edeltReceive` | 2 | Receive | Recepción |
| `edeltImport` | 3 | Import | Importación |
| `edeltNote` | 4 | Note | Nota |
| `edeltWarning` | 5 | Warning | Advertencia |
| `edeltError` | 6 | Error | Error |
| `edeltWSData` | 7 | WS Data | Datos del servicio web |
| `edeltAuthorityProcessBegins` | 8 | Authority Process Begins | Inicia el proceso de la autoridad |
| `edeltAuthorityProcessFinished` | 9 | Authority Process Finished | Finaliza el proceso de la autoridad |

## Used by (3 properties)

- [EDFEntryAddLogInputParams](../Tipos-Complejos/EDFEntryAddLogInputParams.md).`LogType`
- [EDFEntryLog](../Tipos-Complejos/EDFEntryLog.md).`LogType`
- [EDFEntryLogInputParams](../Tipos-Complejos/EDFEntryLogInputParams.md).`LogType`
