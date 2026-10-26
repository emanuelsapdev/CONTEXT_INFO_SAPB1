# SCLC - SCLC

- **Tabla:** SCLC
- **Descripción:** SCLC
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SCLC.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `LangCode` | Language Code | Int | 11 | - |  |  |
| 2 | `BaseID` | Base language ID | Int | 11 | - |  |  |
| 3 | `HotKeyID` | Hotkey language ID | Int | 11 | - |  |  |
| 4 | `Updated` | Date of update | Date | 8 | - |  |  |
| 5 | `File` | Localization Resource File | Text | 16 | - |  |  |
| 6 | `FileName` | Localization file name | nVarChar | 64 | - |  |  |
| 7 | `UpdTime` | Time of update | Int | 11 | - |  |  |
| 8 | `Version` | B1 version | nVarChar | 32 | - |  |  |
| 9 | `PatchLevel` | Special build string | nVarChar | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | LangCode |
