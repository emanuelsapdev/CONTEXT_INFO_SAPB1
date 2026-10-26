# ElectronicDocProtocolCodeStrEnum — Código de protocolo electrónico (texto)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ElectronicDocProtocolCodeStrEnum`
- **Descripción (ES):** Código de protocolo electrónico (texto)
- **Underlying type:** Edm.Int32
- **Members:** 31

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `edpcs_Invalid` | 0 | Invalid | Inválido |
| `edpcs_GEN` | 1 | GEN | Genérico |
| `edpcs_EET` | 2 | EET | EET |
| `edpcs_CFDI` | 3 | CFDI | CFDI |
| `edpcs_FPA` | 4 | FPA | FPA |
| `edpcs_MTD` | 5 | MTD | MTD |
| `edpcs_EWB` | 6 | EWB | EWB |
| `edpcs_PEPPOL` | 7 | PEPPOL | PEPPOL |
| `edpcs_HOI` | 8 | HOI | HOI |
| `edpcs_MYF` | 9 | MYF | MYF |
| `edpcs_EIS` | 10 | EIS | EIS |
| `edpcs_IIS` | 11 | IIS | IIS |
| `edpcs_IIS_Annual` | 12 | IIS Annual | IIS anual |
| `edpcs_DIGIPOORT` | 13 | DIGIPOORT | DIGIPOORT |
| `edpcs_EBooks` | 14 | E Books | Libros electrónicos |
| `edpcs_DOX` | 15 | DOX | DOX |
| `edpcs_RTIE` | 16 | RTIE | RTIE |
| `edpcs_EBilling` | 17 | E Billing | Facturación electrónica |
| `edpcs_TaxService` | 18 | Tax Service | Servicio de impuestos |
| `edpcs_AFE` | 19 | AFE | AFE (factura electrónica Argentina) |
| `edpcs_DocSign` | 20 | Document Sign | Firma de documentos |
| `edpcs_KSeF` | 21 | K Se F | KSeF |
| `edpcs_GSTReturn` | 22 | GST Return | Declaración GST |
| `edpcs_PTDocSign` | 23 | PT Document Sign | Firma PT |
| `edpcs_SkatDK` | 24 | Skat DK | Skat DK |
| `edpcs_EII` | 25 | EII | EII |
| `edpcs_NFe` | 26 | N Fe | NF-e |
| `edpcs_PTeInvoicing` | 27 | P Te Invoicing | Facturación electrónica PT |
| `edpcs_PTeCom` | 28 | P Te Com | PT eCom |
| `edpcs_VeriFactu` | 29 | Veri Factu | VeriFactu |
| `edpcs_BAS` | 30 | BAS | BAS |

## Used by (19 properties)

- [EDFDocMappingInputParams](../Tipos-Complejos/EDFDocMappingInputParams.md).`Code`
- [EDFEntry](../Tipos-Complejos/EDFEntry.md).`Code`
- [EDFEntryAddLogInputParams](../Tipos-Complejos/EDFEntryAddLogInputParams.md).`Code`
- [EDFEntryInputParams](../Tipos-Complejos/EDFEntryInputParams.md).`Code`
- [EDFEntryListInputParams](../Tipos-Complejos/EDFEntryListInputParams.md).`Code`
- [EDFEntryLogInputParams](../Tipos-Complejos/EDFEntryLogInputParams.md).`Code`
- [EDFImportEntry](../Tipos-Complejos/EDFImportEntry.md).`Code`
- [EDFProtocol](../Entidades/ElectronicDocuments.md).`Code`
- [EDFProtocolInputParams](../Tipos-Complejos/EDFProtocolInputParams.md).`Code`
- [EDFProtocolParameter](../Tipos-Complejos/EDFProtocolParameter.md).`Code`
- [EDFProtocolParameterInputParams](../Tipos-Complejos/EDFProtocolParameterInputParams.md).`Code`
- [EDFProtocolWithParameters](../Tipos-Complejos/EDFProtocolWithParameters.md).`Code`
- [ExportDetermination](../Entidades/ExportDeterminations.md).`Code`
- [ExportDeterminationParams](../Tipos-Complejos/ExportDeterminationParams.md).`Code`
- [ExportDeterminationsParams](../Tipos-Complejos/ExportDeterminationsParams.md).`Code`
- [ImportDetermination](../Entidades/ImportDeterminations.md).`Code`
- [ImportDeterminationParams](../Tipos-Complejos/ImportDeterminationParams.md).`Code`
- [ImportDeterminationsParams](../Tipos-Complejos/ImportDeterminationsParams.md).`Code`
- [MailElectronicDocumentParam](../Tipos-Complejos/MailElectronicDocumentParam.md).`ProtocolCode`
