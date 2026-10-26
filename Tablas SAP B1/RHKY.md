# RHKY - Hotkeys

- **Tabla:** RHKY
- **Descripción:** Hotkeys
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RHKY.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Language` | Language code | Int | 11 | - |  |  |
| 2 | `Num` | Hotkey Number | Int | 11 | - |  |  |
| 3 | `FormName` | Form name | nVarChar | 64 | - |  |  |
| 4 | `ItemNum` | Item number | Int | 11 | - |  |  |
| 5 | `HkeyIndex` | Hotkey Index in String | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Language, Num |
| ITEM | Yes | Language, FormName, ItemNum |
