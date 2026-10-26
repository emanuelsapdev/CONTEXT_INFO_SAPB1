# AOA4 - Blanket Agreement - Recurring Transactions

- **Tabla:** AOA4
- **Descripción:** Blanket Agreement - Recurring Transactions
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AOA4.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AgrNo` | Agreement No. | Int | 11 | [OOAT](OOAT.md) |  |  |
| 2 | `RcpEntry` | Recurring Template Entry | Int | 11 | [ORCP](ORCP.md) |  |  |
| 3 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AgrNo, RcpEntry, LogInstanc |
