# MessageDataColumn — Columnas de datos del mensaje

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `MessageDataColumn`
- **Descripción (ES):** Columnas de datos del mensaje
- **Description (EN):** Message Data Column

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ColumnName` | Edm.String | Yes | Column Name | Nombre de columna |
| 2 | `Link` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Link | Vínculo |
| 3 | `MessageDataLines` | Collection([MessageDataLine](../Tipos-Complejos/MessageDataLine.md)) | Yes | Message Data Lines | Líneas de datos del mensaje |

## Used by (properties)

- [Message](../Entidades/Messages.md).`MessageDataColumns`
