# PCI1 - Process Checklist Element Extended Data

- **Tabla:** PCI1
- **Descripción:** Process Checklist Element Extended Data
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PCI1.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `InstancePk` | Instance Primary Key | Int | 11 | [OPCI](OPCI.md) |  |  |
| 2 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 3 | `BPMNElId` | BPMN Model Element ID | nVarChar | 254 | - |  |  |
| 4 | `BPMNElDes` | BPMN Model Element Description | nVarChar | 254 | - |  |  |
| 5 | `ParamType` | Parameter Type | nVarChar | 254 | - |  |  |
| 6 | `ParamKey` | Parameter Key | nVarChar | 254 | - |  |  |
| 7 | `ParamVal` | Parameter Value | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | InstancePk, LineNum |
