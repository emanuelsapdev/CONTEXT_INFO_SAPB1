# STA1 - Valid Period

- **Tabla:** STA1
- **Descripción:** Valid Period
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/STA1.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `StaCode` | Tax Parameter Code | nVarChar | 8 | [OSTA](OSTA.md) |  |  |
| 2 | `SttType` | Tax Type | Int | 11 | [OSTT](OSTT.md) |  |  |
| 3 | `EfctDate` | Effective From | Date | 8 | - |  |  |
| 4 | `Rate` | Rate | Num | 19.6 | - |  |  |
| 5 | `TaaSUpdate` | Last Update By TaaS | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | StaCode, SttType, EfctDate |
