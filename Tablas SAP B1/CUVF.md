# CUVF - User Validations

- **Tabla:** CUVF
- **Descripción:** User Validations
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CUVF.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IndexID` | Index | Int | 11 | [CUDV](CUDV.md) |  |  |
| 2 | `Value` | Field Value | nVarChar | 254 | - |  |  |
| 3 | `Key` | Field Key | nVarChar | 254 | - |  |  |
| 4 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 5 | `ValueText` | Value Text | nVarChar | 254 | - |  |  |
| 6 | `CreateTS` | Create Time | Int | 11 | - |  |  |
| 7 | `UpdateTS` | Update Time | Int | 11 | - |  |  |
| 8 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 9 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 10 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 11 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | IndexID, LineNum |
