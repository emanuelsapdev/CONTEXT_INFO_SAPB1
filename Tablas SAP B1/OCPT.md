# OCPT - Cockpit Main Table

- **Tabla:** OCPT
- **Descripción:** Cockpit Main Table
- **Cantidad de campos:** 18
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCPT.html

## Campos (18)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `Code` | Cockpit Code | Int | 6 | - |  |  |
| 3 | `Name` | Name | nVarChar | 20 | - |  |  |
| 4 | `Descr` | Description | nVarChar | 100 | - |  |  |
| 5 | `IsDefault` | Is Default | VarChar | 1 | - | N | `Y`<br>`N` |
| 6 | `UserSign` | User ID | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `IsPublic` | Public | VarChar | 1 | - | N | `Y`<br>`N` |
| 8 | `Strategy` | Layout Strategy | nVarChar | 20 | - |  |  |
| 9 | `_Top` | Client Top | Int | 11 | - |  |  |
| 10 | `_Left` | Client Left | Int | 11 | - |  |  |
| 11 | `_Width` | Client Width | Int | 11 | - |  |  |
| 12 | `_Height` | Client Height | Int | 11 | - |  |  |
| 13 | `Date` | Publication Date | Date | 8 | - |  |  |
| 14 | `Time` | Publication Time | Int | 6 | - |  |  |
| 15 | `Mnfacturer` | Provider | nVarChar | 50 | - |  |  |
| 16 | `Pubby` | Published By | nVarChar | 30 | - |  |  |
| 17 | `Disabled` | Disabled | VarChar | 1 | - | N | `Y`<br>`N` |
| 18 | `Type` | Type | VarChar | 1 | - | U | `U` = User<br>`T` = Template |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| CODE | Yes | Code, UserSign |
| NAME | Yes | Name, UserSign |
