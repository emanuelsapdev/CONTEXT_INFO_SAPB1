# OSRL - Serial Numbers

- **Tabla:** OSRL
- **Descripción:** Serial Numbers
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSRL.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 2 | `SerialNum` | Serial Number | nVarChar | 17 | - |  |  |
| 3 | `CardCode` | Customer Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 4 | `DocNum` | Invoice Number | Int | 11 | - |  |  |
| 5 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ItemCode, SerialNum |
| INV_NUM | No | DocNum, ItemCode |
| CARD_KEY | No | CardCode |
