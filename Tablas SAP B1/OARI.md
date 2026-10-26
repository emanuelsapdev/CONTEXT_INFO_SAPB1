# OARI - Add-On - Company Definitions

- **Tabla:** OARI
- **Descripción:** Add-On - Company Definitions
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OARI.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AddOnID` | Add-On ID | Int | 11 | - |  |  |
| 2 | `EGroup` | Execution Group | VarChar | 1 | - |  | `A` = Automatic<br>`M` = Manual<br>`C` = Critical |
| 3 | `AStatus` | Is add-on active? | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 4 | `EventOrder` | Add-on Event Order | Int | 11 | - |  |  |
| 5 | `IsAdd64` | Add-On is 64 Bit | VarChar | 1 | - | N |  |
| 6 | `AddPlat` | Add-On Installer Platform | VarChar | 1 | - | N | `N` = x86<br>`X` = x64<br>`A` = ARM |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AddOnID |
