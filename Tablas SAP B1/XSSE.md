# XSSE - XS Session

- **Tabla:** XSSE
- **Descripción:** XS Session
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/XSSE.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SID` | SID | nVarChar | 32 | - |  |  |
| 2 | `XKEY` | XKEY | nVarChar | 50 | - |  |  |
| 3 | `VALUE` | VALUE | Text | 16 | - |  |  |
| 4 | `UPDATETIME` | UPDATETIME | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SID, XKEY |
