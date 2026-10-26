# OWST - Confirmation Level

- **Tabla:** OWST
- **Descripción:** Confirmation Level
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWST.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WstCode` | Stage | Int | 11 | [OWST](OWST.md) |  |  |
| 2 | `Name` | Name | nVarChar | 20 | - |  |  |
| 3 | `Remarks` | Description | nVarChar | 100 | - |  |  |
| 4 | `MaxReqr` | No. of Authorizers | Int | 6 | - | 1 |  |
| 5 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `MaxRejReqr` | No. of Rejects | Int | 6 | - | 1 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WstCode |
| NAME | Yes | Name |
