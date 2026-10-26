# TPW5 - Challan Information

- **Tabla:** TPW5
- **Descripción:** Challan Information
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TPW5.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Absolute Entry No | Int | 11 | [OTPW](OTPW.md) |  |  |
| 2 | `ChlnDate` | Challan Date | Date | 8 | - |  |  |
| 3 | `ChlnNo` | Challan No | nVarChar | 50 | - |  |  |
| 4 | `ChlnBank` | Challan Bank | nVarChar | 100 | - |  |  |
| 5 | `ChlnMemo` | Challan Memo | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
