# TAAS - Result of TaaS Tax Code Check

- **Tabla:** TAAS
- **Descripción:** Result of TaaS Tax Code Check
- **Cantidad de campos:** 21
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TAAS.html

## Campos (21)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Internal` | Internal Number | Int | 11 | - |  |  |
| 2 | `TaxObjType` | Tax Object Type | nVarChar | 20 | - |  |  |
| 3 | `TaxAbsEntr` | Tax Abs Entry | Int | 11 | - |  |  |
| 4 | `LineSeq` | Row Sequence | Int | 11 | - |  |  |
| 5 | `DocObjType` | Doc. Object Type | nVarChar | 20 | - |  |  |
| 6 | `InvDocEntr` | InvDocEntry | Int | 11 | - |  |  |
| 7 | `DocDate` | Doc. Date | Date | 8 | - |  |  |
| 8 | `SrcArrType` | Source Array Type | Int | 11 | - |  |  |
| 9 | `SrcLineNum` | Source Row Number | Int | 11 | - | -1 |  |
| 10 | `TaxCode` | Tax Code | nVarChar | 8 | - |  |  |
| 11 | `StaCode` | Tax Authorities Code | nVarChar | 8 | - |  |  |
| 12 | `StaType` | Tax Authorities Type | Int | 11 | - |  |  |
| 13 | `IsOK` | Is OK | VarChar | 1 | - |  |  |
| 14 | `ErrorType` | Error Type | VarChar | 1 | - |  |  |
| 15 | `ErrorDescr` | Error Description | nVarChar | 254 | - |  |  |
| 16 | `IsLiable` | Is Tax Liable | VarChar | 1 | - |  |  |
| 17 | `BaseSum` | Base Sum | Num | 19.6 | - |  |  |
| 18 | `Tax1Rate` | TAX1 Rate | Num | 19.6 | - |  |  |
| 19 | `TaasRate` | TaaS Rate | Num | 19.6 | - |  |  |
| 20 | `Tax1VatSum` | Tax1 VAT Sum | Num | 19.6 | - |  |  |
| 21 | `TaasVatSum` | TaaS VAT Sum | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| DUMMY | Yes | Internal |
