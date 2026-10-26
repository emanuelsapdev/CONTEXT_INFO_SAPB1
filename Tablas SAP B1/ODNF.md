# ODNF - DNF Code

- **Tabla:** ODNF
- **Descripción:** DNF Code
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODNF.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | - |  |  |
| 2 | `NCMEntry` | NCM Code | Int | 11 | [ONCM](ONCM.md) |  |  |
| 3 | `DNFCode` | DNF Code | nVarChar | 5 | - |  |  |
| 4 | `DNFUoM` | DNF UoM | nVarChar | 10 | - |  |  |
| 5 | `DNFFactor` | DNF Factor | Num | 19.6 | - |  |  |
| 6 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 7 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 8 | `UpdateDate` | Update Date | Date | 8 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| NCM_DNF | Yes | NCMEntry, DNFCode |
