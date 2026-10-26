# OMDC - Master Data Cleanup

- **Tabla:** OMDC
- **Descripción:** Master Data Cleanup
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OMDC.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | - |  |  |
| 2 | `Name` | Master Data Cleanup Name | nVarChar | 100 | - |  |  |
| 3 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 4 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 5 | `Status` | Status | VarChar | 1 | - |  | `S` = Saved<br>`E` = Executed |
| 6 | `UpdUser` | Last Update User | nVarChar | 30 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
