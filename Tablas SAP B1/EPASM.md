# EPASM - EPASM

- **Tabla:** EPASM
- **Descripción:** EPASM
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/EPASM.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AsmName` | plugin assembly name | nVarChar | 100 | - |  |  |
| 2 | `PkgName` | FK to the EPPKG table | nVarChar | 50 | - |  |  |
| 3 | `AsmType` | Ttypes contained in assembly | nVarChar | 20 | - | All | `Messages` = Only IMessage contained in the assembly<br>`Processors` = Only IMessageProcessor contained in the assembly<br>`All` = All types are in the assembly |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AsmName |
