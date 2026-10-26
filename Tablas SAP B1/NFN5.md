# NFN5 - NF Skipped Numbers

- **Tabla:** NFN5
- **Descripción:** NF Skipped Numbers
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/NFN5.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SeqCode` | Sequence Code | Int | 6 | - |  |  |
| 2 | `NFeNoFrom` | NF-e No. From | Int | 11 | - | 0 |  |
| 3 | `NFeNoTo` | NF-e No. To | Int | 11 | - | 0 |  |
| 4 | `Year` | Year | Int | 6 | - |  |  |
| 5 | `Reason` | Reason for Number Skipping | nVarChar | 254 | - |  |  |
| 6 | `Reply` | Reply from the Authority | nVarChar | 50 | - |  |  |
| 7 | `Status` | Status | VarChar | 1 | - | N | `N` = New<br>`S` = Sent<br>`A` = Approved<br>`E` = Error |
| 8 | `VisOrder` | Visual Order | Int | 6 | - |  |  |
| 9 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 10 | `CreateTime` | Creation Time | Int | 11 | - |  |  |
| 11 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 12 | `UpdateTime` | Update Time | Int | 11 | - |  |  |
| 13 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 14 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SeqCode, VisOrder |
