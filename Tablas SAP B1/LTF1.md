# LTF1 - Legal Text Format Lines

- **Tabla:** LTF1
- **Descripción:** Legal Text Format Lines
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/LTF1.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Format ID | Int | 11 | [OLTF](OLTF.md) |  |  |
| 2 | `LineNum` | Line No. | Int | 11 | - |  |  |
| 3 | `LineCode` | Format Code | nVarChar | 30 | [OLTI](OLTI.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
