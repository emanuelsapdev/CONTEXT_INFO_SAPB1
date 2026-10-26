# OULA - EULA

- **Tabla:** OULA
- **Descripción:** EULA
- **Cantidad de campos:** 15
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OULA.html

## Campos (15)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SerialNum` | Serial Number | Int | 11 | - |  |  |
| 2 | `Signed` | Signed | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 3 | `Checked` | Checked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 4 | `EULAType` | EULA Type | VarChar | 1 | - | P | `E` = Evaluation<br>`P` = Productive |
| 5 | `Licensor` | Licensor | nVarChar | 100 | - |  |  |
| 6 | `Licensee` | Licensee | nVarChar | 100 | - |  |  |
| 7 | `InstallNo` | Installation Number | nVarChar | 30 | - |  |  |
| 8 | `Signer` | Signer | nVarChar | 155 | - |  |  |
| 9 | `UFunction` | Signer Function | nVarChar | 100 | - |  |  |
| 10 | `Username` | B1 User Name | nVarChar | 155 | - |  |  |
| 11 | `SignDate` | Signing Date | Date | 8 | - |  |  |
| 12 | `DocVer` | EULA Document Version | nVarChar | 50 | - |  |  |
| 13 | `EULADoc` | EULA Document | Text | 16 | - |  |  |
| 14 | `EULAFormat` | EULA Format | nVarChar | 50 | - | TXT | `PDF` = PDF<br>`TXT` = TXT |
| 15 | `Checksum` | EULA Record Checksum | nVarChar | 150 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SerialNum |
