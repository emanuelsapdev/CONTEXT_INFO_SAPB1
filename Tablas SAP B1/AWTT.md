# AWTT - Withholding Tax Type

- **Tabla:** AWTT
- **Descripción:** Withholding Tax Type
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AWTT.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WTTypeId` | Internal Number | Int | 11 | - |  |  |
| 2 | `WTType` | Type | nVarChar | 10 | - |  |  |
| 3 | `WTThresh` | Min. WTax Amount | Num | 19.6 | - |  |  |
| 4 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 5 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `UpdateDate` | Update Date | Date | 8 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WTTypeId, LogInstanc |
| WT_TYPE | Yes | WTType, LogInstanc |
