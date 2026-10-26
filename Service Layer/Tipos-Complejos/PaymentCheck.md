# PaymentCheck — Cheques del pago

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PaymentCheck`
- **Descripción (ES):** Cheques del pago
- **Description (EN):** Payment Check
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 19

## Properties (19)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 2 | `DueDate` | Edm.DateTimeOffset | Yes | Due Date | Fecha de vencimiento |
| 3 | `CheckNumber` | Edm.Int32 | Yes | Check Number | Número de cheque |
| 4 | `BankCode` | Edm.String | Yes | Bank Code | Código del banco |
| 5 | `Branch` | Edm.String | Yes | Branch | Sucursal |
| 6 | `AccounttNum` | Edm.String | Yes | Accountt Number | Número de cuenta |
| 7 | `Details` | Edm.String | Yes | Details | Detalles |
| 8 | `Trnsfrable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Trnsfrable | Transferible |
| 9 | `CheckSum` | Edm.Double | Yes | Check Sum | Importe del cheque |
| 10 | `Currency` | Edm.String | Yes | Currency | Moneda |
| 11 | `CountryCode` | Edm.String | Yes | Country Code | Código de país |
| 12 | `CheckAbsEntry` | Edm.Int32 | Yes | Check Abs Entry | Entrada absoluta del cheque |
| 13 | `CheckAccount` | Edm.String | Yes | Check Account | Cuenta del cheque |
| 14 | `ManualCheck` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Manual Check | Cheque manual |
| 15 | `FiscalID` | Edm.String | Yes | Fiscal ID | ID fiscal |
| 16 | `OriginallyIssuedBy` | Edm.String | Yes | Originally Issued By | Emitido originalmente por |
| 17 | `Endorse` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Endorse | Endosar |
| 18 | `EndorsableCheckNo` | Edm.Int32 | Yes | Endorsable Check Number | N.º de cheque endosable |
| 19 | `ECheck` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | E Check | Cheque electrónico |

## Used by (properties)

- [Payment](../Entidades/VendorPayments.md).`PaymentChecks`
