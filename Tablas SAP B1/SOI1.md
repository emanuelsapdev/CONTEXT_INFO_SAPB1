# SOI1 - Statement of Import - Business Partners

- **Tabla:** SOI1
- **Descripción:** Statement of Import - Business Partners
- **Cantidad de campos:** 2
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SOI1.html

## Campos (2)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WizardId` | Wizard ID | Int | 11 | [OSOI](OSOI.md) |  |  |
| 2 | `CardCode` | BP Card Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WizardId, CardCode |
