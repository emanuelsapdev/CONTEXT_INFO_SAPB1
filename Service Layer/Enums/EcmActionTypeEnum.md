# EcmActionTypeEnum — Tipo de acción ECM

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `EcmActionTypeEnum`
- **Descripción (ES):** Tipo de acción ECM
- **Underlying type:** Edm.Int32
- **Members:** 16

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `latNone` | 0 | None | Ninguno |
| `latSetup` | 1 | Setup | Configuración |
| `latReport` | 2 | Report | Informe |
| `latDocumentAR` | 3 | Document AR | Documento de ventas |
| `latDocumentAP` | 4 | Document AP | Documento de compras |
| `latDraft` | 5 | Draft | Borrador |
| `latOther` | 6 | Other | Otro |
| `latSkip` | 7 | Skip | Omitir |
| `latContingency` | 8 | Contingency | Contingencia |
| `latBpCheck` | 9 | Bp Check | Verificación de socio de negocios |
| `latPaymentIncoming` | 10 | Payment Incoming | Pago recibido |
| `latPaymentOutgoing` | 11 | Payment Outgoing | Pago efectuado |
| `latReconciliation` | 12 | Reconciliation | Conciliación |
| `latDraftAP` | 13 | Draft AP | Borrador de compras |
| `latTransportation` | 14 | Transportation | Transporte |
| `latInvTransfer` | 15 | Inv Transfer | Transferencia de stock |

## Used by (1 properties)

- [EcmAction](../Tipos-Complejos/EcmAction.md).`Type`
