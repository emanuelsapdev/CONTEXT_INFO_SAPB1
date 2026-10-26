# OMSG - Messaging Service Settings

- **Tabla:** OMSG
- **Descripción:** Messaging Service Settings
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OMSG.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `USERID` | User Signature | Int | 6 | - | -1 |  |
| 2 | `Signature` | E-Mail signature | Text | 16 | - |  |  |
| 3 | `UseCompSig` | Use Company Signature | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 4 | `DummySig` | Dummy Signature | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | USERID |
