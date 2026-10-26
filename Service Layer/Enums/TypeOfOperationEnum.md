# TypeOfOperationEnum — Tipo de operación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `TypeOfOperationEnum`
- **Descripción (ES):** Tipo de operación
- **Underlying type:** Edm.Int32
- **Members:** 7

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `tooProfessionalServices` | 1 | Professional Services | Servicios profesionales |
| `tooRentingAssets` | 2 | Renting Assets | Alquiler de bienes |
| `tooOthers` | 3 | Others | Otros |
| `tooDisposalOfGoods` | 4 | Disposal Of Goods | Enajenación de bienes |
| `tooImportOfGoodsAndServices` | 5 | Import Of Goods And Services | Importación de bienes y servicios |
| `tooImportByVirtualTransfer` | 6 | Import By Virtual Transfer | Importación por transferencia virtual |
| `tooGlobalOperations` | 7 | Global Operations | Operaciones globales |

## Used by (1 properties)

- [BusinessPartner](../Entidades/BusinessPartners.md).`TypeOfOperation`
