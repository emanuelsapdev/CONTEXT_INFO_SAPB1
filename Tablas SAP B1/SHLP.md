# SHLP - Server Help

- **Tabla:** SHLP
- **Descripción:** Server Help
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SHLP.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `LangCode` | Language Code | nVarChar | 5 | - |  |  |
| 2 | `HelpImage` | Help Image | Text | 16 | - |  |  |
| 3 | `Version` | Help Version | Int | 11 | - |  |  |
| 4 | `helpPath` | Help Path | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | LangCode |
