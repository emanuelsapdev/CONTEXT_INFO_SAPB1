# ResidenceNumberTypeEnum — Tipo de número de residencia

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ResidenceNumberTypeEnum`
- **Descripción (ES):** Tipo de número de residencia
- **Underlying type:** Edm.Int32
- **Members:** 6

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rntSpanishFiscalID` | 0 | Spanish Fiscal ID | NIF español |
| `rntVATRegistrationNumber` | 1 | VAT Registration Number | Número de registro de IVA |
| `rntPassport` | 2 | Passport | Pasaporte |
| `rntFiscalIDIssuedbytheResidenceCountry` | 3 | Fiscal ID Issuedbythe Residence Country | ID fiscal emitido por el país de residencia |
| `rntCertificateofFiscalResidence` | 4 | Certificateof Fiscal Residence | Certificado de residencia fiscal |
| `rntOtherDocument` | 5 | Other Document | Otro documento |

## Used by (2 properties)

- [BusinessPartner](../Entidades/BusinessPartners.md).`ResidenNumber`
- [JournalEntry](../Entidades/JournalEntries.md).`ResidenceNumberType`
