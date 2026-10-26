# OTWS - E-Tax Web Site

- **Tabla:** OTWS
- **Descripción:** E-Tax Web Site
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OTWS.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | E-Tax Internal ID | Int | 6 | - |  |  |
| 2 | `TwsName` | E-Tax Web Site Name | nVarChar | 64 | - |  |  |
| 3 | `TwsURL` | E-Tax Web Site URL | Text | 16 | - |  |  |
| 4 | `TwsDescrip` | E-Tax Web Site Description | nVarChar | 200 | - |  |  |
| 5 | `UserSign` | User Signature - Create | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| TWSNAME | No | TwsName |
