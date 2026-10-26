# AFML - Tax Formula Master Table

- **Tabla:** AFML
- **Descripción:** Tax Formula Master Table
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AFML.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | - |  |  |
| 2 | `Code` | Code | nVarChar | 20 | - |  |  |
| 3 | `Descr` | Description | nVarChar | 100 | - |  |  |
| 4 | `SttId` | Tax Type ID | Int | 11 | [OSTT](OSTT.md) |  |  |
| 5 | `FmlLang` | Formula Language Free Text | Text | 16 | - |  |  |
| 6 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 7 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 8 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 9 | `FmlType` | Formula Type | VarChar | 1 | - | T | `T` = Tax<br>`W` = WTax |
| 10 | `IsOrigFml` | Original/Edited Formula | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId, LogInstanc |
| CODE | Yes | FmlType, Code, LogInstanc |
