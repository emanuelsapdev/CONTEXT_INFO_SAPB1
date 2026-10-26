# IMT1 - Acct data in selected template

- **Tabla:** IMT1
- **Descripción:** Acct data in selected template
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/IMT1.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TemplateId` | Template ID | Int | 6 | [OIMT](OIMT.md) | -1 |  |
| 2 | `AccountId` | Account ID | Int | 6 | - | -1 |  |
| 3 | `DebitCredi` | Debit or Credit | VarChar | 1 | - | U | `U` = Unknown<br>`D` = DEBIT<br>`C` = CREDIT<br>`B` = Both<br>`T` = Total |
| 4 | `OrderCalc` | Order Calc | Int | 6 | - | -1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TemplateId, AccountId |
