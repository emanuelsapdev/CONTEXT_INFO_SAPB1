# OPOS - POS Master Data

- **Tabla:** OPOS
- **Descripción:** POS Master Data
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPOS.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `EquipNo` | Equipment No. | nVarChar | 20 | - |  |  |
| 2 | `Model` | Model | nVarChar | 20 | - |  |  |
| 3 | `ManufSN` | Manufacturer Serial No. | nVarChar | 21 | - |  |  |
| 4 | `RegNo` | Register No. | Int | 6 | - |  |  |
| 5 | `NFModel` | Fiscal Document Model | nVarChar | 6 | [ONFM](ONFM.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | EquipNo |
