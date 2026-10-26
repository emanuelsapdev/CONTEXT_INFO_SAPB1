# OSHR - Shareholder's Rights and Interests Report History

- **Tabla:** OSHR
- **Descripción:** Shareholder's Rights and Interests Report History
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSHR.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Id` | Identity | Int | 11 | - |  |  |
| 2 | `Name` | Report Name | nVarChar | 40 | - |  |  |
| 3 | `UserSign` | Creater's code | Int | 6 | - |  |  |
| 4 | `UserName` | Name of Creator | nVarChar | 20 | - |  |  |
| 5 | `CreateDate` | Report Created On | Date | 8 | - |  |  |
| 6 | `StartDate` | Date Range Start | Date | 8 | - |  |  |
| 7 | `EndDate` | Date Range End | Date | 8 | - |  |  |
| 8 | `TemplateId` | Template ID | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Id |
