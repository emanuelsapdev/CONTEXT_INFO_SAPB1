# ODCC - Dashboard Cache Configuration

- **Tabla:** ODCC
- **Descripción:** Dashboard Cache Configuration
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODCC.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Abs Entry | Int | 11 | - |  |  |
| 2 | `Enable` | Enable | VarChar | 1 | - | N | `Y`<br>`N` |
| 3 | `Start` | Start | Int | 11 | - |  |  |
| 4 | `CronString` | Cron String | nVarChar | 254 | - |  |  |
| 5 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
