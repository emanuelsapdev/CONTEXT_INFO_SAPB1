# FAM1 - Fixed Asset Data Migration - Rows

- **Tabla:** FAM1
- **Descripción:** Fixed Asset Data Migration - Rows
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/FAM1.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WizardId` | Wizard ID | Int | 11 | [OFAM](OFAM.md) |  |  |
| 2 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 3 | `ObjectType` | Object Type | nVarChar | 20 | - |  | `1470000002` = Account Determination<br>`1470000003` = Depreciation Areas<br>`1470000004` = Depreciation Type Pools<br>`1470000000` = Depreciation Types<br>`1470000032` = Asset Classes<br>`4` = Items<br>`35` = Item Numbering |
| 4 | `ObjectCode` | Object Code | nVarChar | 20 | - |  |  |
| 5 | `ObjectName` | Object Name | nVarChar | 100 | - |  |  |
| 6 | `Status` | Status | VarChar | 1 | - | Y | `Y` = Successful<br>`N` = Failed |
| 7 | `Message` | Message | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WizardId, LineNum |
