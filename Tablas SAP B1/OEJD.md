# OEJD - Company Details for ERV-JAb

- **Tabla:** OEJD
- **Descripción:** Company Details for ERV-JAb
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OEJD.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `CRegNum` | Commercial Register Number | nVarChar | 7 | - |  |  |
| 3 | `LFBSheet` | Legal Form on Actl Bal Sht Dte | nVarChar | 3 | - |  | `AG` = Public Limited Company (AG)<br>`SC` = European Cooperative Society (SCE)<br>`SE` = Company under European Law (SE, Societa Europaea)<br>`GEN` = Industrial Cooperative Society<br>`GES` = Limited Liability Company (GmbH)<br>`KG` = Limited Partnership<br>`OG` = Open Company |
| 4 | `LFBSheetPr` | Lgl Form on Bal Sht Dte Prv Yr | nVarChar | 3 | - |  | `AG` = Public Limited Company (AG)<br>`SC` = European Cooperative Society (SCE)<br>`SE` = Company under European Law (SE, Societa Europaea)<br>`GEN` = Industrial Cooperative Society<br>`GES` = Limited Liability Company (GmbH)<br>`KG` = Limited Partnership<br>`OG` = Open Company<br>`CNE` = Company does not exist |
| 5 | `RegNum` | Reg. No. of Partner Company | nVarChar | 7 | - |  |  |
| 6 | `CmpanyName` | Company Name | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
