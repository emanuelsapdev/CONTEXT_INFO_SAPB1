# OWHL - Register of VAT Payers

- **Tabla:** OWHL
- **Descripción:** Register of VAT Payers
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWHL.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ImportDate` | Import Date | Date | 8 | - |  |  |
| 2 | `HashCount` | Hash Count | Int | 11 | - |  |  |
| 3 | `Comment` | Comments | nVarChar | 254 | - |  |  |
| 4 | `NextDate` | Next Date | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ImportDate |
