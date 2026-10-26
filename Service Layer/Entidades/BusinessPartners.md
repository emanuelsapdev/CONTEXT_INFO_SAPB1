# BusinessPartners — Socios de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BusinessPartners`
- **Descripción (ES):** Socios de negocios
- **Entity type:** `BusinessPartner` (open type: accepts dynamic/UDF properties)
- **Key:** `CardCode` (Edm.String)
- **DB tables (main / lines):** [OCRD](../../Tablas%20SAP%20B1/OCRD.md), [CRD1](../../Tablas%20SAP%20B1/CRD1.md), [OCPR](../../Tablas%20SAP%20B1/OCPR.md), [OCRB](../../Tablas%20SAP%20B1/OCRB.md)
- **ETag / optimistic concurrency:** Yes (`DataVersion`) — send `If-Match` on PATCH/DELETE/actions

- **Properties:** 322 · **Navigation properties:** 93 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BusinessPartners?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BusinessPartners/$count` | Contar |
| Get by key | `GET /b1s/v2/BusinessPartners('value')` | Obtener por clave |
| Create | `POST /b1s/v2/BusinessPartners` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BusinessPartners('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BusinessPartners('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/BusinessPartners('value')` (only if the B1 object allows removal) | Borrar |

## Properties (322)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `CardCode` 🔑 | Edm.String | No | Card Code | Código del socio de negocios |
| 2 | `CardName` | Edm.String | Yes | Card Name | Nombre del socio de negocios |
| 3 | `CardType` | [BoCardTypes](../Enums/BoCardTypes.md) | Yes | Card Type | Tipo de socio de negocios (cliente/proveedor/lead) |
| 4 | `GroupCode` | Edm.Int32 | Yes | Group Code | Código de grupo |
| 5 | `Address` | Edm.String | Yes | Address | Dirección |
| 6 | `ZipCode` | Edm.String | Yes | Zip Code | Código postal |
| 7 | `MailAddress` | Edm.String | Yes | Mail Address | Dirección postal (envío) |
| 8 | `MailZipCode` | Edm.String | Yes | Mail Zip Code | Código postal (envío) |
| 9 | `Phone1` | Edm.String | Yes | Phone 1 | Teléfono 1 |
| 10 | `Phone2` | Edm.String | Yes | Phone 2 | Teléfono 2 |
| 11 | `Fax` | Edm.String | Yes | Fax | Fax |
| 12 | `ContactPerson` | Edm.String | Yes | Contact Person | Persona de contacto |
| 13 | `Notes` | Edm.String | Yes | Notes | Notas |
| 14 | `PayTermsGrpCode` | Edm.Int32 | Yes | Pay Terms Group Code | Código de condiciones de pago |
| 15 | `CreditLimit` | Edm.Double | Yes | Credit Limit | Límite de crédito |
| 16 | `MaxCommitment` | Edm.Double | Yes | Max Commitment | Compromiso máximo |
| 17 | `DiscountPercent` | Edm.Double | Yes | Discount Percent | Porcentaje de descuento |
| 18 | `VatLiable` | [BoVatStatus](../Enums/BoVatStatus.md) | Yes | Vat Liable | Sujeto a IVA |
| 19 | `FederalTaxID` | Edm.String | Yes | Federal Tax ID | CUIT / ID fiscal federal |
| 20 | `DeductibleAtSource` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Deductible At Source | Deducible en la fuente |
| 21 | `DeductionPercent` | Edm.Double | Yes | Deduction Percent | Porcentaje de deducción |
| 22 | `DeductionValidUntil` | Edm.DateTimeOffset | Yes | Deduction Valid Until | Deducción válida hasta |
| 23 | `PriceListNum` | Edm.Int32 | Yes | Price List Number | Número de lista de precios |
| 24 | `IntrestRatePercent` | Edm.Double | Yes | Intrest Rate Percent | Porcentaje de tasa de interés |
| 25 | `CommissionPercent` | Edm.Double | Yes | Commission Percent | Porcentaje de comisión |
| 26 | `CommissionGroupCode` | Edm.Int32 | Yes | Commission Group Code | Código de grupo de comisiones |
| 27 | `FreeText` | Edm.String | Yes | Free Text | Texto libre |
| 28 | `SalesPersonCode` | Edm.Int32 | Yes | Sales Person Code | Código del empleado de ventas |
| 29 | `Currency` | Edm.String | Yes | Currency | Moneda |
| 30 | `RateDiffAccount` | Edm.String | Yes | Rate Diff Account | Cuenta de diferencias de cambio |
| 31 | `Cellular` | Edm.String | Yes | Cellular | Celular |
| 32 | `AvarageLate` | Edm.Int32 | Yes | Avarage Late | Atraso promedio |
| 33 | `City` | Edm.String | Yes | City | Ciudad |
| 34 | `County` | Edm.String | Yes | County | Condado |
| 35 | `Country` | Edm.String | Yes | Country | País |
| 36 | `MailCity` | Edm.String | Yes | Mail City | Ciudad (envío) |
| 37 | `MailCounty` | Edm.String | Yes | Mail County | Condado (envío) |
| 38 | `MailCountry` | Edm.String | Yes | Mail Country | País (envío) |
| 39 | `EmailAddress` | Edm.String | Yes | Email Address | Dirección de correo electrónico |
| 40 | `Picture` | Edm.String | Yes | Picture | Imagen |
| 41 | `DefaultAccount` | Edm.String | Yes | Default Account | Cuenta predeterminada |
| 42 | `DefaultBranch` | Edm.String | Yes | Default Branch | Sucursal predeterminada |
| 43 | `DefaultBankCode` | Edm.String | Yes | Default Bank Code | Código de banco predeterminado |
| 44 | `AdditionalID` | Edm.String | Yes | Additional ID | ID adicional |
| 45 | `Pager` | Edm.String | Yes | Pager | Buscapersonas |
| 46 | `FatherCard` | Edm.String | Yes | Father Card | Socio de negocios consolidador (padre) |
| 47 | `CardForeignName` | Edm.String | Yes | Card Foreign Name | Nombre extranjero del socio de negocios |
| 48 | `FatherType` | [BoFatherCardTypes](../Enums/BoFatherCardTypes.md) | Yes | Father Type | Tipo de consolidación (pagos/entregas) |
| 49 | `DeductionOffice` | Edm.String | Yes | Deduction Office | Oficina de deducción |
| 50 | `ExportCode` | Edm.String | Yes | Export Code | Código de exportación |
| 51 | `MinIntrest` | Edm.Double | Yes | Min Intrest | Interés mínimo |
| 52 | `CurrentAccountBalance` | Edm.Double | Yes | Current Account Balance | Saldo de cuenta actual |
| 53 | `OpenDeliveryNotesBalance` | Edm.Double | Yes | Open Delivery Notes Balance | Saldo de entregas abiertas |
| 54 | `OpenOrdersBalance` | Edm.Double | Yes | Open Orders Balance | Saldo de pedidos abiertos |
| 55 | `OpenChecksBalance` | Edm.Double | Yes | Open Checks Balance | Saldo de cheques abiertos |
| 56 | `VatGroup` | Edm.String | Yes | Vat Group | Grupo de IVA (indicador de impuesto) |
| 57 | `ShippingType` | Edm.Int32 | Yes | Shipping Type | Clase de expedición |
| 58 | `Password` | Edm.String | Yes | Password | Contraseña |
| 59 | `Indicator` | Edm.String | Yes | Indicator | Indicador |
| 60 | `IBAN` | Edm.String | Yes | IBAN | IBAN |
| 61 | `CreditCardCode` | Edm.Int32 | Yes | Credit Card Code | Código de tarjeta de crédito |
| 62 | `CreditCardNum` | Edm.String | Yes | Credit Card Number | Número de tarjeta de crédito |
| 63 | `CreditCardExpiration` | Edm.DateTimeOffset | Yes | Credit Card Expiration | Vencimiento de tarjeta de crédito |
| 64 | `DebitorAccount` | Edm.String | Yes | Debitor Account | Cuenta deudora |
| 65 | `OpenOpportunities` | Edm.Int32 | Yes | Open Opportunities | Oportunidades abiertas |
| 66 | `Valid` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Valid | Válido (activo) |
| 67 | `ValidFrom` | Edm.DateTimeOffset | Yes | Valid From | Válido desde |
| 68 | `ValidTo` | Edm.DateTimeOffset | Yes | Valid To | Válido hasta |
| 69 | `ValidRemarks` | Edm.String | Yes | Valid Remarks | Comentarios de validez |
| 70 | `Frozen` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Frozen | Congelado (inactivo) |
| 71 | `FrozenFrom` | Edm.DateTimeOffset | Yes | Frozen From | Congelado desde |
| 72 | `FrozenTo` | Edm.DateTimeOffset | Yes | Frozen To | Congelado hasta |
| 73 | `FrozenRemarks` | Edm.String | Yes | Frozen Remarks | Comentarios de congelación |
| 74 | `Block` | Edm.String | Yes | Block | Barrio/bloque |
| 75 | `BillToState` | Edm.String | Yes | Bill To State | Estado/provincia de facturación |
| 76 | `ShipToState` | Edm.String | Yes | Ship To State | Estado/provincia de envío |
| 77 | `ExemptNum` | Edm.String | Yes | Exempt Number | Número de exención |
| 78 | `Priority` | Edm.Int32 | Yes | Priority | Prioridad |
| 79 | `FormCode1099` | Edm.Int32 | Yes | Form Code 1099 | Código de formulario 1099 |
| 80 | `Box1099` | Edm.String | Yes | Box 1099 | Casilla 1099 |
| 81 | `PeymentMethodCode` | Edm.String | Yes | Peyment Method Code | Código de vía de pago |
| 82 | `BackOrder` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Back Order | Pedido pendiente (backorder) |
| 83 | `PartialDelivery` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Partial Delivery | Entrega parcial |
| 84 | `BlockDunning` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Block Dunning | Bloquear reclamaciones |
| 85 | `BankCountry` | Edm.String | Yes | Bank Country | País del banco |
| 86 | `HouseBank` | Edm.String | Yes | House Bank | Banco propio |
| 87 | `HouseBankCountry` | Edm.String | Yes | House Bank Country | País del banco propio |
| 88 | `HouseBankAccount` | Edm.String | Yes | House Bank Account | Cuenta bancaria propia |
| 89 | `ShipToDefault` | Edm.String | Yes | Ship To Default | Dirección de envío predeterminada |
| 90 | `DunningLevel` | Edm.Int32 | Yes | Dunning Level | Nivel de reclamación |
| 91 | `DunningDate` | Edm.DateTimeOffset | Yes | Dunning Date | Fecha de reclamación |
| 92 | `CollectionAuthorization` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Collection Authorization | Autorización de cobro |
| 93 | `DME` | Edm.String | Yes | DME | DME (intercambio de datos) |
| 94 | `InstructionKey` | Edm.String | Yes | Instruction Key | Clave de instrucción |
| 95 | `SinglePayment` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Single Payment | Pago único |
| 96 | `ISRBillerID` | Edm.String | Yes | ISR Biller ID | ID de facturador ISR |
| 97 | `PaymentBlock` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Payment Block | Bloqueo de pago |
| 98 | `ReferenceDetails` | Edm.String | Yes | Reference Details | Detalles de referencia |
| 99 | `HouseBankBranch` | Edm.String | Yes | House Bank Branch | Sucursal del banco propio |
| 100 | `OwnerIDNumber` | Edm.String | Yes | Owner ID Number | N.º de identificación del titular |
| 101 | `PaymentBlockDescription` | Edm.Int32 | Yes | Payment Block Description | Descripción del bloqueo de pago |
| 102 | `TaxExemptionLetterNum` | Edm.String | Yes | Tax Exemption Letter Number | N.º de carta de exención de impuestos |
| 103 | `MaxAmountOfExemption` | Edm.Double | Yes | Max Amount Of Exemption | Importe máximo de exención |
| 104 | `ExemptionValidityDateFrom` | Edm.DateTimeOffset | Yes | Exemption Validity Date From | Validez de exención desde |
| 105 | `ExemptionValidityDateTo` | Edm.DateTimeOffset | Yes | Exemption Validity Date To | Validez de exención hasta |
| 106 | `LinkedBusinessPartner` | Edm.String | Yes | Linked Business Partner | Socio de negocios vinculado |
| 107 | `LastMultiReconciliationNum` | Edm.Int32 | Yes | Last Multi Reconciliation Number | Último número de conciliación múltiple |
| 108 | `DeferredTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Deferred Tax | Impuesto diferido |
| 109 | `Equalization` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Equalization | Recargo de equivalencia |
| 110 | `SubjectToWithholdingTax` | [BoYesNoNoneEnum](../Enums/BoYesNoNoneEnum.md) | Yes | Subject To Withholding Tax | Sujeto a retención de impuestos |
| 111 | `CertificateNumber` | Edm.String | Yes | Certificate Number | Número de certificado |
| 112 | `ExpirationDate` | Edm.DateTimeOffset | Yes | Expiration Date | Fecha de vencimiento |
| 113 | `NationalInsuranceNum` | Edm.String | Yes | National Insurance Number | Número de seguridad social |
| 114 | `AccrualCriteria` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Accrual Criteria | Criterio de periodificación |
| 115 | `WTCode` | Edm.String | Yes | Withholding Tax Code | Código de retención |
| 116 | `BillToBuildingFloorRoom` | Edm.String | Yes | Bill To Building Floor Room | Edificio/piso/oficina de facturación |
| 117 | `DownPaymentClearAct` | Edm.String | Yes | Down Payment Clear Act | Cuenta de compensación de anticipos |
| 118 | `ChannelBP` | Edm.String | Yes | Channel Business Partner | Socio de canal |
| 119 | `DefaultTechnician` | Edm.Int32 | Yes | Default Technician | Técnico predeterminado |
| 120 | `BilltoDefault` | Edm.String | Yes | Billto Default | Dirección de facturación predeterminada |
| 121 | `CustomerBillofExchangDisc` | Edm.String | Yes | Customer Billof Exchang Disc | Letras de cambio de clientes descontadas |
| 122 | `Territory` | Edm.Int32 | Yes | Territory | Territorio |
| 123 | `ShipToBuildingFloorRoom` | Edm.String | Yes | Ship To Building Floor Room | Edificio/piso de envío |
| 124 | `CustomerBillofExchangPres` | Edm.String | Yes | Customer Billof Exchang Pres | Letras de cambio de clientes presentadas |
| 125 | `ProjectCode` | Edm.String | Yes | Project Code | Código de proyecto |
| 126 | `VatGroupLatinAmerica` | Edm.String | Yes | Vat Group Latin America | Grupo de IVA (Latinoamérica) |
| 127 | `DunningTerm` | Edm.String | Yes | Dunning Term | Condición de reclamación |
| 128 | `Website` | Edm.String | Yes | Website | Sitio web |
| 129 | `OtherReceivablePayable` | Edm.String | Yes | Other Receivable Payable | Otras cuentas por cobrar/pagar |
| 130 | `BillofExchangeonCollection` | Edm.String | Yes | Billof Exchangeon Collection | Letra de cambio en cobranza |
| 131 | `CompanyPrivate` | [BoCardCompanyTypes](../Enums/BoCardCompanyTypes.md) | Yes | Company Private | Tipo de entidad (empresa/privado/gobierno/empleado) |
| 132 | `LanguageCode` | Edm.Int32 | Yes | Language Code | Código de idioma |
| 133 | `UnpaidBillofExchange` | Edm.String | Yes | Unpaid Billof Exchange | Letra de cambio impaga |
| 134 | `WithholdingTaxDeductionGroup` | Edm.Int32 | Yes | Withholding Tax Deduction Group | Grupo de deducción de retenciones |
| 135 | `ClosingDateProcedureNumber` | Edm.Int32 | Yes | Closing Date Procedure Number | Número de procedimiento de fecha de cierre |
| 136 | `Profession` | Edm.String | Yes | Profession | Profesión |
| 137 | `BankChargesAllocationCode` | Edm.String | Yes | Bank Charges Allocation Code | Código de imputación de comisiones bancarias |
| 138 | `TaxRoundingRule` | [BoTaxRoundingRuleTypes](../Enums/BoTaxRoundingRuleTypes.md) | Yes | Tax Rounding Rule | Regla de redondeo de impuestos |
| 139 | `Properties1` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 1 | Propiedad 1 |
| 140 | `Properties2` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 2 | Propiedad 2 |
| 141 | `Properties3` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 3 | Propiedad 3 |
| 142 | `Properties4` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 4 | Propiedad 4 |
| 143 | `Properties5` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 5 | Propiedad 5 |
| 144 | `Properties6` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 6 | Propiedad 6 |
| 145 | `Properties7` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 7 | Propiedad 7 |
| 146 | `Properties8` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 8 | Propiedad 8 |
| 147 | `Properties9` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 9 | Propiedad 9 |
| 148 | `Properties10` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 10 | Propiedad 10 |
| 149 | `Properties11` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 11 | Propiedad 11 |
| 150 | `Properties12` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 12 | Propiedad 12 |
| 151 | `Properties13` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 13 | Propiedad 13 |
| 152 | `Properties14` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 14 | Propiedad 14 |
| 153 | `Properties15` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 15 | Propiedad 15 |
| 154 | `Properties16` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 16 | Propiedad 16 |
| 155 | `Properties17` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 17 | Propiedad 17 |
| 156 | `Properties18` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 18 | Propiedad 18 |
| 157 | `Properties19` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 19 | Propiedad 19 |
| 158 | `Properties20` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 20 | Propiedad 20 |
| 159 | `Properties21` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 21 | Propiedad 21 |
| 160 | `Properties22` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 22 | Propiedad 22 |
| 161 | `Properties23` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 23 | Propiedad 23 |
| 162 | `Properties24` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 24 | Propiedad 24 |
| 163 | `Properties25` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 25 | Propiedad 25 |
| 164 | `Properties26` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 26 | Propiedad 26 |
| 165 | `Properties27` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 27 | Propiedad 27 |
| 166 | `Properties28` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 28 | Propiedad 28 |
| 167 | `Properties29` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 29 | Propiedad 29 |
| 168 | `Properties30` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 30 | Propiedad 30 |
| 169 | `Properties31` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 31 | Propiedad 31 |
| 170 | `Properties32` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 32 | Propiedad 32 |
| 171 | `Properties33` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 33 | Propiedad 33 |
| 172 | `Properties34` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 34 | Propiedad 34 |
| 173 | `Properties35` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 35 | Propiedad 35 |
| 174 | `Properties36` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 36 | Propiedad 36 |
| 175 | `Properties37` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 37 | Propiedad 37 |
| 176 | `Properties38` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 38 | Propiedad 38 |
| 177 | `Properties39` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 39 | Propiedad 39 |
| 178 | `Properties40` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 40 | Propiedad 40 |
| 179 | `Properties41` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 41 | Propiedad 41 |
| 180 | `Properties42` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 42 | Propiedad 42 |
| 181 | `Properties43` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 43 | Propiedad 43 |
| 182 | `Properties44` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 44 | Propiedad 44 |
| 183 | `Properties45` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 45 | Propiedad 45 |
| 184 | `Properties46` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 46 | Propiedad 46 |
| 185 | `Properties47` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 47 | Propiedad 47 |
| 186 | `Properties48` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 48 | Propiedad 48 |
| 187 | `Properties49` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 49 | Propiedad 49 |
| 188 | `Properties50` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 50 | Propiedad 50 |
| 189 | `Properties51` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 51 | Propiedad 51 |
| 190 | `Properties52` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 52 | Propiedad 52 |
| 191 | `Properties53` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 53 | Propiedad 53 |
| 192 | `Properties54` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 54 | Propiedad 54 |
| 193 | `Properties55` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 55 | Propiedad 55 |
| 194 | `Properties56` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 56 | Propiedad 56 |
| 195 | `Properties57` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 57 | Propiedad 57 |
| 196 | `Properties58` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 58 | Propiedad 58 |
| 197 | `Properties59` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 59 | Propiedad 59 |
| 198 | `Properties60` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 60 | Propiedad 60 |
| 199 | `Properties61` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 61 | Propiedad 61 |
| 200 | `Properties62` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 62 | Propiedad 62 |
| 201 | `Properties63` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 63 | Propiedad 63 |
| 202 | `Properties64` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 64 | Propiedad 64 |
| 203 | `CompanyRegistrationNumber` | Edm.String | Yes | Company Registration Number | Número de registro de la sociedad |
| 204 | `VerificationNumber` | Edm.String | Yes | Verification Number | Número de verificación |
| 205 | `DiscountBaseObject` | [DiscountGroupBaseObjectEnum](../Enums/DiscountGroupBaseObjectEnum.md) | Yes | Discount Base Object | Objeto base del descuento |
| 206 | `DiscountRelations` | [DiscountGroupRelationsEnum](../Enums/DiscountGroupRelationsEnum.md) | Yes | Discount Relations | Relaciones de descuento |
| 207 | `TypeReport` | [AssesseeTypeEnum](../Enums/AssesseeTypeEnum.md) | Yes | Type Report | Tipo de informe |
| 208 | `ThresholdOverlook` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Threshold Overlook | Omitir umbral |
| 209 | `SurchargeOverlook` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Surcharge Overlook | Omitir recargo |
| 210 | `Remark1` | Edm.Int32 | Yes | Remark 1 | Comentario 1 |
| 211 | `ConCerti` | Edm.String | Yes | Con Certi | Certificado de concesión |
| 212 | `DownPaymentInterimAccount` | Edm.String | Yes | Down Payment Interim Account | Cuenta transitoria de anticipos |
| 213 | `OperationCode347` | [OperationCode347Enum](../Enums/OperationCode347Enum.md) | Yes | Operation Code 347 | Código de operación (modelo 347) |
| 214 | `InsuranceOperation347` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Insurance Operation 347 | Operación de seguros (modelo 347) |
| 215 | `HierarchicalDeduction` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Hierarchical Deduction | Deducción jerárquica |
| 216 | `ShaamGroup` | [ShaamGroupEnum](../Enums/ShaamGroupEnum.md) | Yes | Shaam Group | Grupo Shaam (Israel) |
| 217 | `WithholdingTaxCertified` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Withholding Tax Certified | Retención certificada |
| 218 | `BookkeepingCertified` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Bookkeeping Certified | Contabilidad certificada |
| 219 | `PlanningGroup` | Edm.String | Yes | Planning Group | Grupo de planificación |
| 220 | `Affiliate` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Affiliate | Afiliado |
| 221 | `Industry` | Edm.Int32 | Yes | Industry | Ramo (industria) |
| 222 | `VatIDNum` | Edm.String | Yes | Vat ID Number | Número de identificación de IVA |
| 223 | `DatevAccount` | Edm.String | Yes | Datev Account | Cuenta DATEV |
| 224 | `DatevFirstDataEntry` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Datev First Data Entry | Primera entrada de datos DATEV |
| 225 | `UseShippedGoodsAccount` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Use Shipped Goods Account | Usar cuenta de mercancías enviadas |
| 226 | `GTSRegNo` | Edm.String | Yes | GTS Reg Number | N.º de registro GTS |
| 227 | `GTSBankAccountNo` | Edm.String | Yes | GTS Bank Account Number | N.º de cuenta bancaria GTS (China) |
| 228 | `GTSBillingAddrTel` | Edm.String | Yes | GTS Billing Addr Tel | Dirección y teléfono de facturación GTS |
| 229 | `ETaxWebSite` | Edm.Int32 | Yes | E Tax Web Site | Sitio web de impuestos electrónicos |
| 230 | `HouseBankIBAN` | Edm.String | Yes | House Bank IBAN | IBAN del banco propio |
| 231 | `VATRegistrationNumber` | Edm.String | Yes | VAT Registration Number | Número de registro de IVA |
| 232 | `RepresentativeName` | Edm.String | Yes | Representative Name | Nombre del representante |
| 233 | `IndustryType` | Edm.String | Yes | Industry Type | Tipo de ramo |
| 234 | `BusinessType` | Edm.String | Yes | Business Type | Tipo de negocio |
| 235 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 236 | `AutomaticPosting` | [AutomaticPostingEnum](../Enums/AutomaticPostingEnum.md) | Yes | Automatic Posting | Contabilización automática |
| 237 | `InterestAccount` | Edm.String | Yes | Interest Account | Cuenta de intereses |
| 238 | `FeeAccount` | Edm.String | Yes | Fee Account | Cuenta de cargos |
| 239 | `CampaignNumber` | Edm.Int32 | Yes | Campaign Number | Número de campaña |
| 240 | `AliasName` | Edm.String | Yes | Alias Name | Alias |
| 241 | `DefaultBlanketAgreementNumber` | Edm.Int32 | Yes | Default Blanket Agreement Number | Número de acuerdo global predeterminado |
| 242 | `EffectiveDiscount` | [DiscountGroupRelationsEnum](../Enums/DiscountGroupRelationsEnum.md) | Yes | Effective Discount | Descuento efectivo |
| 243 | `NoDiscounts` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Number Discounts | Sin descuentos |
| 244 | `EffectivePrice` | [EffectivePriceEnum](../Enums/EffectivePriceEnum.md) | Yes | Effective Price | Precio efectivo |
| 245 | `EffectivePriceConsidersPriceBeforeDiscount` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Effective Price Considers Price Before Discount | Precio efectivo considera precio antes de descuento |
| 246 | `GlobalLocationNumber` | Edm.String | Yes | Global Location Number | Número de localización global (GLN) |
| 247 | `EDISenderID` | Edm.String | Yes | EDI Sender ID | ID de remitente EDI |
| 248 | `EDIRecipientID` | Edm.String | Yes | EDI Recipient ID | ID de destinatario EDI |
| 249 | `ResidenNumber` | [ResidenceNumberTypeEnum](../Enums/ResidenceNumberTypeEnum.md) | Yes | Residen Number | Número de residencia |
| 250 | `RelationshipCode` | Edm.String | Yes | Relationship Code | Código de relación |
| 251 | `RelationshipDateFrom` | Edm.DateTimeOffset | Yes | Relationship Date From | Relación desde |
| 252 | `RelationshipDateTill` | Edm.DateTimeOffset | Yes | Relationship Date Till | Relación hasta |
| 253 | `UnifiedFederalTaxID` | Edm.String | Yes | Unified Federal Tax ID | ID fiscal federal unificado |
| 254 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 255 | `TypeOfOperation` | [TypeOfOperationEnum](../Enums/TypeOfOperationEnum.md) | Yes | Type Of Operation | Tipo de operación |
| 256 | `EndorsableChecksFromBP` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Endorsable Checks From Business Partner | Cheques endosables del socio de negocios |
| 257 | `AcceptsEndorsedChecks` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Accepts Endorsed Checks | Acepta cheques endosados |
| 258 | `OwnerCode` | Edm.Int32 | Yes | Owner Code | Código del titular |
| 259 | `BlockSendingMarketingContent` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Block Sending Marketing Content | Bloquear envío de contenido de marketing |
| 260 | `AgentCode` | Edm.String | Yes | Agent Code | Código de agente |
| 261 | `PriceMode` | [PriceModeEnum](../Enums/PriceModeEnum.md) | Yes | Price Mode | Modo de precio (neto/bruto) |
| 262 | `EDocGenerationType` | [EDocGenerationTypeEnum](../Enums/EDocGenerationTypeEnum.md) | Yes | E Document Generation Type | Tipo de generación del documento electrónico |
| 263 | `EDocStreet` | Edm.String | Yes | E Document Street | Calle (documento electrónico) |
| 264 | `EDocStreetNumber` | Edm.String | Yes | E Document Street Number | Número de calle (documento electrónico) |
| 265 | `EDocBuildingNumber` | Edm.Int32 | Yes | E Document Building Number | Número de edificio (documento electrónico) |
| 266 | `EDocZipCode` | Edm.String | Yes | E Document Zip Code | Código postal (documento electrónico) |
| 267 | `EDocCity` | Edm.String | Yes | E Document City | Ciudad (documento electrónico) |
| 268 | `EDocCountry` | Edm.String | Yes | E Document Country | País (documento electrónico) |
| 269 | `EDocDistrict` | Edm.String | Yes | E Document District | Distrito (documento electrónico) |
| 270 | `EDocRepresentativeFirstName` | Edm.String | Yes | E Document Representative First Name | Nombre del representante |
| 271 | `EDocRepresentativeSurname` | Edm.String | Yes | E Document Representative Surname | Apellido del representante |
| 272 | `EDocRepresentativeCompany` | Edm.String | Yes | E Document Representative Company | Sociedad del representante |
| 273 | `EDocRepresentativeFiscalCode` | Edm.String | Yes | E Document Representative Fiscal Code | Código fiscal del representante |
| 274 | `EDocRepresentativeAdditionalId` | Edm.String | Yes | E Document Representative Additional ID | ID adicional del representante |
| 275 | `EDocPECAddress` | Edm.String | Yes | E Document PEC Address | Dirección PEC (Italia) |
| 276 | `IPACodeForPA` | Edm.String | Yes | IPA Code For PA | Código IPA para la administración pública (Italia) |
| 277 | `UpdateDate` | Edm.DateTimeOffset | Yes | Update Date | Fecha de actualización |
| 278 | `UpdateTime` | Edm.TimeOfDay | Yes | Update Time | Hora de actualización |
| 279 | `ExemptionMaxAmountValidationType` | [ExemptionMaxAmountValidationTypeEnum](../Enums/ExemptionMaxAmountValidationTypeEnum.md) | Yes | Exemption Max Amount Validation Type | Tipo de validación del importe máximo de exención |
| 280 | `ECommerceMerchantID` | Edm.String | Yes | E Commerce Merchant ID | ID de comerciante de comercio electrónico |
| 281 | `UseBillToAddrToDetermineTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Use Bill To Addr To Determine Tax | Usar dirección de facturación para determinar impuestos |
| 282 | `CreateDate` | Edm.DateTimeOffset | Yes | Create Date | Fecha de creación |
| 283 | `CreateTime` | Edm.TimeOfDay | Yes | Create Time | Hora de creación |
| 284 | `DefaultTransporterEntry` | Edm.Int32 | Yes | Default Transporter Entry | Transportista predeterminado |
| 285 | `DefaultTransporterLineNumber` | Edm.Int32 | Yes | Default Transporter Line Number | Línea de transportista predeterminada |
| 286 | `FCERelevant` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | FCE Relevant | Relevante para FCE (Factura de Crédito Electrónica) |
| 287 | `FCEValidateBaseDelivery` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | FCE Validate Base Delivery | Validar entrega base para FCE |
| 288 | `MainUsage` | Edm.Int32 | Yes | Main Usage | Uso principal |
| 289 | `EBooksVATExemptionCause` | Edm.Int32 | Yes | E Books VAT Exemption Cause | Causa de exención de IVA (libros electrónicos) |
| 290 | `LegalText` | Edm.String | Yes | Legal Text | Texto legal |
| 291 | `DataVersion` | Edm.Int32 | Yes | Data Version | Versión de datos (control de concurrencia) |
| 292 | `ExchangeRateForIncomingPayment` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Exchange Rate For Incoming Payment | Tipo de cambio para pagos recibidos |
| 293 | `ExchangeRateForOutgoingPayment` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Exchange Rate For Outgoing Payment | Tipo de cambio para pagos efectuados |
| 294 | `CertificateDetails` | Edm.String | Yes | Certificate Details | Detalles del certificado |
| 295 | `DefaultCurrency` | Edm.String | Yes | Default Currency | Moneda predeterminada |
| 296 | `EORINumber` | Edm.String | Yes | EORI Number | Número EORI |
| 297 | `FCEAsPaymentMeans` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | FCE As Payment Means | FCE como medio de pago |
| 298 | `NotRelevantForMonthlyInvoice` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Not Relevant For Monthly Invoice | No relevante para factura mensual |
| 299 | `U_B1SYS_VATCtg` | Edm.String | Yes | [AR localization] VAT Category | [Loc. AR] Condición frente al IVA |
| 300 | `U_B1SYS_FiscIdType` | Edm.String | Yes | [AR localization] Fisc ID Type | [Loc. AR] Tipo de documento de identificación fiscal (CUIT, CUIL, DNI…) |
| 301 | `U_B1SYS_GrsIncId` | Edm.String | Yes | [AR localization] Grs Inc ID | [Loc. AR] Número de inscripción en Ingresos Brutos |
| 302 | `U_B1SYS_GrsIncCtg` | Edm.String | Yes | [AR localization] Grs Inc Category | [Loc. AR] Categoría de Ingresos Brutos |
| 303 | `U_B1SYS_IncTaxCtg` | Edm.String | Yes | [AR localization] Inc Tax Category | [Loc. AR] Categoría frente al impuesto a las ganancias |
| 304 | `U_B1SYS_ReproWebSta` | Edm.Int32 | Yes | [AR localization] Repro Web Sta | [Loc. AR] Estado en ReproWeb |
| 305 | `U_B1SYS_ShareFromO` | Edm.String | Yes | [AR localization] Share From O | [Loc. AR] Participación de otros (convenio multilateral) |
| 306 | `U_B1SYS_Employer` | Edm.String | Yes | [AR localization] Employer | [Loc. AR] Empleador |
| 307 | `U_B1SYS_MonoAct` | Edm.String | Yes | [AR localization] Mono Act | [Loc. AR] Actividad de monotributo |
| 308 | `U_B1SYS_MonoCtg` | Edm.String | Yes | [AR localization] Mono Category | [Loc. AR] Categoría de monotributo |
| 309 | `ElectronicProtocols` | Collection([ElectronicProtocol](../Tipos-Complejos/ElectronicProtocol.md)) | Yes | Electronic Protocols | Protocolos electrónicos |
| 310 | `BPAddresses` | Collection([BPAddress](../Tipos-Complejos/BPAddress.md)) | Yes | Business Partner Addresses | Direcciones del socio de negocios |
| 311 | `ContactEmployees` | Collection([ContactEmployee](../Tipos-Complejos/ContactEmployee.md)) | Yes | Contact Employees | Personas de contacto |
| 312 | `BPAccountReceivablePaybleCollection` | Collection([BPAccountReceivablePayble](../Tipos-Complejos/BPAccountReceivablePayble.md)) | Yes | Business Partner Account Receivable Payble Collection | Colección de cuentas asociadas por cobrar/pagar del socio de negocios |
| 313 | `BPPaymentMethods` | Collection([BPPaymentMethod](../Tipos-Complejos/BPPaymentMethod.md)) | Yes | Business Partner Payment Methods | Vías de pago del socio de negocios |
| 314 | `BPWithholdingTaxCollection` | Collection([BPWithholdingTax](../Tipos-Complejos/BPWithholdingTax.md)) | Yes | Business Partner Withholding Tax Collection | Colección de retenciones del socio de negocios |
| 315 | `BPPaymentDates` | Collection([BPPaymentDate](../Tipos-Complejos/BPPaymentDate.md)) | Yes | Business Partner Payment Dates | Fechas de pago del socio de negocios |
| 316 | `BPBranchAssignment` | Collection([BPBranchAssignmentItem](../Tipos-Complejos/BPBranchAssignmentItem.md)) | Yes | Business Partner Branch Assignment | Asignación de sucursales del socio de negocios |
| 317 | `BPBankAccounts` | Collection([BPBankAccount](../Tipos-Complejos/BPBankAccount.md)) | Yes | Business Partner Bank Accounts | Cuentas bancarias del socio de negocios |
| 318 | `BPFiscalTaxIDCollection` | Collection([BPFiscalTaxID](../Tipos-Complejos/BPFiscalTaxID.md)) | Yes | Business Partner Fiscal Tax ID Collection | Colección de identificaciones fiscales del socio de negocios |
| 319 | `DiscountGroups` | Collection([DiscountGroup](../Tipos-Complejos/DiscountGroup.md)) | Yes | Discount Groups | Grupos de descuento |
| 320 | `BPIntrastatExtension` | [BPIntrastatExtension](../Tipos-Complejos/BPIntrastatExtension.md) | Yes | Business Partner Intrastat Extension | Extensión Intrastat del socio de negocios |
| 321 | `BPBlockSendingMarketingContents` | Collection([BPBlockSendingMarketingContent](../Tipos-Complejos/BPBlockSendingMarketingContent.md)) | Yes | Business Partner Block Sending Marketing Contents | Bloqueos de envío de contenido de marketing del socio de negocios |
| 322 | `BPCurrenciesCollection` | Collection([BPCurrencies](../Tipos-Complejos/BPCurrencies.md)) | Yes | Business Partner Currencies Collection | Colección de monedas del socio de negocios |

