# OERN - Excise Register Numbering

- **Tabla:** OERN
- **Descripción:** Excise Register Numbering
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OERN.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `NumTypeID` | ID for numbering type | Int | 11 | - |  |  |
| 2 | `NumTypeNam` | Name for numbering type | nVarChar | 30 | - |  |  |
| 3 | `FirstNum` | First number | Int | 11 | - | 1 |  |
| 4 | `NextNum` | Next Number | Int | 11 | - | 1 |  |
| 5 | `LastNum` | Last Number | Int | 11 | - |  |  |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `ResetDate` | Date of last reset | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | NumTypeID |
