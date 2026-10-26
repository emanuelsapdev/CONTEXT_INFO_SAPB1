# InternalReconciliationRow — Líneas de la conciliación interna

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `InternalReconciliationRow`
- **Descripción (ES):** Líneas de la conciliación interna
- **Description (EN):** Internal Reconciliation Row

- **Properties:** 9

## Properties (9)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineSeq` | Edm.Int32 | Yes | Line Seq | Secuencia de línea |
| 2 | `ShortName` | Edm.String | Yes | Short Name | Nombre corto |
| 3 | `TransId` | Edm.Int32 | Yes | Trans ID | ID de transacción (asiento) |
| 4 | `TransRowId` | Edm.Int32 | Yes | Trans Row ID | ID de línea de la transacción |
| 5 | `SrcObjTyp` | Edm.String | Yes | Src Obj Typ | Tipo de objeto de origen |
| 6 | `SrcObjAbs` | Edm.Int32 | Yes | Src Obj Abs | Entrada del objeto de origen |
| 7 | `CreditOrDebit` | [CreditOrDebitEnum](../Enums/CreditOrDebitEnum.md) | Yes | Credit Or Debit | Haber o debe |
| 8 | `ReconcileAmount` | Edm.Double | Yes | Reconcile Amount | Importe a conciliar |
| 9 | `CashDiscount` | Edm.Double | Yes | Cash Discount | Descuento por pronto pago |

## Used by (properties)

- [InternalReconciliation](../Entidades/InternalReconciliations.md).`InternalReconciliationRows`
