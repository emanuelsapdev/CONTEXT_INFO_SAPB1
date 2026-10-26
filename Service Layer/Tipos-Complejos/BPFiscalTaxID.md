# BPFiscalTaxID — Identificación fiscal del socio de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BPFiscalTaxID`
- **Descripción (ES):** Identificación fiscal del socio de negocios
- **Description (EN):** Business Partner Fiscal Tax ID
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 20

## Properties (20)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Address` | Edm.String | Yes | Address | Dirección |
| 2 | `CNAECode` | Edm.Int32 | Yes | CNAE Code | Código CNAE |
| 3 | `TaxId0` | Edm.String | Yes | Tax ID 0 | ID fiscal 0 |
| 4 | `TaxId1` | Edm.String | Yes | Tax ID 1 | ID fiscal 1 |
| 5 | `TaxId2` | Edm.String | Yes | Tax ID 2 | ID fiscal 2 |
| 6 | `TaxId3` | Edm.String | Yes | Tax ID 3 | ID fiscal 3 |
| 7 | `TaxId4` | Edm.String | Yes | Tax ID 4 | ID fiscal 4 |
| 8 | `TaxId5` | Edm.String | Yes | Tax ID 5 | ID fiscal 5 |
| 9 | `TaxId6` | Edm.String | Yes | Tax ID 6 | ID fiscal 6 |
| 10 | `TaxId7` | Edm.String | Yes | Tax ID 7 | ID fiscal 7 |
| 11 | `TaxId8` | Edm.String | Yes | Tax ID 8 | ID fiscal 8 |
| 12 | `TaxId9` | Edm.String | Yes | Tax ID 9 | ID fiscal 9 |
| 13 | `TaxId10` | Edm.String | Yes | Tax ID 10 | ID fiscal 10 |
| 14 | `TaxId11` | Edm.String | Yes | Tax ID 11 | ID fiscal 11 |
| 15 | `BPCode` | Edm.String | Yes | Business Partner Code | Código del socio de negocios |
| 16 | `AddrType` | [BoAddressType](../Enums/BoAddressType.md) | Yes | Addr Type | Tipo de dirección |
| 17 | `TaxId12` | Edm.String | Yes | Tax ID 12 | ID fiscal 12 |
| 18 | `TaxId13` | Edm.String | Yes | Tax ID 13 | ID fiscal 13 |
| 19 | `AToRetrNFe` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | A To Retr N Fe | Autorización para recuperar NF-e |
| 20 | `TaxId14` | Edm.String | Yes | Tax ID 14 | ID fiscal 14 |

## Used by (properties)

- [BusinessPartner](../Entidades/BusinessPartners.md).`BPFiscalTaxIDCollection`
