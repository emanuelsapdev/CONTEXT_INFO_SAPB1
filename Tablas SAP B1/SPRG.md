# SPRG - Application Start

- **Tabla:** SPRG
- **Descripción:** Application Start
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SPRG.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 2 | `UserCode` | User Code | nVarChar | 25 | - | -1 |  |
| 3 | `Name` | Application Name | nVarChar | 128 | - |  |  |
| 4 | `FileName` | File Name | nVarChar | 254 | - |  |  |
| 5 | `Path` | Application Route | Text | 16 | - |  |  |
| 6 | `Params` | Application Parameters | Text | 16 | - |  |  |
| 7 | `OPRTION` | Operation Method | nVarChar | 50 | - | open | `open` = Open<br>`edit` = Edit<br>`explore` = Find Folder<br>`find` = Find File<br>`print` = Print<br>`properties` = Properties |
| 8 | `WIN_STYLE` | Windows Type | nVarChar | 2 | - | 1 | `0` = Hide<br>`1` = Standard<br>`3` = Enlarge<br>`5` = Operate as Previous<br>`6` = Reduce<br>`9` = Restore |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | LineNum, UserCode |
