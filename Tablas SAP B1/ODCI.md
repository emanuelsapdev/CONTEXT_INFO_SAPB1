# ODCI - Intrastat Configuration

- **Tabla:** ODCI
- **Descripción:** Intrastat Configuration
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODCI.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Configuration Entry ID | Int | 11 | - |  |  |
| 2 | `ConfType` | Configuration Type | VarChar | 1 | - |  | `M` = Additional Measurement Unit<br>`C` = Commodity Codes<br>`P` = Custom Procedures<br>`I` = Incoterms<br>`N` = Nature of Transactions<br>`E` = Ports of Entry and Exit<br>`R` = Service Codes<br>`S` = Statistical Procedures<br>`T` = Transport Modes<br>`G` = Regions |
| 3 | `Code` | Code | nVarChar | 50 | - |  |  |
| 4 | `Descr` | Description | nVarChar | 254 | - |  |  |
| 5 | `PrcstVal` | Percentage Value | Num | 19.6 | - |  |  |
| 6 | `SuppUnit` | Supplementary Unit | Int | 11 | [ODCI](ODCI.md) |  |  |
| 7 | `Export` | Valid for Export | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 8 | `Import` | Valid for Import | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 9 | `StatCode` | Statistical Code | nVarChar | 2 | - |  |  |
| 10 | `DateFrom` | Valid From | Date | 8 | - |  |  |
| 11 | `DateTo` | Valid To | Date | 8 | - |  |  |
| 12 | `TextVal` | Text Value | nVarChar | 12 | - |  |  |
| 13 | `ConfID` | Configuration ID | nVarChar | 254 | - |  |  |
| 14 | `TriangDeal` | Triangular Deal Type | nVarChar | 2 | - |  | `11` = Acquisitions intra-communautaires<br>`21` = Livraison exon�r�e<br>`31` = Facturations dans le cadre d�op�rations triangulaires |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| CONF_ID | No | ConfID |
