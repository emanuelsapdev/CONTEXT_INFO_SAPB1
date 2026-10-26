# XSXA - XS XApp Registration Info

- **Tabla:** XSXA
- **Descripción:** XS XApp Registration Info
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/XSXA.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `XID` | XID | nVarChar | 64 | - |  |  |
| 2 | `NAME` | NAME | nVarChar | 254 | - |  |  |
| 3 | `VERSION` | VERSION | nVarChar | 64 | - |  |  |
| 4 | `PACKAGE` | PACKAGE | nVarChar | 254 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | XID |
| XS_NAME | Yes | NAME |
| XS_PACKAGE | Yes | PACKAGE |
