# OMAO - Mobile Add-On Setting

- **Tabla:** OMAO
- **Descripción:** Mobile Add-On Setting
- **Cantidad de campos:** 13
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OMAO.html

## Campos (13)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | nVarChar | 20 | - |  |  |
| 2 | `Name` | Name | nVarChar | 200 | - |  |  |
| 3 | `URL` | Entry URL | Text | 16 | - |  |  |
| 4 | `Type` | Type | VarChar | 1 | - | M | `M` = Module<br>`H` = Home |
| 5 | `Provider` | Provider | nVarChar | 200 | - |  |  |
| 6 | `ViewStyle` | View Style | VarChar | 1 | - | P | `P` = Page - Universal<br>`F` = Full Screen - iPad<br>`L` = Landscape only - iPad |
| 7 | `LogonMethd` | Logon Method | VarChar | 1 | - | B | `B` = B1i Framework<br>`S` = Standard Logon<br>`N` = No Control |
| 8 | `LogonPyld` | Logon Payload | nVarChar | 254 | - | user={value1}&pwd={value2} |  |
| 9 | `Enable` | Enable | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 10 | `System` | System | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 11 | `B1MobileAp` | SAP Business One | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `B1SalesApp` | SAP Business One Sales | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 13 | `B1SrvcApp` | SAP Business One Service | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
