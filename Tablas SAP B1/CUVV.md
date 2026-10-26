# CUVV - User Validations

- **Tabla:** CUVV
- **Descripción:** User Validations
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CUVV.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IndexID` | Index | Int | 11 | [CSHS](CSHS.md) |  |  |
| 2 | `Value` | Field Value | nVarChar | 254 | - |  |  |
| 3 | `LineNum` | Row Number | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | IndexID, LineNum |
