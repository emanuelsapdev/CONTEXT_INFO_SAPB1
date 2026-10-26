# APJT - Project Plan

- **Tabla:** APJT
- **Descripción:** Project Plan
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/APJT.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `TempType` | Template Type | VarChar | 1 | - | N | `S` = System Template<br>`N` = Nonsystem Template |
| 3 | `TempName` | Template Name | nVarChar | 254 | - |  |  |
| 4 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |
| 5 | `UserSign` | User Signature | Int | 11 | [OUSR](OUSR.md) |  |  |
| 6 | `UserSign2` | Updating User | Int | 11 | [OUSR](OUSR.md) |  |  |
| 7 | `CreateDate` | Production Date | Date | 8 | - |  |  |
| 8 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 9 | `TempDesc` | Template Description | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LogInstanc |