## Navigation properties (93)

Use `GET /b1s/v2/BusinessPartners('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `SalesOpportunities` | Collection([SalesOpportunities](../Entidades/SalesOpportunities.md)) | [SalesOpportunities](SalesOpportunities.md) |  | Oportunidades de venta |
| `UserDefaultGroups` | Collection([UserDefaultGroup](../Entidades/UserDefaultGroups.md)) | [UserDefaultGroups](UserDefaultGroups.md) |  | Grupos de valores predeterminados de usuario |
| `LandedCosts` | Collection([LandedCost](../Entidades/LandedCosts.md)) | [LandedCosts](LandedCosts.md) |  | Costos de importación (landed costs) |
| `StockTransfers` | Collection([StockTransfer](../Entidades/StockTransfers.md)) | [StockTransfers](StockTransfers.md) |  | Transferencias de stock |
| `Warehouses` | Collection([Warehouse](../Entidades/Warehouses.md)) | [Warehouses](Warehouses.md) |  | Almacenes |
| `RecurringTransactionTemplates` | Collection([RecurringTransactionTemplate](../Entidades/RecurringTransactionTemplates.md)) | [RecurringTransactionTemplates](RecurringTransactionTemplates.md) |  | Plantillas de transacciones recurrentes |
| `PurchaseQuotations` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseQuotations](PurchaseQuotations.md) |  | Ofertas de compra |
| `VendorPayments` | Collection([Payment](../Entidades/VendorPayments.md)) | [VendorPayments](VendorPayments.md) |  | Pagos efectuados |
| `CorrectionInvoiceReversal` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionInvoiceReversal](CorrectionInvoiceReversal.md) |  | Anulación de factura de corrección de clientes |
| `CustomerEquipmentCards` | Collection([CustomerEquipmentCard](../Entidades/CustomerEquipmentCards.md)) | [CustomerEquipmentCards](CustomerEquipmentCards.md) |  | Tarjetas de equipo del cliente |
| `CorrectionInvoice` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionInvoice](CorrectionInvoice.md) |  | Factura de corrección de clientes |
| `PurchaseDeliveryNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseDeliveryNotes](PurchaseDeliveryNotes.md) |  | Pedidos de entrada de mercancías |
| `CorrectionPurchaseInvoice` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionPurchaseInvoice](CorrectionPurchaseInvoice.md) |  | Factura de corrección de proveedores |
| `PartnersSetups` | Collection([PartnersSetup](../Entidades/PartnersSetups.md)) | [PartnersSetups](PartnersSetups.md) |  | Configuración de socios |
| `InventoryGenEntries` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [InventoryGenEntries](InventoryGenEntries.md) |  | Entradas de mercancías |
| `BPVatExemptions` | Collection([BPVatExemptions](../Entidades/BPVatExemptions.md)) | [BPVatExemptions](BPVatExemptions.md) |  | Exenciones de IVA del socio de negocios |
| `BankPages` | Collection([BankPage](../Entidades/BankPages.md)) | [BankPages](BankPages.md) |  | Páginas de extracto bancario |
| `ServiceCalls` | Collection([ServiceCall](../Entidades/ServiceCalls.md)) | [ServiceCalls](ServiceCalls.md) |  | Llamadas de servicio |
| `Items` | Collection([Item](../Entidades/Items.md)) | [Items](Items.md) |  | Artículos |
| `EmployeesInfo` | Collection([EmployeeInfo](../Entidades/EmployeesInfo.md)) | [EmployeesInfo](EmployeesInfo.md) |  | Empleados |
| `AlternateCatNum` | Collection([AlternateCatNum](../Entidades/AlternateCatNum.md)) | [AlternateCatNum](AlternateCatNum.md) |  | Números de catálogo de socios de negocios |
| `Orders` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Orders](Orders.md) |  | Pedidos de cliente (órdenes de venta) |
| `GLAccountAdvancedRules` | Collection([GLAccountAdvancedRule](../Entidades/GLAccountAdvancedRules.md)) | [GLAccountAdvancedRules](GLAccountAdvancedRules.md) |  | Reglas avanzadas de cuentas de mayor |
| `ServiceContracts` | Collection([ServiceContract](../Entidades/ServiceContracts.md)) | [ServiceContracts](ServiceContracts.md) |  | Contratos de servicio |
| `InventoryGenExits` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [InventoryGenExits](InventoryGenExits.md) |  | Salidas de mercancías |
| `MaterialRevaluation` | Collection([MaterialRevaluation](../Entidades/MaterialRevaluation.md)) | [MaterialRevaluation](MaterialRevaluation.md) |  | Revalorización de inventario |
| `Drafts` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Drafts](Drafts.md) |  | Borradores de documentos |
| `InventoryTransferRequests` | Collection([StockTransfer](../Entidades/StockTransfers.md)) | [InventoryTransferRequests](InventoryTransferRequests.md) |  | Solicitudes de transferencia de stock |
| `ExportDeterminations` | Collection([ExportDetermination](../Entidades/ExportDeterminations.md)) | [ExportDeterminations](ExportDeterminations.md) |  | Determinaciones de exportación |
| `ReturnRequest` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [ReturnRequest](ReturnRequest.md) |  | Solicitudes de devolución de clientes |
| `DeliveryNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [DeliveryNotes](DeliveryNotes.md) |  | Entregas |
| `PurchaseInvoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseInvoices](PurchaseInvoices.md) |  | Facturas de proveedores |
| `StockTransferDrafts` | Collection([StockTransfer](../Entidades/StockTransfers.md)) | [StockTransferDrafts](StockTransferDrafts.md) |  | Borradores de transferencias de stock |
| `SelfInvoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [SelfInvoices](SelfInvoices.md) |  | Autofacturas |
| `BlanketAgreements` | Collection([BlanketAgreement](../Entidades/BlanketAgreements.md)) | [BlanketAgreements](BlanketAgreements.md) |  | Acuerdos globales |
| `Invoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Invoices](Invoices.md) |  | Facturas de clientes |
| `CreditNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CreditNotes](CreditNotes.md) |  | Notas de crédito de clientes |
| `PaymentDrafts` | Collection([Payment](../Entidades/VendorPayments.md)) | [PaymentDrafts](PaymentDrafts.md) |  | Borradores de pagos |
| `DeductionTaxHierarchies` | Collection([DeductionTaxHierarchy](../Entidades/DeductionTaxHierarchies.md)) | [DeductionTaxHierarchies](DeductionTaxHierarchies.md) |  | Jerarquías de deducción de retenciones |
| `Contacts` | Collection([Contact](../Entidades/Contacts.md)) | [Contacts](Contacts.md) |  | Contactos |
| `PurchaseCreditNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseCreditNotes](PurchaseCreditNotes.md) |  | Notas de crédito de proveedores |
| `BusinessPartnerGroup` | [BusinessPartnerGroup](../Entidades/BusinessPartnerGroups.md) | [BusinessPartnerGroups](BusinessPartnerGroups.md) | GroupCode → Code | Grupos de socios de negocios |
| `PaymentTermsType` | [PaymentTermsType](../Entidades/PaymentTermsTypes.md) | [PaymentTermsTypes](PaymentTermsTypes.md) | PayTermsGrpCode → GroupNumber | Condiciones de pago |
| `PriceList` | [PriceList](../Entidades/PriceLists.md) | [PriceLists](PriceLists.md) | PriceListNum → PriceListNo | Lista de precios |
| `CommissionGroup` | [CommissionGroup](../Entidades/CommissionGroups.md) | [CommissionGroups](CommissionGroups.md) | CommissionGroupCode → CommissionGroupCode | Grupo de comisiones |
| `SalesPerson` | [SalesPerson](../Entidades/SalesPersons.md) | [SalesPersons](SalesPersons.md) | SalesPersonCode → SalesEmployeeCode | Empleado de ventas |
| `Currency2` | [Currency](../Entidades/Currencies.md) | [Currencies](Currencies.md) | Currency → Code | Monedas |
| `ChartOfAccount` | [ChartOfAccount](../Entidades/ChartOfAccounts.md) | [ChartOfAccounts](ChartOfAccounts.md) | RateDiffAccount → Code | Plan de cuentas (cuentas de mayor) |
| `Country2` | [Country](../Entidades/Countries.md) | [Countries](Countries.md) | Country → Code | Países/Regiones |
| `VatGroup2` | [VatGroup](../Entidades/VatGroups.md) | [VatGroups](VatGroups.md) | VatGroup → Code | Grupos de impuestos (IVA) |
| `ShippingType2` | [ShippingType](../Entidades/ShippingTypes.md) | [ShippingTypes](ShippingTypes.md) | ShippingType → Code | Clases de expedición |
| `FactoringIndicator` | [FactoringIndicator](../Entidades/FactoringIndicators.md) | [FactoringIndicators](FactoringIndicators.md) | Indicator → IndicatorCode | Indicadores de factoring |
| `CreditCard` | [CreditCard](../Entidades/CreditCards.md) | [CreditCards](CreditCards.md) | CreditCardCode → CreditCardCode | Tarjeta de crédito |
| `BPPriority` | [BPPriority](../Entidades/BPPriorities.md) | [BPPriorities](BPPriorities.md) | Priority → Priority | Prioridades de socios de negocios |
| `Forms1099` | [Forms1099](../Entidades/Forms1099.md) | [Forms1099](Forms1099.md) | FormCode1099 → FormCode | Formularios 1099 |
| `WizardPaymentMethod` | [WizardPaymentMethod](../Entidades/WizardPaymentMethods.md) | [WizardPaymentMethods](WizardPaymentMethods.md) | PeymentMethodCode → PaymentMethodCode | Vías de pago del asistente de pagos |
| `DunningLetter` | [DunningLetter](../Entidades/DunningLetters.md) | [DunningLetters](DunningLetters.md) | DunningLevel → RowNumber | Cartas de reclamación |
| `PaymentBlock2` | [PaymentBlock](../Entidades/PaymentBlocks.md) | [PaymentBlocks](PaymentBlocks.md) | PaymentBlockDescription → AbsEntry | Bloqueos de pago |
| `WithholdingTaxCode` | [WithholdingTaxCode](../Entidades/WithholdingTaxCodes.md) | [WithholdingTaxCodes](WithholdingTaxCodes.md) | WTCode → WTCode | Códigos de retención de impuestos |
| `EmployeeInfo` | [EmployeeInfo](../Entidades/EmployeesInfo.md) | [EmployeesInfo](EmployeesInfo.md) | DefaultTechnician → EmployeeID | Empleados |
| `Territory2` | [Territory](../Entidades/Territories.md) | [Territories](Territories.md) | Territory → TerritoryID | Territorios |
| `Project` | [Project](../Entidades/Projects.md) | [Projects](Projects.md) | ProjectCode → Code | Proyecto |
| `SalesTaxCode` | [SalesTaxCode](../Entidades/SalesTaxCodes.md) | [SalesTaxCodes](SalesTaxCodes.md) | VatGroupLatinAmerica → Code | Códigos del impuesto sobre ventas |
| `DunningTerm2` | [DunningTerm](../Entidades/DunningTerms.md) | [DunningTerms](DunningTerms.md) | DunningTerm → Code | Condiciones de reclamación |
| `UserLanguage` | [UserLanguage](../Entidades/UserLanguages.md) | [UserLanguages](UserLanguages.md) | LanguageCode → Code | Idiomas de usuario |
| `DeductionTaxGroup` | [DeductionTaxGroup](../Entidades/DeductionTaxGroups.md) | [DeductionTaxGroups](DeductionTaxGroups.md) | WithholdingTaxDeductionGroup → GroupKey | Grupos de deducción de retenciones |
| `ClosingDateProcedure` | [ClosingDateProcedure](../Entidades/ClosingDateProcedure.md) | [ClosingDateProcedure](ClosingDateProcedure.md) | ClosingDateProcedureNumber → ClosingDateNum | Procedimiento de fecha de cierre |
| `BankChargesAllocationCode2` | [BankChargesAllocationCode](../Entidades/BankChargesAllocationCodes.md) | [BankChargesAllocationCodes](BankChargesAllocationCodes.md) | BankChargesAllocationCode → Code | Códigos de imputación de comisiones bancarias |
| `Industry2` | [Industry](../Entidades/Industries.md) | [Industries](Industries.md) | Industry → IndustryCode | Ramos (industrias) |
| `TaxWebSite` | [TaxWebSite](../Entidades/TaxWebSites.md) | [TaxWebSites](TaxWebSites.md) | ETaxWebSite → AbsEntry | Sitios web de impuestos |
| `Campaign` | [Campaign](../Entidades/Campaigns.md) | [Campaigns](Campaigns.md) | CampaignNumber → CampaignNumber | Campañas |
| `BlanketAgreement` | [BlanketAgreement](../Entidades/BlanketAgreements.md) | [BlanketAgreements](BlanketAgreements.md) | DefaultBlanketAgreementNumber → AgreementNo | Acuerdo global |
| `EWBTransporter` | [EWBTransporter](../Entidades/EWBTransporters.md) | [EWBTransporters](EWBTransporters.md) | DefaultTransporterEntry → AbsEntry | Transportistas EWB |
| `ProductionOrders` | Collection([ProductionOrder](../Entidades/ProductionOrders.md)) | [ProductionOrders](ProductionOrders.md) |  | Órdenes de fabricación |
| `DownPayments` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [DownPayments](DownPayments.md) |  | Facturas de anticipo de clientes |
| `SalesTaxInvoices` | Collection([SalesTaxInvoice](../Entidades/SalesTaxInvoices.md)) | [SalesTaxInvoices](SalesTaxInvoices.md) |  | Facturas de impuestos de venta |
| `PurchaseDownPayments` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseDownPayments](PurchaseDownPayments.md) |  | Facturas de anticipo de proveedores |
| `PurchaseReturns` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseReturns](PurchaseReturns.md) |  | Devoluciones de mercancías a proveedores |
| `Activities` | Collection([Activity](../Entidades/Activities.md)) | [Activities](Activities.md) |  | Actividades |
| `PurchaseOrders` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseOrders](PurchaseOrders.md) |  | Pedidos de compra (órdenes de compra) |
| `SelfCreditMemos` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [SelfCreditMemos](SelfCreditMemos.md) |  | Autonotas de crédito |
| `Quotations` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Quotations](Quotations.md) |  | Ofertas de ventas (cotizaciones) |
| `Returns` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Returns](Returns.md) |  | Devoluciones de clientes |
| `DepreciationAreas` | Collection([DepreciationArea](../Entidades/DepreciationAreas.md)) | [DepreciationAreas](DepreciationAreas.md) |  | Áreas de amortización |
| `SpecialPrices` | Collection([SpecialPrice](../Entidades/SpecialPrices.md)) | [SpecialPrices](SpecialPrices.md) |  | Precios especiales |
| `ProjectManagements` | Collection([PM_ProjectDocumentData](../Entidades/ProjectManagements.md)) | [ProjectManagements](ProjectManagements.md) |  | Gestión de proyectos |
| `GoodsReturnRequest` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [GoodsReturnRequest](GoodsReturnRequest.md) |  | Solicitudes de devolución de mercancías |
| `CorrectionPurchaseInvoiceReversal` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionPurchaseInvoiceReversal](CorrectionPurchaseInvoiceReversal.md) |  | Anulación de factura de corrección de proveedores |
| `IncomingPayments` | Collection([Payment](../Entidades/VendorPayments.md)) | [IncomingPayments](IncomingPayments.md) |  | Pagos recibidos |
| `SpecificWTHAmountsService` | Collection([SpecificWTHAmounts](../Entidades/SpecificWTHAmountsService.md)) | [SpecificWTHAmountsService](SpecificWTHAmountsService.md) |  | Importes de retención específicos |
| `PurchaseRequests` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseRequests](PurchaseRequests.md) |  | Solicitudes de compra |
| `PurchaseTaxInvoices` | Collection([PurchaseTaxInvoice](../Entidades/PurchaseTaxInvoices.md)) | [PurchaseTaxInvoices](PurchaseTaxInvoices.md) |  | Facturas de impuestos de compra |
| `BusinessPlaces` | Collection([BusinessPlace](../Entidades/BusinessPlaces.md)) | [BusinessPlaces](BusinessPlaces.md) |  | Lugares de negocios |

## Service operations that use this type

- [`BusinessPartnersService_InitData`](../Servicios/BusinessPartnersService.md#businesspartnersservice_initdata)
