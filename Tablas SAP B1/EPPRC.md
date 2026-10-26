# EPPRC - EPPRC

- **Tabla:** EPPRC
- **Descripción:** EPPRC
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/EPPRC.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PrcId` | Plugin processor id | nVarChar | 60 | - |  |  |
| 2 | `AsmName` | FK to EPASM table | nVarChar | 100 | - |  |  |
| 3 | `PrcType` | the type name of the processor | nVarChar | 160 | - |  |  |
| 4 | `OutSerName` | default service | nVarChar | 160 | - |  |  |
| 5 | `OutOprName` | default service operation | nVarChar | 60 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | PrcId |
