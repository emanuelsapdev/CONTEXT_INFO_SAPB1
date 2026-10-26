# ABOC - External Bank Operation Code - Log

- **Tabla:** ABOC
- **Descripción:** External Bank Operation Code - Log
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ABOC.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `OpCodeCat` | Operation Code Category | nVarChar | 30 | - |  |  |
| 3 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 4 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 5 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LogInstanc |
