# SWRS - SWRS

- **Tabla:** SWRS
- **Descripción:** SWRS
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SWRS.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ResourceID` | Workflow Resource ID | Identity | 11 | - |  |  |
| 2 | `Name` | Workflow Resouce Name | nVarChar | 254 | - |  |  |
| 3 | `Version` | Resource Version | nVarChar | 13 | - |  |  |
| 4 | `DeploymtID` | Deployment ID | Int | 11 | [SWDP](SWDP.md) |  |  |
| 5 | `Bytes` | Resource Library | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ResourceID |
