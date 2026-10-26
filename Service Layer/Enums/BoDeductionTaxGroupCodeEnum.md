# BoDeductionTaxGroupCodeEnum — Código de grupo de deducción de retenciones (Israel)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoDeductionTaxGroupCodeEnum`
- **Descripción (ES):** Código de grupo de deducción de retenciones (Israel)
- **Underlying type:** Edm.Int32
- **Members:** 11

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `dtgcInterestReceivers` | 1 | Interest Receivers | Receptores de intereses |
| `dtgcEmployeeReceivingCommission` | 2 | Employee Receiving Commission | Empleado que recibe comisión |
| `dtgcWritersPrice` | 3 | Writers Price | Pago a escritores |
| `dtgcPaidServices` | 6 | Paid Services | Servicios pagados |
| `dtgcPaymentsToForeignCitizens` | 7 | Payments To Foreign Citizens | Pagos a ciudadanos extranjeros |
| `dtgcPaymentsForCitizensInForeignCountries` | 8 | Payments For Citizens In Foreign Countries | Pagos a ciudadanos en el exterior |
| `dtgcInvalidPaymentFromCompensationFund` | 11 | Invalid Payment From Compensation Fund | Pago inválido del fondo de compensación |
| `dtgcRepaymentToEmployerFromCompensationFund` | 12 | Repayment To Employer From Compensation Fund | Reintegro al empleador del fondo de compensación |
| `dtgcRentalPayments` | 13 | Rental Payments | Pagos de alquiler |
| `dtgcPaymentsFromStudyFund` | 14 | Payments From Study Fund | Pagos del fondo de estudios |
| `dtgcDividendPayments` | 18 | Dividend Payments | Pagos de dividendos |

## Used by (1 properties)

- [DeductionTaxGroup](../Entidades/DeductionTaxGroups.md).`GroupCode`
