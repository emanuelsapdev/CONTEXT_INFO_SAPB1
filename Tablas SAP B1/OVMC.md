# OVMC - Value Mapping Communication Object

- **Tabla:** OVMC
- **Descripción:** Value Mapping Communication Object
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OVMC.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `SYS_ID` | Third Party System ID | Int | 11 | - |  |  |
| 3 | `ObjectId` | Object ID | Int | 11 | - |  |  |
| 4 | `Type` | Type | nVarChar | 2 | - | MD | `MD` = Master Data<br>`TR` = Transaction |
| 5 | `StartDate` | Start Date | Date | 8 | - |  |  |
| 6 | `StartTime` | Start Time | Int | 11 | - |  |  |
| 7 | `EndDate` | End Date | Date | 8 | - |  |  |
| 8 | `EndTime` | End Time | Int | 11 | - |  |  |
| 9 | `Message` | Message | Text | 16 | - |  |  |
| 10 | `Status` | Communication Status | VarChar | 1 | - | P | `P` = Pending<br>`E` = Error<br>`N` = New<br>`S` = Successful<br>`R` = Rejected |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
