# WHL3 - Register of VAT Payers - BPs Compared with OWHL

- **Tabla:** WHL3
- **Descripción:** Register of VAT Payers - BPs Compared with OWHL
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WHL3.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `LastDate` | Last Date | Date | 8 | - |  |  |
| 2 | `CardCode` | BP Code | nVarChar | 15 | - |  |  |
| 3 | `NIP` | Federal Tax ID | nVarChar | 32 | - |  |  |
| 4 | `BankAcc` | Bank Account | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CardCode, NIP, BankAcc |
