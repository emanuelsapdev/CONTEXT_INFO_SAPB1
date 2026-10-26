# UFRM - UFRM

- **Tabla:** UFRM
- **Descripción:** UFRM
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UFRM.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `guid` | Guid | nVarChar | 36 | - |  |  |
| 2 | `fatherId` | Father Id | nVarChar | 36 | - |  |  |
| 3 | `formName` | Form Name | nVarChar | 254 | - |  |  |
| 4 | `objId` | Object Id | nVarChar | 36 | - |  |  |
| 5 | `frmNameSid` | Form Name String Index | Int | 11 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | guid |
| FATHER_ID | No | fatherId |
| OBJECT_ID | Yes | objId |
