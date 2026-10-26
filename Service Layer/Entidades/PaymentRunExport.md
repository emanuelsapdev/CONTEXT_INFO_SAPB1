# PaymentRunExport — Exportación de ejecución de pagos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `PaymentRunExport`
- **Descripción (ES):** Exportación de ejecución de pagos
- **Entity type:** `PaymentRunExport` (open type: accepts dynamic/UDF properties)
- **Key:** `AbsoluteEntry` (Edm.Int32)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 96 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/PaymentRunExport?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/PaymentRunExport/$count` | Contar |
| Get by key | `GET /b1s/v2/PaymentRunExport(1)` | Obtener por clave |
| Create | `POST /b1s/v2/PaymentRunExport` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/PaymentRunExport(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/PaymentRunExport(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/PaymentRunExport(1)` (only if the B1 object allows removal) | Borrar |

## Properties (96)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsoluteEntry` 🔑 | Edm.Int32 | No | Absolute Entry | Entrada absoluta (ID interno) |
| 2 | `RunDate` | Edm.DateTimeOffset | Yes | Run Date | Fecha de ejecución |
| 3 | `VendorNum` | Edm.String | Yes | Vendor Number | Número de proveedor |
| 4 | `CustomerNum` | Edm.String | Yes | Customer Number | Número de cliente |
| 5 | `PaymentMethod` | Edm.String | Yes | Payment Method | Vía de pago |
| 6 | `DocNum` | Edm.Int32 | Yes | Document Number | Número de documento |
| 7 | `FiscalYear` | Edm.DateTimeOffset | Yes | Fiscal Year | Ejercicio fiscal |
| 8 | `Countery` | Edm.String | Yes | Countery | País |
| 9 | `CompanyTaxNum` | Edm.String | Yes | Company Tax Number | Número fiscal de la sociedad |
| 10 | `PayeeName` | Edm.String | Yes | Payee Name | Nombre del beneficiario |
| 11 | `PayeePostalCode` | Edm.String | Yes | Payee Postal Code | Código postal del beneficiario |
| 12 | `PayeeCity` | Edm.String | Yes | Payee City | Ciudad del beneficiario |
| 13 | `PayeeStreet` | Edm.String | Yes | Payee Street | Calle del beneficiario |
| 14 | `PayeeCountry` | Edm.String | Yes | Payee Country | País del beneficiario |
| 15 | `PayeeState` | Edm.String | Yes | Payee State | Estado del beneficiario |
| 16 | `PayeeBankName` | Edm.String | Yes | Payee Bank Name | Nombre del banco del beneficiario |
| 17 | `PayeeBankZip` | Edm.String | Yes | Payee Bank Zip | Código postal del banco del beneficiario |
| 18 | `PayeeBankCity` | Edm.String | Yes | Payee Bank City | Ciudad del banco del beneficiario |
| 19 | `PayeeBankStreet` | Edm.String | Yes | Payee Bank Street | Calle del banco del beneficiario |
| 20 | `PayeeBankCountry` | Edm.String | Yes | Payee Bank Country | País del banco del beneficiario |
| 21 | `PayeeBankAccount` | Edm.String | Yes | Payee Bank Account | Cuenta bancaria del beneficiario |
| 22 | `PayeeBankCode` | Edm.String | Yes | Payee Bank Code | Código del banco del beneficiario |
| 23 | `PayeeBankCtrlKey` | Edm.String | Yes | Payee Bank Ctrl Key | Clave de control del banco del beneficiario |
| 24 | `PayeeBankSwiftNum` | Edm.String | Yes | Payee Bank Swift Number | SWIFT del banco del beneficiario |
| 25 | `PayeeBankIBAN` | Edm.String | Yes | Payee Bank IBAN | IBAN del banco del beneficiario |
| 26 | `PostingDate` | Edm.DateTimeOffset | Yes | Posting Date | Fecha de contabilización |
| 27 | `BankAccount` | Edm.String | Yes | Bank Account | Cuenta bancaria |
| 28 | `BankCountry` | Edm.String | Yes | Bank Country | País del banco |
| 29 | `BankCode` | Edm.String | Yes | Bank Code | Código del banco |
| 30 | `BankIBAN` | Edm.String | Yes | Bank IBAN | IBAN bancario |
| 31 | `GLAccount` | Edm.String | Yes | G/L Account | Cuenta de mayor |
| 32 | `Currency` | Edm.String | Yes | Currency | Moneda |
| 33 | `DocAmountLocal` | Edm.Double | Yes | Document Amount Local | Importe del documento (moneda local) |
| 34 | `DocCurrnecy` | Edm.String | Yes | Document Currnecy | Moneda del documento |
| 35 | `DocAmountForign` | Edm.Double | Yes | Document Amount Forign | Importe del documento (ME) |
| 36 | `DocCashDiscount` | Edm.Double | Yes | Document Cash Discount | Descuento por pronto pago del documento |
| 37 | `DocCashDiscountForign` | Edm.Double | Yes | Document Cash Discount Forign | Descuento por pronto pago del documento (ME) |
| 38 | `DocNumOffieldPaid` | Edm.Int32 | Yes | Document Number Offield Paid | Número de documento del campo pagado |
| 39 | `DocRate` | Edm.Double | Yes | Document Rate | Tipo de cambio del documento |
| 40 | `WizCode` | Edm.Int32 | Yes | Wiz Code | Código del asistente |
| 41 | `CollectionAuthorization` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Collection Authorization | Autorización de cobro |
| 42 | `PayeeBankPostOffice` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Payee Bank Post Office | Oficina postal del banco del beneficiario |
| 43 | `PayeeBankNextCheckNumber` | Edm.Int32 | Yes | Payee Bank Next Check Number | Siguiente número de cheque del banco del beneficiario |
| 44 | `PayeeBankHouseBank` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Payee Bank House Bank | Banco propio del beneficiario |
| 45 | `PayeeBankBlock` | Edm.String | Yes | Payee Bank Block | Barrio del banco del beneficiario |
| 46 | `PayeeBankCounty` | Edm.String | Yes | Payee Bank County | Condado del banco del beneficiario |
| 47 | `PayeeBankState` | Edm.String | Yes | Payee Bank State | Estado del banco del beneficiario |
| 48 | `PayeeBankBISR` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Payee Bank BISR | BISR del banco del beneficiario |
| 49 | `PayeeBankUserNum1` | Edm.String | Yes | Payee Bank User Number 1 | N.º de usuario 1 del banco del beneficiario |
| 50 | `PayeeBankUserNum2` | Edm.String | Yes | Payee Bank User Number 2 | N.º de usuario 2 del banco del beneficiario |
| 51 | `PayeeBankUserNum3` | Edm.String | Yes | Payee Bank User Number 3 | N.º de usuario 3 del banco del beneficiario |
| 52 | `PayeeBankUserNum4` | Edm.String | Yes | Payee Bank User Number 4 | N.º de usuario 4 del banco del beneficiario |
| 53 | `InstructionKey` | Edm.String | Yes | Instruction Key | Clave de instrucción |
| 54 | `PaymentFormat` | Edm.String | Yes | Payment Format | Formato de pago |
| 55 | `CompanyName` | Edm.String | Yes | Company Name | Nombre de la sociedad |
| 56 | `CompanyAddress` | Edm.String | Yes | Company Address | Dirección de la sociedad |
| 57 | `Status` | [BoOpexStatus](../Enums/BoOpexStatus.md) | Yes | Status | Estado |
| 58 | `CompIsrBillerID` | Edm.String | Yes | Comp Isr Biller ID | ID de facturador ISR de la sociedad |
| 59 | `VendorIsrBillerID` | Edm.String | Yes | Vendor Isr Biller ID | ID de facturador ISR del proveedor |
| 60 | `AdditionalIdNumber` | Edm.String | Yes | Additional ID Number | Número de identificación adicional |
| 61 | `OrganizationNumber` | Edm.String | Yes | Organization Number | Número de organización |
| 62 | `PayeeBankBranch` | Edm.String | Yes | Payee Bank Branch | Sucursal del banco del beneficiario |
| 63 | `PaymentBankBranch` | Edm.String | Yes | Payment Bank Branch | Sucursal del banco de pago |
| 64 | `UserName` | Edm.String | Yes | User Name | Nombre de usuario |
| 65 | `UserEMail` | Edm.String | Yes | User E Mail | Correo del usuario |
| 66 | `UserMobilePhoneNumber` | Edm.String | Yes | User Mobile Phone Number | Celular del usuario |
| 67 | `UserFaxNumber` | Edm.String | Yes | User Fax Number | Fax del usuario |
| 68 | `UserDepartment` | Edm.Int32 | Yes | User Department | Departamento del usuario |
| 69 | `DebitMemo` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Debit Memo | Nota de débito |
| 70 | `EUInternalTransfer` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | EU Internal Transfer | Transferencia interna UE |
| 71 | `FilePath` | Edm.String | Yes | File Path | Ruta del archivo |
| 72 | `OrderingParty` | Edm.String | Yes | Ordering Party | Ordenante |
| 73 | `PaymentBankControlKey` | Edm.String | Yes | Payment Bank Control Key | Clave de control del banco de pago |
| 74 | `PayeeTaxNumber` | Edm.String | Yes | Payee Tax Number | Número fiscal del beneficiario |
| 75 | `PaymentKeyCode` | Edm.String | Yes | Payment Key Code | Código de clave de pago |
| 76 | `PayeeReferenceDetails` | Edm.String | Yes | Payee Reference Details | Detalles de referencia del beneficiario |
| 77 | `FormatName` | Edm.String | Yes | Format Name | Nombre de formato |
| 78 | `PaymentDonewithCheck` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Payment Donewith Check | Pago realizado con cheque |
| 79 | `CompanyBlock` | Edm.String | Yes | Company Block | Barrio de la sociedad |
| 80 | `CompanyCity` | Edm.String | Yes | Company City | Ciudad de la sociedad |
| 81 | `CompanyCounty` | Edm.String | Yes | Company County | Condado de la sociedad |
| 82 | `CompanyState` | Edm.String | Yes | Company State | Estado/provincia de la sociedad |
| 83 | `CompanyStreet` | Edm.String | Yes | Company Street | Calle de la sociedad |
| 84 | `CompanyZipCode` | Edm.String | Yes | Company Zip Code | Código postal de la sociedad |
| 85 | `PaymentBankCharges` | Edm.String | Yes | Payment Bank Charges | Comisiones bancarias del pago |
| 86 | `PaymentBankUserNo1` | Edm.String | Yes | Payment Bank User Number 1 | N.º de usuario 1 del banco de pago |
| 87 | `PaymentBankUserNo2` | Edm.String | Yes | Payment Bank User Number 2 | N.º de usuario 2 del banco de pago |
| 88 | `PaymentBankUserNo3` | Edm.String | Yes | Payment Bank User Number 3 | N.º de usuario 3 del banco de pago |
| 89 | `PaymentBankUserNo4` | Edm.String | Yes | Payment Bank User Number 4 | N.º de usuario 4 del banco de pago |
| 90 | `PaymentBankChargesAllocationCode` | Edm.String | Yes | Payment Bank Charges Allocation Code | Código de imputación de comisiones del pago |
| 91 | `PaymentOrderNum` | Edm.Int32 | Yes | Payment Order Number | Número de orden de pago |
| 92 | `FreeText1` | Edm.String | Yes | Free Text 1 | Texto libre 1 |
| 93 | `FreeText2` | Edm.String | Yes | Free Text 2 | Texto libre 2 |
| 94 | `FreeText3` | Edm.String | Yes | Free Text 3 | Texto libre 3 |
| 95 | `RowType` | [PaymentRunExportRowTypeEnum](../Enums/PaymentRunExportRowTypeEnum.md) | Yes | Row Type | Tipo de línea |
| 96 | `PaymentRunExport_Lines` | Collection([PaymentRunExport_Line](../Tipos-Complejos/PaymentRunExport_Line.md)) | Yes | Payment Run Export Lines | Líneas de exportación de la ejecución de pagos |

## Navigation properties (1)

Use `GET /b1s/v2/PaymentRunExport(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BankChargesAllocationCode` | [BankChargesAllocationCode](../Entidades/BankChargesAllocationCodes.md) | [BankChargesAllocationCodes](BankChargesAllocationCodes.md) | PaymentBankCharges → Code | Código de imputación de comisiones bancarias |
