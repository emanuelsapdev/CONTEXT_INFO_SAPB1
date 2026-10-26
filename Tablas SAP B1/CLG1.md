# CLG1 - Activity CheckIns

- **Tabla:** CLG1
- **Descripción:** Activity CheckIns
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CLG1.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ClgCode` | Activity Number | Int | 11 | [OCLG](OCLG.md) |  |  |
| 2 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 3 | `Date` | Date | Date | 8 | - |  |  |
| 4 | `Location` | Location | nVarChar | 254 | - |  |  |
| 5 | `Latitude` | Latitude | nVarChar | 13 | - |  |  |
| 6 | `Longitude` | Longitude | nVarChar | 14 | - |  |  |
| 7 | `Time` | Time | Int | 11 | - |  |  |
| 8 | `OwnerUser` | Owner User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 9 | `OwnerEmp` | Owner Employee | Int | 11 | [OHEM](OHEM.md) |  |  |
| 10 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 11 | `SendAs` | Send As | VarChar | 1 | - | 0 | `0` = To<br>`1` = Cc<br>`2` = Bcc |
| 12 | `RecpntType` | Recipient Type | VarChar | 1 | - | 0 | `0` = User<br>`1` = Employee<br>`2` = Contact Person<br>`3` = Distribution List<br>`4` = Other |
| 13 | `RecpntName` | Recipient Name | nVarChar | 50 | [OUSR](OUSR.md) |  |  |
| 14 | `EmailAddr` | Email Address | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ClgCode, LineNum |
