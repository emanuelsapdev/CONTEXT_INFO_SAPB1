# OAT3 - Item Details: Activity

- **Tabla:** OAT3
- **Descripción:** Item Details: Activity
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OAT3.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AgrNo` | Agreement No. | Int | 11 | [OOAT](OOAT.md) |  |  |
| 2 | `AgrLnNum` | Agreement Line Number | Int | 11 | - |  |  |
| 3 | `AgrEfctNum` | Line Number | Int | 11 | - |  |  |
| 4 | `ActivityID` | Activity ID | Int | 11 | [OCLG](OCLG.md) |  |  |
| 5 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AgrNo, AgrLnNum, AgrEfctNum, ActivityID |
