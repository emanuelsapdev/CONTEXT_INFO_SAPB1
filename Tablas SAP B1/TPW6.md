# TPW6 - Journal Entry Information

- **Tabla:** TPW6
- **Descripción:** Journal Entry Information
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TPW6.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | [OTPW](OTPW.md) |  |  |
| 2 | `JeId` | JE Number | Int | 11 | [OJDT](OJDT.md) |  |  |
| 3 | `JeLineId` | Line Number of JE | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, JeId, JeLineId |
