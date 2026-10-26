# UPT1 - User Authorization Tree - Extended Permission

- **Tabla:** UPT1
- **Descripción:** User Authorization Tree - Extended Permission
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UPT1.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PermId` | Authorization ID | nVarChar | 20 | [OUPT](OUPT.md) |  |  |
| 2 | `FormId` | Form ID | nVarChar | 20 | - |  |  |
| 3 | `VisOrder` | Display Order | Int | 6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | PermId, FormId |
| FORM_ID | No | FormId |
