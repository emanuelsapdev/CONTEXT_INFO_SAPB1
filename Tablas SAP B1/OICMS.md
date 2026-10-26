# OICMS - Unencumbered ICMS Exemption Reason

- **Tabla:** OICMS
- **Descripción:** Unencumbered ICMS Exemption Reason
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OICMS.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ID` | ICMS Internal Key | Int | 11 | - |  |  |
| 2 | `CstSuffix` | CST Suffix for ICMS | nVarChar | 2 | - |  |  |
| 3 | `MotDes` | motDesICMS | Int | 11 | - | 0 |  |
| 4 | `Descrip` | Description | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ID |
