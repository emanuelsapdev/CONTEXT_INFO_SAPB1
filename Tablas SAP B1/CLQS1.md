# CLQS1 - List of Question Orders for "Ask AI" App in Web Client

- **Tabla:** CLQS1
- **Descripción:** List of Question Orders for "Ask AI" App in Web Client
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CLQS1.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SeqId` | Internal Question Order ID | Int | 11 | [OCLQS](OCLQS.md) |  |  |
| 2 | `QuestionId` | Question ID | Int | 11 | [OCLQ](OCLQ.md) |  |  |
| 3 | `VisOrder` | Visible Order | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SeqId, QuestionId |
