# MVLD - MVLD

- **Tabla:** MVLD
- **Descripción:** MVLD
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MVLD.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `guid` | Guid | nVarChar | 36 | - |  |  |
| 2 | `fatherId` | Father Id | nVarChar | 36 | - |  |  |
| 3 | `lineNum` | Line Number | Int | 11 | - |  |  |
| 4 | `value` | Value | nVarChar | 254 | - |  |  |
| 5 | `note` | Note | nVarChar | 254 | - |  |  |
| 6 | `noteSid` | Note String Id | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | fatherId, lineNum |
| GUID | Yes | guid |
