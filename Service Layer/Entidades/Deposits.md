# Deposits — Depósitos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `Deposits`
- **Descripción (ES):** Depósitos
- **Entity type:** `Deposit` (open type: accepts dynamic/UDF properties)
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** [ODPS](../../Tablas%20SAP%20B1/ODPS.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 48 · **Navigation properties:** 5 · **Bound actions:** 2

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/Deposits?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/Deposits/$count` | Contar |
| Get by key | `GET /b1s/v2/Deposits(1)` | Obtener por clave |
| Create | `POST /b1s/v2/Deposits` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/Deposits(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/Deposits(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/Deposits(1)` (only if the B1 object allows removal) | Borrar |
| Action `CancelDeposit` | `POST /b1s/v2/Deposits(1)/CancelDeposit` | Cancelar depósito |
| Action `CancelDepositbyCurrentSystemDate` | `POST /b1s/v2/Deposits(1)/CancelDepositbyCurrentSystemDate` | Cancelar depósito con la fecha actual del sistema |

## Properties (48)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DepositNumber` | Edm.Int32 | Yes | Deposit Number | Número de depósito |
| 2 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 3 | `DepositType` | [BoDepositTypeEnum](../Enums/BoDepositTypeEnum.md) | Yes | Deposit Type | Tipo de depósito |
| 4 | `DepositDate` | Edm.DateTimeOffset | Yes | Deposit Date | Fecha del depósito |
| 5 | `DepositCurrency` | Edm.String | Yes | Deposit Currency | Moneda del depósito |
| 6 | `DepositAccount` | Edm.String | Yes | Deposit Account | Cuenta de depósito |
| 7 | `DepositorName` | Edm.String | Yes | Depositor Name | Nombre del depositante |
| 8 | `Bank` | Edm.String | Yes | Bank | Banco |
| 9 | `BankAccountNum` | Edm.String | Yes | Bank Account Number | Número de cuenta bancaria |
| 10 | `BankBranch` | Edm.String | Yes | Bank Branch | Sucursal bancaria |
| 11 | `BankReference` | Edm.String | Yes | Bank Reference | Referencia bancaria |
| 12 | `JournalRemarks` | Edm.String | Yes | Journal Remarks | Comentarios del asiento |
| 13 | `TotalLC` | Edm.Double | Yes | Total LC (local currency) | Total (moneda local) |
| 14 | `TotalFC` | Edm.Double | Yes | Total FC (foreign currency) | Total (ME) |
| 15 | `TotalSC` | Edm.Double | Yes | Total SC (system currency) | Total (moneda del sistema) |
| 16 | `AllocationAccount` | Edm.String | Yes | Allocation Account | Cuenta de asignación |
| 17 | `DocRate` | Edm.Double | Yes | Document Rate | Tipo de cambio del documento |
| 18 | `TaxAccount` | Edm.String | Yes | Tax Account | Cuenta de impuestos |
| 19 | `TaxAmount` | Edm.Double | Yes | Tax Amount | Importe de impuestos |
| 20 | `CommissionAccount` | Edm.String | Yes | Commission Account | Cuenta de comisión |
| 21 | `Commission` | Edm.Double | Yes | Commission | Comisión |
| 22 | `CommissionDate` | Edm.DateTimeOffset | Yes | Commission Date | Fecha de la comisión |
| 23 | `TaxCode` | Edm.String | Yes | Tax Code | Indicador de impuesto |
| 24 | `DepositAccountType` | [BoDepositAccountTypeEnum](../Enums/BoDepositAccountTypeEnum.md) | Yes | Deposit Account Type | Tipo de cuenta de depósito |
| 25 | `ReconcileAfterDeposit` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Reconcile After Deposit | Conciliar después del depósito |
| 26 | `VoucherAccount` | Edm.String | Yes | Voucher Account | Cuenta del vale |
| 27 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 28 | `Project` | Edm.String | Yes | Project | Proyecto |
| 29 | `DistributionRule` | Edm.String | Yes | Distribution Rule | Norma de reparto |
| 30 | `DistributionRule2` | Edm.String | Yes | Distribution Rule 2 | Norma de reparto 2 |
| 31 | `DistributionRule3` | Edm.String | Yes | Distribution Rule 3 | Norma de reparto 3 |
| 32 | `DistributionRule4` | Edm.String | Yes | Distribution Rule 4 | Norma de reparto 4 |
| 33 | `DistributionRule5` | Edm.String | Yes | Distribution Rule 5 | Norma de reparto 5 |
| 34 | `CommissionCurrency` | Edm.String | Yes | Commission Currency | Moneda de la comisión |
| 35 | `CommissionSC` | Edm.Double | Yes | Commission SC (system currency) | Comisión (moneda del sistema) |
| 36 | `CommissionFC` | Edm.Double | Yes | Commission FC (foreign currency) | Comisión (ME) |
| 37 | `TaxAmountSC` | Edm.Double | Yes | Tax Amount SC (system currency) | Importe de impuestos (moneda del sistema) |
| 38 | `TaxAmountFC` | Edm.Double | Yes | Tax Amount FC (foreign currency) | Importe de impuestos (ME) |
| 39 | `BPLID` | Edm.Int32 | Yes | BPLID | ID de sucursal |
| 40 | `CheckDepositType` | [BoCheckDepositTypeEnum](../Enums/BoCheckDepositTypeEnum.md) | Yes | Check Deposit Type | Tipo de depósito de cheques |
| 41 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 42 | `IncomeTaxAccount` | Edm.String | Yes | Income Tax Account | Cuenta de impuesto a las ganancias |
| 43 | `IncomeTaxAmount` | Edm.Double | Yes | Income Tax Amount | Importe del impuesto a las ganancias |
| 44 | `IncomeTaxAmountSC` | Edm.Double | Yes | Income Tax Amount SC (system currency) | Importe del impuesto a las ganancias (moneda del sistema) |
| 45 | `IncomeTaxAmountFC` | Edm.Double | Yes | Income Tax Amount FC (foreign currency) | Importe del impuesto a las ganancias (ME) |
| 46 | `CheckLines` | Collection([CheckLine](../Tipos-Complejos/CheckLine.md)) | Yes | Check Lines | Líneas de cheques |
| 47 | `CreditLines` | Collection([CreditLine](../Tipos-Complejos/CreditLine.md)) | Yes | Credit Lines | Líneas de tarjetas de crédito |
| 48 | `BOELines` | Collection([BOELine](../Tipos-Complejos/BOELine.md)) | Yes | BOE Lines | Líneas de letras de cambio |

## Navigation properties (5)

Use `GET /b1s/v2/Deposits(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `VatGroup` | [VatGroup](../Entidades/VatGroups.md) | [VatGroups](VatGroups.md) | TaxCode → Code | Grupo de IVA (indicador de impuesto) |
| `Project2` | [Project](../Entidades/Projects.md) | [Projects](Projects.md) | Project → Code | Proyectos |
| `DistributionRule6` | [DistributionRule](../Entidades/DistributionRules.md) | [DistributionRules](DistributionRules.md) | DistributionRule → FactorCode | Normas de reparto |
| `BusinessPlace` | [BusinessPlace](../Entidades/BusinessPlaces.md) | [BusinessPlaces](BusinessPlaces.md) | BPLID → BPLID | Lugar de negocios |
| `Attachments2` | [Attachments2](../Entidades/Attachments2.md) | [Attachments2](Attachments2.md) | AttachmentEntry → AbsoluteEntry | Anexos |

## Bound actions (2)

### CancelDeposit

- **Descripción (ES):** Cancelar depósito
- **Request:** `POST /b1s/v2/Deposits(1)/CancelDeposit`

### CancelDepositbyCurrentSystemDate

- **Descripción (ES):** Cancelar depósito con la fecha actual del sistema
- **Request:** `POST /b1s/v2/Deposits(1)/CancelDepositbyCurrentSystemDate`

