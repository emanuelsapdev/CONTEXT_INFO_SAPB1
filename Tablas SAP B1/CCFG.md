# CCFG - Company Configuration

- **Tabla:** CCFG
- **Descripción:** Company Configuration
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CCFG.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ConfigEntr` | Internal Configuration ID | Int | 11 | - |  |  |
| 2 | `ConfigName` | Configuration File Name | nVarChar | 250 | - |  |  |
| 3 | `ConfigDate` | Configuration File Create Date | Date | 8 | - |  |  |
| 4 | `ConfigTime` | Configuration File Create Time | Int | 6 | - |  |  |
| 5 | `UserCode` | Configuration Created By | Int | 11 | - |  |  |
| 6 | `CreateBy` | Created from Menu: | Int | 11 | - |  | `0` = Express Configuration Wizard<br>`1` = Configuration Management |
| 7 | `ServerName` | Configuration Saved on Server: | nVarChar | 250 | - |  |  |
| 8 | `CompanyDB` | Company Database | nVarChar | 250 | - |  |  |
| 9 | `Internal` | Internal | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ConfigEntr |
