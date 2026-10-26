# BPBankAccount — Cuenta bancaria del socio de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BPBankAccount`
- **Descripción (ES):** Cuenta bancaria del socio de negocios
- **Description (EN):** Business Partner Bank Account
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 34

## Properties (34)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LogInstance` | Edm.Int32 | Yes | Log Instance | Instancia de registro (historial) |
| 2 | `UserNo4` | Edm.String | Yes | User Number 4 | N.º de usuario 4 |
| 3 | `BPCode` | Edm.String | Yes | Business Partner Code | Código del socio de negocios |
| 4 | `County` | Edm.String | Yes | County | Condado |
| 5 | `State` | Edm.String | Yes | State | Estado/provincia |
| 6 | `UserNo2` | Edm.String | Yes | User Number 2 | N.º de usuario 2 |
| 7 | `IBAN` | Edm.String | Yes | IBAN | IBAN |
| 8 | `ZipCode` | Edm.String | Yes | Zip Code | Código postal |
| 9 | `City` | Edm.String | Yes | City | Ciudad |
| 10 | `Block` | Edm.String | Yes | Block | Barrio/bloque |
| 11 | `Branch` | Edm.String | Yes | Branch | Sucursal |
| 12 | `Country` | Edm.String | Yes | Country | País |
| 13 | `Street` | Edm.String | Yes | Street | Calle |
| 14 | `ControlKey` | Edm.String | Yes | Control Key | Clave de control |
| 15 | `UserNo3` | Edm.String | Yes | User Number 3 | N.º de usuario 3 |
| 16 | `BankCode` | Edm.String | Yes | Bank Code | Código del banco |
| 17 | `AccountNo` | Edm.String | Yes | Account Number | Número de cuenta |
| 18 | `UserNo1` | Edm.String | Yes | User Number 1 | N.º de usuario 1 |
| 19 | `InternalKey` | Edm.Int32 | Yes | Internal Key | Clave interna |
| 20 | `BuildingFloorRoom` | Edm.String | Yes | Building Floor Room | Edificio/piso/oficina |
| 21 | `BIK` | Edm.String | Yes | BIK | Código BIK |
| 22 | `AccountName` | Edm.String | Yes | Account Name | Nombre de cuenta |
| 23 | `CorrespondentAccount` | Edm.String | Yes | Correspondent Account | Cuenta corresponsal |
| 24 | `Phone` | Edm.String | Yes | Phone | Teléfono |
| 25 | `Fax` | Edm.String | Yes | Fax | Fax |
| 26 | `CustomerIdNumber` | Edm.String | Yes | Customer ID Number | Número de identificación del cliente |
| 27 | `ISRBillerID` | Edm.String | Yes | ISR Biller ID | ID de facturador ISR |
| 28 | `ISRType` | Edm.Int32 | Yes | ISR Type | Tipo ISR |
| 29 | `BICSwiftCode` | Edm.String | Yes | BIC Swift Code | Código BIC/SWIFT |
| 30 | `ABARoutingNumber` | Edm.String | Yes | ABA Routing Number | Número de ruta ABA |
| 31 | `MandateID` | Edm.String | Yes | Mandate ID | ID de mandato (SEPA) |
| 32 | `SignatureDate` | Edm.DateTimeOffset | Yes | Signature Date | Fecha de firma |
| 33 | `MandateExpDate` | Edm.DateTimeOffset | Yes | Mandate Exp Date | Fecha de vencimiento del mandato |
| 34 | `SEPASeqType` | [SEPASequenceTypeEnum](../Enums/SEPASequenceTypeEnum.md) | Yes | SEPA Seq Type | Tipo de secuencia SEPA |

## Used by (properties)

- [BusinessPartner](../Entidades/BusinessPartners.md).`BPBankAccounts`
