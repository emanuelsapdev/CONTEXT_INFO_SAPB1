# OLCT - Location

- **Tabla:** OLCT
- **Descripción:** Location
- **Cantidad de campos:** 51
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OLCT.html

## Campos (51)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Location Code | Int | 11 | - |  |  |
| 2 | `Location` | Name | nVarChar | 100 | - |  |  |
| 3 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 4 | `PanCirNo` | PAN Circle No. | nVarChar | 32 | - |  |  |
| 5 | `PanWardNo` | PAN Ward No. | nVarChar | 32 | - |  |  |
| 6 | `PanOfficer` | PAN Assessing Officer | nVarChar | 32 | - |  |  |
| 7 | `TanCirNo` | TAN Circle No. | nVarChar | 32 | - |  |  |
| 8 | `TanWardNo` | TAN Ward No. | nVarChar | 32 | - |  |  |
| 9 | `TanOfficer` | TAN Assessing Officer | nVarChar | 32 | - |  |  |
| 10 | `LstVatNo` | LST/VAT Number | nVarChar | 100 | - |  |  |
| 11 | `CstNo` | CST Number | nVarChar | 100 | - |  |  |
| 12 | `ExemptNo` | Exemption Number | nVarChar | 100 | - |  |  |
| 13 | `TanNo` | TAN Number | nVarChar | 100 | - |  |  |
| 14 | `ServTaxNo` | Service Tax Number | nVarChar | 100 | - |  |  |
| 15 | `AsseType` | Assessee Type | nVarChar | 100 | - |  |  |
| 16 | `CompType` | Company Type | nVarChar | 100 | - |  |  |
| 17 | `NatOfBiz` | Nature of Business | nVarChar | 100 | - |  |  |
| 18 | `TinNo` | TIN Number | nVarChar | 100 | - |  |  |
| 19 | `PanNo` | PAN Number | nVarChar | 10 | - |  |  |
| 20 | `RegType` | Registration Type | nVarChar | 2 | - |  | `XM` = XM<br>`XD` = XD<br>`EM` = EM<br>`ED` = ED<br>`SD` = SD |
| 21 | `EccNo` | ECC Number | nVarChar | 40 | - |  |  |
| 22 | `CeRegNo` | CE Register Number | nVarChar | 40 | - |  |  |
| 23 | `CeRange` | CE Range | nVarChar | 60 | - |  |  |
| 24 | `CeDivision` | CE Division | nVarChar | 60 | - |  |  |
| 25 | `CeComRate` | CE Commissionerate | nVarChar | 60 | - |  |  |
| 26 | `ManuCode` | Manufaturer Code | nVarChar | 60 | - |  |  |
| 27 | `Jurisd` | Jurisdiction | nVarChar | 60 | - |  |  |
| 28 | `Street` | Street | nVarChar | 100 | - |  |  |
| 29 | `Block` | Block | nVarChar | 100 | - |  |  |
| 30 | `ZipCode` | Zip Code | nVarChar | 20 | - |  |  |
| 31 | `City` | City | nVarChar | 100 | - |  |  |
| 32 | `County` | County | nVarChar | 100 | - |  |  |
| 33 | `Country` | Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 34 | `State` | State | nVarChar | 3 | - |  |  |
| 35 | `Building` | Building/Floor/Room | Text | 16 | - |  |  |
| 36 | `SSIExmpt` | SSI Exemption | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 37 | `SSIExmptSt` | SSI Exemption Status | VarChar | 1 | - | E | `E` = New Location<br>`N` = Upgrade Not Changed<br>`C` = Upgrade Changed |
| 38 | `CitAddress` | CIT Address | nVarChar | 254 | - |  |  |
| 39 | `CitCity` | CIT City | nVarChar | 100 | - |  |  |
| 40 | `CitPinCode` | CIT Pin Code | nVarChar | 10 | - |  |  |
| 41 | `OnHoldAct` | Capital Goods On Hold Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 42 | `GSTRegnNo` | GSTIN | nVarChar | 15 | - |  |  |
| 43 | `GSTRelevt` | GST Location Relevant | nVarChar | 2 | - | N |  |
| 44 | `GSTTDS` | GSTIN TDS | nVarChar | 30 | - |  |  |
| 45 | `GSTISD` | GSTIN ISD | nVarChar | 30 | - |  |  |
| 46 | `GSTType` | GST Type | Int | 11 | [OGTY](OGTY.md) |  | `-1`<br>`1` = Regular/TDS/ISD<br>`2` = Casual Taxable Person<br>`3` = Composition Levy<br>`4` = Government Department or PSU<br>`5` = Non-Resident Taxable Person<br>`6` = UN Agency or Embassy |
| 47 | `VendorCode` | Vendor Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 48 | `CstmerCode` | Customer Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 49 | `DropShip` | Drop Ship Warehouse | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 50 | `IngClrAc` | Ineligible ITC Clearing A/C | nVarChar | 15 | - |  |  |
| 51 | `IntBrClrAc` | Inter-branch ITC Clearing A/C | nVarChar | 15 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
| LOCATION | Yes | Location |
