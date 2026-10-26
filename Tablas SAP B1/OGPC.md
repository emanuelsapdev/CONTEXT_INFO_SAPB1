# OGPC - Government Payment Code

- **Tabla:** OGPC
- **Descripción:** Government Payment Code
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OGPC.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | - |  |  |
| 2 | `Code` | Code | nVarChar | 6 | - |  |  |
| 3 | `Descr` | Description | nVarChar | 100 | - |  |  |
| 4 | `StateTax` | Reporting by State | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `Prdcity` | Periodicity | VarChar | 1 | - | M | `M` = Monthly<br>`Q` = Quarterly<br>`H` = Semimonthly<br>`T` = Every 10 Days |
| 6 | `SPEDCtgory` | SPED Category | Int | 11 | - |  | `1` = ICMS<br>`2` = ICMS-ST<br>`3` = IPI<br>`4` = ISS<br>`5` = PIS<br>`6` = COFINS<br>`7` = PIS-ST<br>`8` = COFINS-ST |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
| CODE | Yes | Code |
