# ServiceCallScheduling — Programaciones de la llamada de servicio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ServiceCallScheduling`
- **Descripción (ES):** Programaciones de la llamada de servicio
- **Description (EN):** Service Call Scheduling
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 48

## Properties (48)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 2 | `Technician` | Edm.Int32 | Yes | Technician | Técnico |
| 3 | `HandledBy` | Edm.Int32 | Yes | Handled By | Gestionado por |
| 4 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 5 | `StartTime` | Edm.TimeOfDay | Yes | Start Time | Hora de inicio |
| 6 | `EndDate` | Edm.DateTimeOffset | Yes | End Date | Fecha de fin |
| 7 | `EndTime` | Edm.TimeOfDay | Yes | End Time | Hora de fin |
| 8 | `Duration` | Edm.Double | Yes | Duration | Duración |
| 9 | `ActualDuration` | Edm.Double | Yes | Actual Duration | Duración real |
| 10 | `DurationType` | [BoDurations](../Enums/BoDurations.md) | Yes | Duration Type | Tipo de duración |
| 11 | `ActualDurationType` | [BoDurations](../Enums/BoDurations.md) | Yes | Actual Duration Type | Tipo de duración real |
| 12 | `Reminder` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Reminder | Recordatorio |
| 13 | `ReminderPeriod` | Edm.Double | Yes | Reminder Period | Período del recordatorio |
| 14 | `ReminderType` | [BoDurations](../Enums/BoDurations.md) | Yes | Reminder Type | Tipo de recordatorio |
| 15 | `ReminderSent` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Reminder Sent | Recordatorio enviado |
| 16 | `ReminderDate` | Edm.DateTimeOffset | Yes | Reminder Date | Fecha del recordatorio |
| 17 | `ReminderTime` | Edm.TimeOfDay | Yes | Reminder Time | Hora del recordatorio |
| 18 | `DisplayInCalendar` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Display In Calendar | Mostrar en calendario |
| 19 | `IsUnscheduled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Unscheduled | No programado |
| 20 | `Location` | Edm.Int32 | Yes | Location | Ubicación |
| 21 | `AddressName` | Edm.String | Yes | Address Name | Nombre de dirección |
| 22 | `AddressText` | Edm.String | Yes | Address Text | Texto de la dirección |
| 23 | `Street` | Edm.String | Yes | Street | Calle |
| 24 | `City` | Edm.String | Yes | City | Ciudad |
| 25 | `Room` | Edm.String | Yes | Room | Sala/oficina |
| 26 | `State` | Edm.String | Yes | State | Estado/provincia |
| 27 | `Country` | Edm.String | Yes | Country | País |
| 28 | `Address2` | Edm.String | Yes | Address 2 | Dirección 2 |
| 29 | `Address3` | Edm.String | Yes | Address 3 | Dirección 3 |
| 30 | `AddressType` | Edm.String | Yes | Address Type | Tipo de dirección |
| 31 | `StreetNo` | Edm.String | Yes | Street Number | Número de calle |
| 32 | `ZipCode` | Edm.String | Yes | Zip Code | Código postal |
| 33 | `Block` | Edm.String | Yes | Block | Barrio/bloque |
| 34 | `County` | Edm.String | Yes | County | Condado |
| 35 | `TaxOffice` | Edm.String | Yes | Tax Office | Oficina tributaria |
| 36 | `GlobalLocNum` | Edm.String | Yes | Global Loc Number | Número de localización global (GLN) |
| 37 | `IsClosed` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Closed | Está cerrado |
| 38 | `Remark` | Edm.String | Yes | Remark | Comentario |
| 39 | `AddressTypeBS` | [BoAddressType](../Enums/BoAddressType.md) | Yes | Address Type BS | Tipo de dirección (facturación/envío) |
| 40 | `SignatureName` | Edm.String | Yes | Signature Name | Nombre de la firma |
| 41 | `SalesOrders` | Edm.String | Yes | Sales Orders | Pedidos de cliente |
| 42 | `CheckInDate` | Edm.DateTimeOffset | Yes | Check In Date | Fecha de check-in |
| 43 | `CheckInTime` | Edm.TimeOfDay | Yes | Check In Time | Hora de check-in |
| 44 | `CheckInLocation` | Edm.String | Yes | Check In Location | Ubicación de check-in |
| 45 | `CheckInLatitude` | Edm.String | Yes | Check In Latitude | Latitud de check-in |
| 46 | `CheckInLongitude` | Edm.String | Yes | Check In Longitude | Longitud de check-in |
| 47 | `CheckOutDate` | Edm.DateTimeOffset | Yes | Check Out Date | Fecha de check-out |
| 48 | `CheckOutTime` | Edm.TimeOfDay | Yes | Check Out Time | Hora de check-out |

## Used by (properties)

- [ServiceCall](../Entidades/ServiceCalls.md).`ServiceCallSchedulings`
