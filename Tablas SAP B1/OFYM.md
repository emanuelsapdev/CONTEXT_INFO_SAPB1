# OFYM - Financial Year Master

- **Tabla:** OFYM
- **Descripción:** Financial Year Master
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OFYM.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | - |  |  |
| 2 | `Code` | Code | nVarChar | 6 | - |  |  |
| 3 | `Descr` | Description | nVarChar | 30 | - |  |  |
| 4 | `StartDate` | Start Date | Date | 8 | - |  |  |
| 5 | `EndDate` | End Date | Date | 8 | - |  |  |
| 6 | `AssessYear` | Assessment Year | nVarChar | 6 | - |  |  |
| 7 | `TcsAcmBase` | TCS Accumulation Base | VarChar | 1 | - | I | `I` = Accumulation Based on Invoice<br>`P` = Accumulation Based on Payment |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
| CODE | Yes | Code |
| ASSESSYEAR | Yes | AssessYear |
