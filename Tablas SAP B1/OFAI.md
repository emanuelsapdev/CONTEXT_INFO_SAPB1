# OFAI - Microsoft 365 Application Identity

- **Tabla:** OFAI
- **Descripción:** Microsoft 365 Application Identity
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OFAI.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ID` | ID | nVarChar | 254 | - |  |  |
| 2 | `APP_ID` | Microsoft 365 Application ID | nVarChar | 254 | - |  |  |
| 3 | `APP_PASS` | Microsoft 365 Application Secret | nVarChar | 254 | - |  |  |
| 4 | `SUP_ACCT` | Supported Account Type | VarChar | 1 | - | A | `S` = Single Tenant<br>`M` = Multiple Tenant<br>`A` = Multiple Tenant and Personal Account<br>`P` = Personal Account Only |
| 5 | `TENANT_ID` | Microsoft 365 Tenant ID | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ID |
