# QAG1 - Query Authorization Group Assignment

- **Tabla:** QAG1
- **Descripción:** Query Authorization Group Assignment
- **Cantidad de campos:** 2
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/QAG1.html

## Campos (2)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AUTHGRPID` | Query Authorization Group ID | Int | 11 | [OQAG](OQAG.md) |  |  |
| 2 | `CATEGORYID` | Category ID | Int | 11 | [OQCN](OQCN.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AUTHGRPID, CATEGORYID |
