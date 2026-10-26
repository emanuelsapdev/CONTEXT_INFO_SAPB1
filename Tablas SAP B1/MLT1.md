# MLT1 - Translations in user language

- **Tabla:** MLT1
- **Descripción:** Translations in user language
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MLT1.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TranEntry` | Key From Header Table | Int | 11 | - |  |  |
| 2 | `LangCode` | Language Code of User Language | Int | 11 | - |  |  |
| 3 | `Trans` | Translation Content | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TranEntry, LangCode |
