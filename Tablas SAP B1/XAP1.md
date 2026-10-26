# XAP1 - Page of XAPP

- **Tabla:** XAP1
- **Descripción:** Page of XAPP
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/XAP1.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Key of page | Int | 11 | - |  |  |
| 2 | `XAPEntry` | Foreign key of XAPP | Int | 11 | - |  |  |
| 3 | `Name` | Page name | nVarChar | 250 | - |  |  |
| 4 | `Default` | Is default or not | VarChar | 1 | - | N |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
