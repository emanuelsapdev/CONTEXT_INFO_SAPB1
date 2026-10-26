# IntrastatConfigurationEnum — Configuración de Intrastat

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `IntrastatConfigurationEnum`
- **Descripción (ES):** Configuración de Intrastat
- **Underlying type:** Edm.Int32
- **Members:** 10

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `enAdditionalMeasureUnit` | 0 | Additional Measure Unit | Unidad de medida adicional |
| `enCommodityCodes` | 1 | Commodity Codes | Códigos de mercancía |
| `enCustomProcedures` | 2 | Custom Procedures | Procedimientos aduaneros |
| `enIncoterms` | 3 | Incoterms | Incoterms |
| `enNatureOfTransactions` | 4 | Nature Of Transactions | Naturaleza de las transacciones |
| `enPortsOfEntryAndExit` | 5 | Ports Of Entry And Exit | Puertos de entrada y salida |
| `enServiceCodes` | 6 | Service Codes | Códigos de servicio |
| `enStatisticalProcedures` | 7 | Statistical Procedures | Procedimientos estadísticos |
| `enTransportModes` | 8 | Transport Modes | Modos de transporte |
| `enRegions` | 9 | Regions | Regiones |

## Used by (2 properties)

- [IntrastatConfiguration](../Entidades/IntrastatConfiguration.md).`ConfType`
- [IntrastatConfigurationParams](../Tipos-Complejos/IntrastatConfigurationParams.md).`ConfType`
