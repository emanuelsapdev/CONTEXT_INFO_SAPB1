# CRD9 - OCRD Extension

- **Tabla:** CRD9
- **Descripción:** OCRD Extension
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CRD9.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CardCode` | BP Code | nVarChar | 25 | [OCRD](OCRD.md) |  |  |
| 2 | `ISTransMod` | Intrastat Transport Mode | Int | 11 | [ODCI](ODCI.md) |  |  |
| 3 | `ISIncoterm` | Intrastat Incoterms | Int | 11 | [ODCI](ODCI.md) |  |  |
| 4 | `ISState` | Intrastat State | Int | 11 | [ODCI](ODCI.md) |  |  |
| 5 | `ISNatTrans` | Intrastat Nature of Trans. | Int | 11 | [ODCI](ODCI.md) |  |  |
| 6 | `ISStatProc` | Intrastat Statistical Proc. | Int | 11 | [ODCI](ODCI.md) |  |  |
| 7 | `ISCustProc` | Intrastat Customs Proc. | Int | 11 | [ODCI](ODCI.md) |  |  |
| 8 | `ISCRYOrig` | Intrastat Country Origin | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 9 | `ISPort` | Intrastat Port of Entry/Exit | Int | 11 | [ODCI](ODCI.md) |  |  |
| 10 | `ISDomFrgld` | Intrastat Domestic/Foreign ID | VarChar | 1 | - |  |  |
| 11 | `ISRelevant` | Intrastat Relevant | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CardCode |
