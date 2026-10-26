# MPO1 - Value Mapping Data

- **Tabla:** MPO1
- **Descripción:** Value Mapping Data
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MPO1.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `LineId` | Line Id | Int | 11 | - |  |  |
| 3 | `ThirdPID` | Third party internal number | Int | 11 | - |  |  |
| 4 | `ThirdPVal` | Third Party Value | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineId |
