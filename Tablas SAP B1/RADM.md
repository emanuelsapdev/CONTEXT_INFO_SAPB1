# RADM - Resource Administration

- **Tabla:** RADM
- **Descripción:** Resource Administration
- **Cantidad de campos:** 21
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RADM.html

## Campos (21)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DevGroup` | Development Group | nVarChar | 3 | - |  |  |
| 2 | `ResVersion` | Resource Version | nVarChar | 5 | - |  |  |
| 3 | `ReleaseDte` | Rsleade Date | Date | 8 | - |  |  |
| 4 | `RelFrzDate` | GUI Freeze Date for Release | Date | 8 | - |  |  |
| 5 | `Sp1Date` | SP1 Date | Date | 8 | - |  |  |
| 6 | `Sp1FrzDate` | GUI Freeze Date for SP1 | Date | 8 | - |  |  |
| 7 | `Sp2Date` | SP2 Date | Date | 8 | - |  |  |
| 8 | `Sp2FrzDate` | GUI Freeze Date for SP2 | Date | 8 | - |  |  |
| 9 | `DbLocked` | Is DB Locked for Edit | Int | 11 | - |  | `0` = Not Locked<br>`1` = GUI Freeze (Translations)<br>`2` = Read Only<br>`3` = Full Lock |
| 10 | `DbVersion` | Resource DB Version | nVarChar | 10 | - |  |  |
| 11 | `CreateDate` | Creation Date of DB | Date | 8 | - |  |  |
| 12 | `CreateTime` | Creation Time of DB | Int | 11 | - | 0 |  |
| 13 | `CanLogin` | Can Users Login | VarChar | 1 | - |  |  |
| 14 | `ValidPath` | Valid Path For Running | nVarChar | 100 | - |  |  |
| 15 | `P4Path` | P4 Version Path | nVarChar | 100 | - |  |  |
| 16 | `MDVersion` | Metadata Version | Int | 11 | - | -1 |  |
| 17 | `VerScpDate` | Version Scope Date | Date | 8 | - |  |  |
| 18 | `VerScpTime` | Version Scope Time | Int | 11 | - | 0 |  |
| 19 | `TransVer` | Translation Version | nVarChar | 10 | - |  |  |
| 20 | `Flags` | Resource flags | nVarChar | 100 | - |  |  |
| 21 | `WpFileName` | Wallpaper File Name | nVarChar | 100 | - | NotSet |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ResVersion |
