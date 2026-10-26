# OCCD - Cargo Customs Declaration Numbers

- **Tabla:** OCCD
- **Descripción:** Cargo Customs Declaration Numbers
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCCD.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CCDNum` | CCD Number | nVarChar | 40 | - |  |  |
| 2 | `Date` | Date | Date | 8 | - |  |  |
| 3 | `CustBroker` | Customs Broker | nVarChar | 15 | - |  |  |
| 4 | `DocNum` | Imp./Exp. Document Number | nVarChar | 20 | - |  |  |
| 5 | `DocDate` | Imp./Exp. Document Date | Date | 8 | - |  |  |
| 6 | `SupNum` | Supply Agreement Number | nVarChar | 20 | - |  |  |
| 7 | `SupDate` | Supply Agreement Date | Date | 8 | - |  |  |
| 8 | `CustTerm` | Customs Terminal | nVarChar | 15 | - |  |  |
| 9 | `PayKey` | Payment Internal ID | nVarChar | 4 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CCDNum |
