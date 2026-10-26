# OCLC - Change Logs Cleanup

- **Tabla:** OCLC
- **Descripción:** Change Logs Cleanup
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCLC.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `ClnpScn` | Cleanup Scenario Name | nVarChar | 100 | - |  |  |
| 3 | `ClnpDate` | Cleanup Date | Date | 8 | - |  |  |
| 4 | `UpTo` | Clean Up Logs Until | Date | 8 | - |  |  |
| 5 | `Rmrks` | Remarks | nVarChar | 254 | - |  |  |
| 6 | `CreateTS` | Create Time - Incl. Secs | Int | 11 | - |  |  |
| 7 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
