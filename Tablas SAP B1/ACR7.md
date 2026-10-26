# ACR7 - Fiscal IDs for BP Master Data - History

- **Tabla:** ACR7
- **Descripción:** Fiscal IDs for BP Master Data - History
- **Cantidad de campos:** 27
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ACR7.html

## Campos (27)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CardCode` | BP Code | nVarChar | 25 | [OCRD](OCRD.md) |  |  |
| 2 | `Address` | Address | nVarChar | 50 | - |  |  |
| 3 | `TaxId0` | Tax ID 0 | nVarChar | 100 | - |  |  |
| 4 | `TaxId1` | Tax ID 1 | nVarChar | 100 | - |  |  |
| 5 | `TaxId2` | Tax ID 2 | nVarChar | 100 | - |  |  |
| 6 | `TaxId3` | Tax ID 3 | nVarChar | 100 | - |  |  |
| 7 | `TaxId4` | Tax ID 4 | nVarChar | 100 | - |  |  |
| 8 | `TaxId5` | Tax ID 5 | nVarChar | 100 | - |  |  |
| 9 | `TaxId6` | Tax ID 6 | nVarChar | 100 | - |  |  |
| 10 | `TaxId7` | Tax ID 7 | nVarChar | 100 | - |  |  |
| 11 | `TaxId8` | Tax ID 8 | nVarChar | 100 | - |  |  |
| 12 | `TaxId9` | Tax ID 9 | nVarChar | 100 | - |  |  |
| 13 | `CNAEId` | Brazilian CNAE Code | Int | 11 | [OCNA](OCNA.md) |  |  |
| 14 | `TaxId10` | Tax ID 10 | nVarChar | 100 | - |  |  |
| 15 | `TaxId11` | Tax ID 11 | nVarChar | 100 | - |  |  |
| 16 | `AddrType` | Address Type | VarChar | 1 | - | S | `S` = Ship To<br>`B` = Bill To |
| 17 | `ECCNo` | E.C.C. No. | nVarChar | 40 | - |  |  |
| 18 | `CERegNo` | C.E. Registration No. | nVarChar | 40 | - |  |  |
| 19 | `CERange` | C.E. Range | nVarChar | 60 | - |  |  |
| 20 | `CEDivis` | C.E. Division | nVarChar | 60 | - |  |  |
| 21 | `CEComRate` | C.E. Commisionerate | nVarChar | 60 | - |  |  |
| 22 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 23 | `SefazDate` | Date of Update from SEFAZ | Date | 8 | - |  |  |
| 24 | `TaxId12` | Tax ID 12 | nVarChar | 50 | - |  |  |
| 25 | `TaxId13` | Deductee Ref. No. in India | nVarChar | 100 | - |  |  |
| 26 | `AToRetrNFe` | Authorization to Retrieve NFe from SEFAZ | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 27 | `TaxId14` | ITR Filing | nVarChar | 250 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CardCode, Address, AddrType, LogInstanc |
