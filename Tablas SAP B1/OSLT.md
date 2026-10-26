# OSLT - Service Call Solutions

- **Tabla:** OSLT
- **Descripción:** Service Call Solutions
- **Cantidad de campos:** 17
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSLT.html

## Campos (17)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SltCode` | Solution Code | Int | 11 | - |  |  |
| 2 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 3 | `StatusNum` | Status | Int | 11 | [OSST](OSST.md) |  |  |
| 4 | `Owner` | Owner | Int | 11 | [OUSR](OUSR.md) |  |  |
| 5 | `CreatedBy` | Created By | Int | 11 | [OUSR](OUSR.md) |  |  |
| 6 | `DateCreate` | Creation Date | Date | 8 | - |  |  |
| 7 | `UpdateBy` | Last Update by | Int | 11 | [OUSR](OUSR.md) |  |  |
| 8 | `DateUpdate` | Last Update Date | Date | 8 | - |  |  |
| 9 | `Subject` | Subject | nVarChar | 254 | - |  |  |
| 10 | `Symptom` | Symptom | nVarChar | 254 | - |  |  |
| 11 | `Cause` | Cause | nVarChar | 254 | - |  |  |
| 12 | `Descriptio` | Description | Text | 16 | - |  |  |
| 13 | `Attachment` | Attachments | Text | 16 | - |  |  |
| 14 | `AtcEntry` | Attachment Entry | Int | 11 | - |  |  |
| 15 | `Transfered` | Year Transfer | VarChar | 1 | - | N |  |
| 16 | `Instance` | Instance | Int | 6 | - | 0 |  |
| 17 | `DataVers` | Data Version | Int | 11 | - | 1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SltCode |
