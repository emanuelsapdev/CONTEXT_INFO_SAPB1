# CUDC - User Display Cat.

- **Tabla:** CUDC
- **Descripción:** User Display Cat.
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CUDC.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CodeID` | Code | Int | 11 | - |  |  |
| 2 | `NameID` | Name | nVarChar | 20 | - |  |  |
| 3 | `FormID` | Form ID | Int | 11 | - |  |  |
| 4 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CodeID |
| FORM | No | NameID |
