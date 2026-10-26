# IMT11 - Calculated expression's constituent with sign for specifying account in specific template

- **Tabla:** IMT11
- **Descripción:** Calculated expression's constituent with sign for specifying account in specific template
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/IMT11.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TemplateId` | Template ID | Int | 6 | [IMT1](IMT1.md) | -1 |  |
| 2 | `AccountId` | Account ID | Int | 6 | [IMT1](IMT1.md) | -1 |  |
| 3 | `Sign` | Sing of the constituent | VarChar | 1 | - | A | `A` = Add<br>`S` = Sub |
| 4 | `PoSt_ID` | Id into Post Structure | Int | 6 | - | -1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TemplateId, AccountId, PoSt_ID |
