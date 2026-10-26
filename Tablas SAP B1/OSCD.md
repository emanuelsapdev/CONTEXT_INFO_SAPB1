# OSCD - Service Code Table

- **Tabla:** OSCD
- **Descripción:** Service Code Table
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSCD.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | ID | Int | 11 | - |  |  |
| 2 | `County` | County Code | Int | 11 | [OCNT](OCNT.md) |  |  |
| 3 | `ServiceCD` | Service Code | nVarChar | 15 | - |  |  |
| 4 | `Descrip` | Description | nVarChar | 70 | - |  |  |
| 5 | `Incomimg` | Is Incomimg(Y/N) | VarChar | 1 | - | Y | `Y` = Incoming<br>`N` = Outgoing |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| CODE | Yes | County, ServiceCD |
