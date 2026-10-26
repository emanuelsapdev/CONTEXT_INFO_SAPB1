# AADP2 - Report Settings - History

- **Tabla:** AADP2
- **Descripción:** Report Settings - History
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AADP2.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PrintId` | Print No. | nVarChar | 4 | [OADP](OADP.md) |  |  |
| 2 | `RptType` | Report Type | nVarChar | 20 | - |  | `1` = Aging Report<br>`2` = Dunning Wizard |
| 3 | `EmailSbj` | E-Mail Subject | nVarChar | 254 | - |  |  |
| 4 | `EmailBody` | Email Body | Text | 16 | - |  |  |
| 5 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | PrintId, RptType, LogInstanc |
