# SWPD - SWPD

- **Tabla:** SWPD
- **Descripción:** SWPD
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SWPD.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ProcDefID` | WF process definition ID | Identity | 11 | - |  |  |
| 2 | `DeploymtID` | Deployment ID | Int | 11 | [SWDP](SWDP.md) |  |  |
| 3 | `ResourceID` | Resource ID | Int | 11 | [SWRS](SWRS.md) |  |  |
| 4 | `Key` | WF process definition key | nVarChar | 254 | - |  |  |
| 5 | `Name` | WF process definition name | nVarChar | 254 | - |  |  |
| 6 | `Desc` | WF process definition | Text | 16 | - |  |  |
| 7 | `Category` | WF category uri | nVarChar | 50 | - |  |  |
| 8 | `Version` | WF process definition version | nVarChar | 13 | - |  |  |
| 9 | `ProcType` | Process definition type | nVarChar | 20 | - |  |  |
| 10 | `Status` | Status during import | VarChar | 1 | - | M | `M` = Importing<br>`P` = Imported<br>`F` = Import failed<br>`I` = Inactive<br>`A` = Active<br>`E` = Activate failed<br>`D` = Deleted |
| 11 | `StartType` | Start Type | VarChar | 1 | - | M | `M` = Manual Start<br>`T` = Timer Start<br>`C` = Conditional Start |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ProcDefID |
