# MABV - Menu Abbreviation

- **Tabla:** MABV
- **Descripción:** Menu Abbreviation
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MABV.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `absEntry` | Internal Key | Int | 11 | - |  |  |
| 2 | `pkgName` | Package Name | nVarChar | 200 | - |  |  |
| 3 | `fileName` | FileName | nVarChar | 200 | - |  |  |
| 4 | `imprtDate` | Import Date | Date | 8 | - |  |  |
| 5 | `pkgPath` | Package Path | nVarChar | 200 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | absEntry |
| PKG_NAME | Yes | pkgName |
