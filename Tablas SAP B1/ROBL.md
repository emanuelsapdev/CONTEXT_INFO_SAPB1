# ROBL - Resource Object I/E Log

- **Tabla:** ROBL
- **Descripción:** Resource Object I/E Log
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ROBL.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RobjKey` | Resource Object Key | Int | 11 | - |  |  |
| 2 | `Language` | Language | Int | 11 | - |  |  |
| 3 | `ImportDate` | Date Object Imported In Lang | Date | 8 | - |  |  |
| 4 | `ImportTime` | Time Imported | Int | 6 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RobjKey, Language |
