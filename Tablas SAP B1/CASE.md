# CASE - Internal Recon. Upgrade 2007A

- **Tabla:** CASE
- **Descripción:** Internal Recon. Upgrade 2007A
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CASE.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Intl ID for Inconsistent Amt | Int | 11 | - |  |  |
| 2 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 3 | `CreateTime` | Creation Time | Int | 6 | - |  |  |
| 4 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 5 | `Message` | Show Message? | VarChar | 1 | - | N | `Y`<br>`N`<br>`S` |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
