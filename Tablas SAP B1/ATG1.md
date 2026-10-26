# ATG1 - Installment Layout - History

- **Tabla:** ATG1
- **Descripción:** Installment Layout - History
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ATG1.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CTGCode` | Payment Method Code | Int | 6 | [OCTG](OCTG.md) |  |  |
| 2 | `IntsNo` | Installment No. | Int | 6 | - |  |  |
| 3 | `InstMonth` | Installment Month | Int | 6 | - | 0 |  |
| 4 | `InstDays` | Installment Days | Int | 6 | - | 0 |  |
| 5 | `InstPrcnt` | Installment % | Num | 19.6 | - |  |  |
| 6 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CTGCode, IntsNo, LogInstanc |
| ABS_ENTRY | Yes | CTGCode, InstMonth, InstDays, LogInstanc |
