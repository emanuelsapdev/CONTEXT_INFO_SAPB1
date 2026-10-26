# ElectronicDocProcessingTargetEnum — Destino de procesamiento del documento electrónico

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ElectronicDocProcessingTargetEnum`
- **Descripción (ES):** Destino de procesamiento del documento electrónico
- **Underlying type:** Edm.Int32
- **Members:** 32

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `edpt_Invalid` | -1 | Invalid | Inválido |
| `edpt_All` | 0 | All | Todos |
| `edpt_None` | 1 | None | Ninguno |
| `edpt_LegacyB1iSender` | 2 | Legacy B 1i Sender | Emisor B1i heredado |
| `edpt_B1iEventSender` | 3 | B 1i Event Sender | Emisor de eventos B1i |
| `edpt_LegacyXMLFile` | 4 | Legacy XML File | Archivo XML heredado |
| `edpt_ConnectorXML` | 5 | Connector XML | Conector XML |
| `edpt_ConnectorB1iWS` | 6 | Connector B 1i WS | Conector servicio web B1i |
| `edpt_ConnectorPEPPOL` | 7 | Connector PEPPOL | Conector PEPPOL |
| `edpt_ConnectorEET` | 8 | Connector EET | Conector EET |
| `edpt_ConnectorEETv2` | 9 | Connector EE Tv 2 | Conector EET v2 |
| `edpt_ConnectorCFDi` | 10 | Connector CF Di | Conector CFDi |
| `edpt_ConnectorEBooks` | 11 | Connector E Books | Conector de libros electrónicos |
| `edpt_ConnectorDOX` | 12 | Connector DOX | Conector DOX |
| `edpt_ConnectorDigipoort` | 13 | Connector Digipoort | Conector Digipoort |
| `edpt_ImportWizardManualFile` | 14 | Import Wizard Manual File | Asistente de importación: archivo manual |
| `edpt_ImportWizardAutomaticFile` | 15 | Import Wizard Automatic File | Asistente de importación: archivo automático |
| `edpt_ImportWizardWebService` | 16 | Import Wizard Web Service | Asistente de importación: servicio web |
| `edpt_ConnectorFPA` | 17 | Connector FPA | Conector FPA |
| `edpt_ConnectorDocSign` | 18 | Connector Document Sign | Conector de firma de documentos |
| `edpt_ConnectorAFE` | 19 | Connector AFE | Conector AFE (Argentina) |
| `edpt_ConnectorGSTReturn` | 20 | Connector GST Return | Conector de declaración GST |
| `edpt_ConnectorKSeF` | 21 | Connector K Se F | Conector KSeF |
| `edpt_ConnectorPTDocSign` | 22 | Connector PT Document Sign | Conector de firma PT |
| `edpt_ConnectorSkatDK` | 23 | Connector Skat DK | Conector Skat DK |
| `edpt_ConnectorEII` | 24 | Connector EII | Conector EII |
| `edpt_ConnectorPTeInvoicing` | 25 | Connector P Te Invoicing | Conector facturación electrónica PT |
| `edpt_ConnectorEBilling` | 26 | Connector E Billing | Conector de facturación electrónica |
| `edpt_ConnectorEDSHOI` | 27 | Connector EDSHOI | Conector EDS HOI |
| `edpt_ConnectorPTeCom` | 28 | Connector P Te Com | Conector PT eCom |
| `edpt_ConnectorVeriFactu` | 29 | Connector Veri Factu | Conector VeriFactu |
| `edpt_ManualImport` | 30 | Manual Import | Importación manual |

## Used by (1 properties)

- [EDFEntryListInputParams](../Tipos-Complejos/EDFEntryListInputParams.md).`ProcessingTarget`
