# ONCP - New Cockpit Table

- **Tabla:** ONCP
- **Descripción:** New Cockpit Table
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ONCP.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `Name` | Name | nVarChar | 100 | - |  |  |
| 3 | `Owner` | Owner | Int | 11 | [OUSR](OUSR.md) |  |  |
| 4 | `GroupId` | Group ID | Int | 11 | - |  |  |
| 5 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 6 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 7 | `IsPublic` | Public | VarChar | 1 | - | N | `Y`<br>`N` |
| 8 | `Pubby` | Published By | nVarChar | 30 | - |  |  |
| 9 | `PubDate` | Publication Date | Date | 8 | - |  |  |
| 10 | `Type` | Type | VarChar | 1 | - | T | `U` = User<br>`T` = Template |
| 11 | `Descr` | Description | nVarChar | 100 | - |  |  |
| 12 | `Date` | Publication Date | Date | 8 | - |  |  |
| 13 | `Time` | Publication Time | Int | 6 | - |  |  |
| 14 | `Mnfacturer` | Provider | nVarChar | 50 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| NAME | Yes | Name, Owner |
