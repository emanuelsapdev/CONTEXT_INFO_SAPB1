# TPL1 - Template - Records

- **Tabla:** TPL1
- **Descripción:** Template - Records
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TPL1.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TplNum` | Template Code | Int | 11 | [OTPL](OTPL.md) |  |  |
| 2 | `LineNum` | Line No. | Int | 11 | - |  |  |
| 3 | `FieldPos` | Field Pos. | Int | 11 | - |  |  |
| 4 | `SrcArrType` | Source Array Type | Int | 11 | - | 1 | `-1` = None<br>`1` = Main<br>`12` = Array 1<br>`13` = Array 2<br>`14` = Array 3<br>`15` = Array 4<br>`16` = Array 5<br>`17` = Array 6<br>`18` = Array 7<br>`19` = Array 8<br>`20` = Array 9<br>`21` = Array 10<br>`22` = Array 11 |
| 5 | `SrcObjType` | Source Object Type | Int | 11 | - | -1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TplNum, LineNum |
