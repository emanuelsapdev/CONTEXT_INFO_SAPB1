# BoExpenseOperationTypeEnum — Tipo de operación de gastos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoExpenseOperationTypeEnum`
- **Descripción (ES):** Tipo de operación de gastos
- **Underlying type:** Edm.Int32
- **Members:** 8

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bo_ExpOpType_ProfessionalServices` | 0 | Exp Op Type Professional Services | Servicios profesionales |
| `bo_ExpOpType_RentingAssets` | 1 | Exp Op Type Renting Assets | Alquiler de bienes |
| `bo_ExpOpType_Others` | 2 | Exp Op Type Others | Otros |
| `bo_ExpOpType_None` | 3 | Exp Op Type None | Ninguno |
| `bo_ExpOpType_DisposalOfGoods` | 4 | Exp Op Type Disposal Of Goods | Enajenación de bienes |
| `bo_ExpOpType_ImportOfGoodsAndServices` | 5 | Exp Op Type Import Of Goods And Services | Importación de bienes y servicios |
| `bo_ExpOpType_ImportByVirtualTransfer` | 6 | Exp Op Type Import By Virtual Transfer | Importación por transferencia virtual |
| `bo_ExpOpType_GlobalOperations` | 7 | Exp Op Type Global Operations | Operaciones globales |

## Used by (1 properties)

- [DocumentLine](../Tipos-Complejos/DocumentLine.md).`ExpenseOperationType`
