# ACR12 - BP eDoc Settings - History

- **Tabla:** ACR12
- **Descripción:** BP eDoc Settings - History
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ACR12.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 2 | `ProtCode` | Communication Type or Protocol | Int | 11 | [OECM](OECM.md) |  | `0` = Invalid<br>`1` = GEN<br>`2` = EET<br>`3` = CFDI<br>`4` = FPA<br>`5` = MTD<br>`6` = EWB<br>`7` = PEPPOL<br>`8` = HOI<br>`10` = EIS<br>`11` = IIS<br>`12` = IIS_ANNUAL<br>`16` = RTIE<br>`17` = E-Billing<br>`18` = Tax Service<br>`19` = AFE<br>`20` = Doc. Sign.<br>`21` = KSeF<br>`29` = Veri*factu<br>`32` = FReINV |
| 3 | `GenType` | Generation Type | VarChar | 1 | - |  | `N` = Not Relevant<br>`G` = Generate<br>`L` = Generate Later |
| 4 | `MapID` | Electronic Document Format Mapping | Int | 11 | - |  |  |
| 5 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 6 | `VatStruct` | VAT Structure | nVarChar | 64 | - |  |  |
| 7 | `ParticipID` | Participant ID | nVarChar | 128 | - |  |  |
| 8 | `ElecUID` | Electronic UID | nVarChar | 46 | - |  |  |
| 9 | `C5Relevant` | Corner 5 Relevant | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CardCode, ProtCode, LogInstanc |
