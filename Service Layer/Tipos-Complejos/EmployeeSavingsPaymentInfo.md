# EmployeeSavingsPaymentInfo — Pago de ahorro del empleado

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EmployeeSavingsPaymentInfo`
- **Descripción (ES):** Pago de ahorro del empleado
- **Description (EN):** Employee Savings Payment Information
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 12

## Properties (12)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `EmployeeID` | Edm.Int32 | Yes | Employee ID | ID de empleado |
| 2 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `ContractName` | Edm.String | Yes | Contract Name | Nombre del contrato |
| 4 | `PaymentNotes` | Edm.String | Yes | Payment Notes | Notas del pago |
| 5 | `AN` | Edm.Double | Yes | AN | Código AN |
| 6 | `ANcurrency` | Edm.String | Yes | A Ncurrency | Moneda AN |
| 7 | `AG` | Edm.Double | Yes | AG | Código AG |
| 8 | `AGcurrency` | Edm.String | Yes | A Gcurrency | Moneda AG |
| 9 | `BankName` | Edm.String | Yes | Bank Name | Nombre del banco |
| 10 | `BankCode` | Edm.String | Yes | Bank Code | Código del banco |
| 11 | `BankAccount` | Edm.String | Yes | Bank Account | Cuenta bancaria |
| 12 | `Sequence` | [ContractSequenceEnum](../Enums/ContractSequenceEnum.md) | Yes | Sequence | Secuencia |

## Used by (properties)

- [EmployeeInfo](../Entidades/EmployeesInfo.md).`EmployeeSavingsPaymentInfoLines`
