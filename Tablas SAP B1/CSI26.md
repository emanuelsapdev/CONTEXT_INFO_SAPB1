# CSI26 - A/R Correction Invoice - E-Way Bill Information

- **Tabla:** CSI26
- **Descripción:** A/R Correction Invoice - E-Way Bill Information
- **Cantidad de campos:** 37
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CSI26.html

## Campos (37)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [OCSI](OCSI.md) |  |  |
| 2 | `SuplyType` | EWB Transaction Type | nVarChar | 20 | - |  | `O` = Outward<br>`I` = Inward |
| 3 | `SubSplyTyp` | EWB Sub-Type | Int | 11 | [OEST](OEST.md) |  |  |
| 4 | `DocType` | EWB Doc. Type | nVarChar | 3 | [OEDT](OEDT.md) |  |  |
| 5 | `TransMode` | EWB Transportation Mode | Int | 11 | [OETM](OETM.md) |  |  |
| 6 | `Distance` | EWB Transport Distance | Num | 19.6 | - |  |  |
| 7 | `TransDocNo` | EWB Transporter Doc. No. | nVarChar | 16 | - |  |  |
| 8 | `TransDate` | EWB Transportation Date | Date | 8 | - |  |  |
| 9 | `VehicleTyp` | EWB Vehicle Type | nVarChar | 2 | [OEVT](OEVT.md) |  |  |
| 10 | `VehicleNo` | EWB Vehicle Number | nVarChar | 15 | - |  |  |
| 11 | `EWayBillNo` | EWB No. | nVarChar | 20 | - |  |  |
| 12 | `EwbDate` | E-Way Bill Date | Date | 8 | - |  |  |
| 13 | `FrmTraName` | EWB Consignor Name | nVarChar | 200 | - |  |  |
| 14 | `FrmAddres1` | EWB Consignor Address 1 | nVarChar | 120 | - |  |  |
| 15 | `FrmAddres2` | EWB Consignor Address 2 | nVarChar | 120 | - |  |  |
| 16 | `FrmZipCode` | EWB Consignor Zip Code | nVarChar | 20 | - |  |  |
| 17 | `ActFrmStat` | Dispatch State of EWB Consignor | nVarChar | 2 | - |  |  |
| 18 | `ToTraName` | EWB Consignee Name | nVarChar | 200 | - |  |  |
| 19 | `ToAddres1` | EWB Consignee Address 1 | nVarChar | 120 | - |  |  |
| 20 | `ToAddres2` | EWB Consignee Address 2 | nVarChar | 120 | - |  |  |
| 21 | `ToZipCode` | EWB Consignee Zip Code | nVarChar | 20 | - |  |  |
| 22 | `ActToState` | Ship-To State of EWB Consignee | nVarChar | 2 | - |  |  |
| 23 | `FrmGSTN` | EWB Consignor GSTN | nVarChar | 15 | - |  |  |
| 24 | `FrmState` | Bill-To State of EWB Consignor | nVarChar | 2 | - |  |  |
| 25 | `ToGSTN` | EWB Consignee GSTN | nVarChar | 15 | - |  |  |
| 26 | `ToState` | Bill-To State of EWB Consignee | nVarChar | 2 | - |  |  |
| 27 | `MainHsnEnt` | EWB Main HSN Entry | Int | 11 | [OCHP](OCHP.md) |  |  |
| 28 | `FrmPlace` | EWB Consignor Place | nVarChar | 50 | - |  |  |
| 29 | `ToPlace` | EWB Consignee Place | nVarChar | 50 | - |  |  |
| 30 | `TransID` | EWB Transporter ID | nVarChar | 15 | - |  |  |
| 31 | `TransName` | EWB Transporter Name | nVarChar | 25 | - |  |  |
| 32 | `ExpireDate` | EWB Expiration Date | Date | 8 | - |  |  |
| 33 | `ObjectType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 165 |  |
| 34 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 35 | `TspEntry` | Transporter Abs. Entry | Int | 11 | [OTSP](OTSP.md) |  |  |
| 36 | `TspLine` | Transportation Line | Int | 11 | - |  |  |
| 37 | `TransType` | Transaction Type | Int | 11 | - |  | `1` = Regular<br>`2` = Bill To-Ship To<br>`3` = Bill From-Dispatch From<br>`4` = Combination of 2 and 3 |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry |
