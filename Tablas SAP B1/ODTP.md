# ODTP - Fixed Assets Depreciation Types

- **Tabla:** ODTP
- **Descripción:** Fixed Assets Depreciation Types
- **Cantidad de campos:** 51
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODTP.html

## Campos (51)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | nVarChar | 15 | - |  |  |
| 2 | `Descr` | Description | nVarChar | 100 | - |  |  |
| 3 | `DprMeth` | Depreciation Method | nVarChar | 2 | - | NO | `NO` = No Depreciation<br>`SL` = Straight Line<br>`SP` = Straight Line Period Control<br>`DB` = Declining Balance<br>`ML` = Multilevel<br>`WO` = Immediate Write-Off<br>`SD` = Special Depreciation<br>`MD` = Manual Depreciation<br>`CF` = Accelerated |
| 4 | `DprTo` | Minimum Depreciated Value | Num | 19.6 | - |  |  |
| 5 | `Rounding` | Round Year End Book Value | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 6 | `InclSalv` | Include Salvage Value in Depr. | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `SalvPerc` | Percentage for Salvage Value | Num | 19.6 | - |  |  |
| 8 | `PerAcq` | Period Control for Acquisition | nVarChar | 2 | - | PR | `PR` = Pro Rata Temporis<br>`HY` = First Year Convention<br>`6M` = Half Year<br>`FY` = Full Year |
| 9 | `PerSubAcq` | Period Control Subacquisition | nVarChar | 2 | - | PR | `PR` = Pro Rata Temporis<br>`YR` = Half Year Convention<br>`FY` = Full Year |
| 10 | `PerRet` | Period Control for Retirement | nVarChar | 2 | - | PR | `PR` = Pro Rata Temporis<br>`YR` = Half Year Convention<br>`EL` = After End of Useful Life |
| 11 | `AcqPRTyp` | Type of PRT for Acquisition | nVarChar | 3 | - | EDB | `EDB` = Exact Daily Base<br>`FCP` = First Day of Current Period<br>`FNP` = First Day of Next Period |
| 12 | `SubPRTyp` | Type of PR for Subacquisition | nVarChar | 3 | - | EDB | `EDB` = Exact Daily Base<br>`FCP` = First Day of Current Period<br>`FNP` = First Day of Next Period |
| 13 | `RetPRTyp` | Type of PR for Retirement | nVarChar | 3 | - | EDB | `EDB` = Exact Daily Base<br>`LPP` = Last Day of Prior Period<br>`LCP` = Last Day of Current Period |
| 14 | `PerDpRev` | Depreciation to Be Reversed % | Num | 19.6 | - |  |  |
| 15 | `ValidFrom` | Valid From | Date | 8 | - | 19000101 |  |
| 16 | `ValidTo` | Valid To | Date | 8 | - | 20991231 |  |
| 17 | `sCalcMeth` | Calc. Method for Straight Line | nVarChar | 3 | - | APC | `APC` = Acquisition Value/Total Useful Life<br>`PRC` = Percentage of Acquisition Value<br>`NBV` = Net Book Value/Remaining Life |
| 18 | `sPercent` | Percentage for Straight Line | Num | 19.6 | - |  |  |
| 19 | `dBase` | Base for Declining Balance | nVarChar | 3 | - | NBV | `NBV` = Net Book Value |
| 20 | `dPercent` | Percentage for Decl. Balance | Num | 19.6 | - |  |  |
| 21 | `dFactor` | Factor for Declining Balance | Num | 19.6 | - | 1 |  |
| 22 | `dAltDprTyp` | Auto. Change Depreciation Type | nVarChar | 15 | [ODTP](ODTP.md) |  |  |
| 23 | `maDecBase` | Reduce Depreciation Base | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 24 | `spMeth` | Calc. Method for Special Depr. | VarChar | 1 | - | D | `D` = Additional<br>`A` = Alternative |
| 25 | `spConcPer` | Concession Period in Years | Int | 11 | - |  |  |
| 26 | `spMaxPerc` | Maximum Percentage | Num | 19.6 | - |  |  |
| 27 | `spAdDpr` | Normal Depreciation | nVarChar | 15 | [ODTP](ODTP.md) |  |  |
| 28 | `spAlDpr` | Alternative Depreciation | nVarChar | 15 | [ODTP](ODTP.md) |  |  |
| 29 | `PoolID` | Depreciation Type Pool ID | nVarChar | 2 | [ODPP](ODPP.md) |  |  |
| 30 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 31 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 32 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 33 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 34 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 35 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 36 | `DprPer` | Depreciation Periods | VarChar | 1 | - | S | `S` = Standard<br>`I` = Individual<br>`U` = Individual Usage |
| 37 | `PerFactor` | Period Factor | Num | 19.6 | - | 1 |  |
| 38 | `spMaxAmnt` | Maximum Amount | Num | 19.6 | - |  |  |
| 39 | `spMaxFlag` | Max. [Percentage\Amount] | VarChar | 1 | - | P | `P` = Percentage<br>`A` = Amount |
| 40 | `CalcBase` | Calculation Base | VarChar | 1 | - | Y | `Y` = Yearly<br>`M` = Monthly |
| 41 | `DeprEndLFY` | Depr. End at Last Full Year | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 42 | `AccuPriorP` | Accu. Depr. of Prior Periods | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 43 | `DeltaCoeff` | Delta Coefficient | Int | 11 | - | 0 |  |
| 44 | `MaxDepr` | Maximum Depreciable Value | Num | 19.6 | - |  |  |
| 45 | `FactorFFY` | Factor Only Relevant to FFY | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 46 | `SnapshotId` | Snapshot ID | Int | 11 | - | 0 |  |
| 47 | `PerTranSou` | Period Control Transfer Source | nVarChar | 2 | - | PR | `PR` = Pro Rata Temporis |
| 48 | `PerTranTar` | Period Control Transfer Target | nVarChar | 2 | - | PR | `PR` = Pro Rata Temporis |
| 49 | `TranSPRTyp` | Type of PR for Transfer Source | nVarChar | 3 | - | EDB | `EDB` = Exact Daily Base<br>`LPP` = Last Day of Prior Period<br>`LCP` = Last Day of Current Period |
| 50 | `TranTPRTyp` | Type of PR for Transfer Target | nVarChar | 3 | - | EDB | `EDB` = Exact Daily Base<br>`FCP` = First Day of Current Period<br>`FNP` = First Day of Next Period |
| 51 | `RoundMeth` | Rounding Method | VarChar | 1 | - | N | `N` = Truncate to Integer<br>`U` = Round Up to Integer<br>`D` = Round Down to Integer |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
