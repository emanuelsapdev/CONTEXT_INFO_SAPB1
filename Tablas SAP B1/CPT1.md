# CPT1 - Cockpit Subtable

- **Tabla:** CPT1
- **Descripción:** Cockpit Subtable
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CPT1.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OCPT](OCPT.md) |  |  |
| 2 | `SubEntry` | Subnumber | Int | 11 | - |  |  |
| 3 | `_Title` | Show Title | nVarChar | 20 | - |  |  |
| 4 | `WdtEntry` | Widget Entry | Int | 11 | [OWDT](OWDT.md) |  |  |
| 5 | `_Left` | Left | Int | 6 | - |  |  |
| 6 | `_Right` | Right | Int | 6 | - |  |  |
| 7 | `_Top` | Top | Int | 6 | - |  |  |
| 8 | `_Bottom` | Bottom | Int | 6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, SubEntry |
