# OPDT - Predefined Text

- **Tabla:** OPDT
- **Descripción:** Predefined Text
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPDT.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `TextCode` | Text Code | nVarChar | 20 | - |  |  |
| 3 | `Text` | TEXT | Text | 16 | - |  |  |
| 4 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 5 | `CreateDate` | Date Created | Date | 8 | - |  |  |
| 6 | `CreateTS` | Create Time - Incl. Secs | Int | 11 | - |  |  |
| 7 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 8 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 9 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 10 | `UserSign2` | Updating User | Int | 6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| CODE | Yes | TextCode |
