# SCRT - SAP Crystal Reports Translations

- **Tabla:** SCRT
- **Descripción:** SAP Crystal Reports Translations
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SCRT.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocCode` | Doc. Code | nVarChar | 8 | - |  |  |
| 2 | `ItemId` | Item ID | nVarChar | 220 | - |  |  |
| 3 | `Language` | Language | Int | 11 | [OLNG](OLNG.md) |  |  |
| 4 | `String` | String | nVarChar | 249 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocCode, ItemId, Language |
