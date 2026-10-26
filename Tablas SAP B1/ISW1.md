# ISW1 - Reported Business Partners

- **Tabla:** ISW1
- **Descripción:** Reported Business Partners
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ISW1.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WizAbsEnt` | Wizard Run Key | Int | 11 | [OISW](OISW.md) |  |  |
| 2 | `CardCode` | Business Partner Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 3 | `CardName` | Business Partner Name | nVarChar | 200 | - |  |  |
| 4 | `CardType` | Business Partner Type | VarChar | 1 | - |  |  |
| 5 | `NatOfTrans` | Nature of Transaction | nVarChar | 50 | - |  |  |
| 6 | `StatProc` | Statistical Procedure | nVarChar | 50 | - |  |  |
| 7 | `CustProc` | Customs Procedure | nVarChar | 50 | - |  |  |
| 8 | `TransMode` | Transport Mode | nVarChar | 12 | - |  |  |
| 9 | `Incoterms` | Incoterms | nVarChar | 12 | - |  |  |
| 10 | `PortEnEx` | Port of Entry or Exit | nVarChar | 50 | - |  |  |
| 11 | `BPVATRegNo` | Business Partner VAT Reg. No. | nVarChar | 32 | - |  |  |
| 12 | `DomFrgID` | Domestic/Foreign Identifier | VarChar | 1 | - |  |  |
| 13 | `CtryOrig` | Country/Region of Origin | nVarChar | 3 | - |  |  |
| 14 | `BPCountry` | Business Partner Country/Region | nVarChar | 3 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WizAbsEnt, CardCode |
