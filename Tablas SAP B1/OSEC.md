# OSEC - Sections

- **Tabla:** OSEC
- **Descripción:** Sections
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSEC.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | - |  |  |
| 2 | `Code` | Code | nVarChar | 15 | - |  |  |
| 3 | `Descr` | Description | nVarChar | 30 | - |  |  |
| 4 | `eCode` | eCode | nVarChar | 3 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
| CODE | Yes | Code |
| ECODE | Yes | eCode |
