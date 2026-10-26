# ACFP - CFOP for Nota Fiscal

- **Tabla:** ACFP
- **Descripción:** CFOP for Nota Fiscal
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ACFP.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ID` | CFOP ID | Int | 11 | - |  |  |
| 2 | `Code` | CFOP Code | nVarChar | 6 | - |  |  |
| 3 | `Descrip` | Description | Text | 16 | - |  |  |
| 4 | `App` | Application | Text | 16 | - |  |  |
| 5 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Auto Incr.<br>`D` = Data Doc.<br>`P` = Partner Implementation |
| 7 | `UserSign` | User Signature | nVarChar | 6 | [OUSR](OUSR.md) |  |  |
| 8 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |
| 9 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 10 | `UpdateDate` | Update Date | Date | 8 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ID, LogInstanc |
| CFOP_CODE | Yes | Code, LogInstanc |
