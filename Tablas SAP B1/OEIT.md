# OEIT - E-Books Invoice Type

- **Tabla:** OEIT
- **Descripción:** E-Books Invoice Type
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OEIT.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Unique Entry | Int | 11 | - |  |  |
| 2 | `Code` | Code | nVarChar | 50 | - |  |  |
| 3 | `Descr` | Description | nVarChar | 254 | - |  |  |
| 4 | `Issuer` | Issuer | VarChar | 1 | - | I | `I` = Included<br>`E` = Excluded |
| 5 | `IssuerBrch` | Branch of Issuer | VarChar | 1 | - | I | `I` = Included<br>`E` = Excluded<br>`Z` = Zero |
| 6 | `Cnterpart` | Counterpart | VarChar | 1 | - | I | `I` = Included<br>`E` = Excluded |
| 7 | `VAT` | VAT | VarChar | 1 | - | I | `I` = Included<br>`E` = Excluded |
| 8 | `PaymtMthod` | Payment Method | VarChar | 1 | - | I | `I` = Included<br>`E` = Excluded |
| 9 | `SubmitedBy` | Submitted By | VarChar | 1 | - | C | `C` = Company<br>`A` = Accountant |
| 10 | `SelfPrice` | Self-Pricing | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| CODE | Yes | Code |
