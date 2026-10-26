# 11–12. Appendices: Service Layer vs. DI API, and Metadata Naming Differences

> Source: *Working with SAP Business One Service Layer* v1.29, chapters 11–12 (paraphrased technical reference).
>
> **Resumen (ES):** equivalencias entre llamadas de la DI API (SAPbobsCOM) y del Service Layer para CRUD, servicios de la sociedad, transacciones, consultas, UDOs y UDFs; y diferencias de nombres de colecciones, objetos y propiedades entre ambos.

## 11. DI API → Service Layer equivalents

| Task | DI API (C#) | Service Layer | Tarea (ES) |
|---|---|---|---|
| Create order | `var order = (Documents)oCompany.GetBusinessObject(BoObjectTypes.oOrders); order.CardCode = "c001"; order.DocDate = DateTime.Today; order.DocDueDate = DateTime.Today; order.Lines.ItemCode = "i001"; order.Lines.Quantity = 1; order.Lines.TaxCode = "T1"; order.Lines.UnitPrice = 100; order.Lines.Add(); int ret = order.Add();` | `POST /Orders {"CardCode": "c001", "DocDate": "2014-04-01", "DocDueDate": "2014-04-01", "DocumentLines": [ {"ItemCode": "i001", "UnitPrice": 100, "Quantity": 1, "TaxCode": "T1"} ]}` | Crear pedido |
| Read order | `order.GetByKey(2); order.GetAsXML();` | `GET /Orders(2)` | Leer |
| Update order | `order.GetByKey(2); order.Comments = "New comments"; order.Update();` | `PATCH /Orders(2) {"Comments": "New comments"}` | Actualizar |
| Delete | `order.GetByKey(2); order.Remove();` | `DELETE /Orders(2)` | Borrar |
| Company info | `var cs = oCompany.GetCompanyService(); var ci = cs.GetCompanyInfo();` | `POST /CompanyService_GetCompanyInfo` | Info de la sociedad |
| Update company info | `ci.AutoCreateCustomerEqCard = BoYesNoEnum.tYES; cs.UpdateCompanyInfo(ci);` | `POST /CompanyService_UpdateCompanyInfo {"CompanyInfo": {"Version": 910160, "EnableExpensesManagement": "tYES", ..., "AutoCreateCustomerEqCard": "tYES", ...}}` (service calls = OData Actions / FunctionImports) | Actualizar info |
| Transaction | `oCompany.StartTransaction(); items.Add(); ... items.Update(); oCompany.EndTransaction(BoWfTransOpt.wf_Commit);` (or `wf_RollBack`) | `$batch` with one **change set** (e.g. `POST /b1s/v1/Items` then `PATCH /b1s/v1/Items('item_001')`); it commits automatically if all parts succeed — the client can't roll back explicitly, and complex logic can't be enclosed like in DI API | Transacción |
| Query | `var rs = (Recordset)oCompany.GetBusinessObject(BoObjectTypes.BoRecordset); rs.DoQuery("Select \"CardCode\", \"CardName\" from OCRD where \"CardCode\" >= 'C001'"); while (!rs.EoF) {...; rs.MoveNext();}` | `GET /BusinessPartners?$select=CardCode, CardName&$filter=CardCode ge 'C001'` (JSON; to iterate like a recordset use an OData client library, e.g. WCF) | Consulta |
| Create UDT | `var t = (UserTablesMD)oCompany.GetBusinessObject(BoObjectTypes.oUserTables); t.TableName = "MyOrder"; t.TableType = BoUTBTableType.bott_Document; t.Add();` | `POST /UserTablesMD {"TableName": "MyOrder", "TableDescription": "My Orders", "TableType": "bott_Document"}` | Crear UDT |
| Create UDF | `var f = (UserFieldsMD)oCompany.GetBusinessObject(BoObjectTypes.oUserFields); f.Name = "CustomerName"; f.Type = BoFieldTypes.db_Alpha; f.Size = 10; f.SubType = BoFldSubTypes.st_None; f.TableName = "@MYORDER"; f.Add();` | `POST /UserFieldsMD {"Name": "CustomerName", "Type": "db_Alpha", "Size": 10, "Description": "Customer name", "SubType": "st_None", "TableName": "@MYORDER"}` | Crear UDF |
| Register UDO | `var u = (UserObjectsMD)oCompany.GetBusinessObject(BoObjectTypes.oUserObjectsMD); u.Code = "MyOrders"; u.Name = "MyOrder"; u.TableName = "MyOrder"; u.ObjectType = BoUDOObjType.boud_Document; u.ChildTables.TableName = "MyOrderLines"; u.ChildTables.ObjectName = "MyOrderLines"; u.ChildTables.Add(); u.Add();` | `POST /UserObjectsMD {"Code": "MyOrders", "Name": "MyOrder", "TableName": "MyOrder", "ObjectType": "boud_Document", "UserObjectMD_ChildTables": [ {"TableName": "MyOrderLines", "ObjectName": "MyOrderLines"} ]}` | Registrar UDO |
| UDO CRUD/query | — | `POST /MyOrders {...,"MyOrderLinesCollection": [...]}`, `GET /MyOrders(10)`, `GET /MyOrders?$select=U_CustomerName, U_DocTotal&$filter=U_CustomerName eq 'c1' and U_DocTotal gt 1000` | CRUD de UDO |
| Read UDF definition | `f.GetByKey("OCRD", 0)` (composite key) | `GET /UserFieldsMD(TableName='OCRD', FieldID=0)` | Leer definición de UDF |
| Update / delete UDF definition | `f.Description = "New Description"; f.Update();` / `f.Remove();` | `PATCH /UserFieldsMD(TableName='OCRD', FieldID=0) {"Description": "New Description"}` / `DELETE ...` | Modificar/borrar UDF |
| Entity with UDF | `bp.UserFields.Fields.Item(0).Value = "udf value"; bp.Add();` / `.Update()` | UDF is a normal property: `POST /BusinessPartners {"CardCode": "bp_001", "CardName": "bp_001_name", "U_u1": "udf value"}`; `GET /BusinessPartners?$filter=startswith(U_u1, 'udf ')`; `PATCH /BusinessPartners('bp_001') {"U_u1": "..."}` | Entidad con UDF |

The full UDO creation sequence is identical in both APIs: (1) main UDT, (2) its UDFs, (3) child UDT, (4) its UDFs, (5) register the UDO — see [03-08](03-08-UDF-UDT-UDO.md).

## 12. Metadata naming differences (SL reuses DI core metadata, adjusted for OData)

To see collection names: SL `GET /b1s/v1/$metadata`; DI API `GetBusinessObjectXmlSchema`.

### 12.1 Collection (sub-object) names

| Service Layer | DI API | Contexto (ES) |
|---|---|---|
| AccountSegmentationsCategories | Categories | Categorías de segmentación |
| BPAccountReceivablePaybleCollection | BPAccountReceivablePayble | Cuentas asociadas del SN |
| BPFiscalTaxIDCollection | BPFiscalTaxID | IDs fiscales del SN |
| BPWithholdingTaxCollection | BPWithholdingTax | Retenciones del SN |
| BillOfExchangeTransBankPages | BillOfExchangeTrans_BankPages | Letras de cambio – páginas bancarias |
| BillOfExchangeTransDeposits | BillOfExchangeTrans_Deposits | Letras de cambio – depósitos |
| BillOfExchangeTransactionLines | BillOfExchangeTransaction_Lines | Letras de cambio – líneas |
| BudgetCostAccountingLines | BudgetCostAccounting_Lines | Presupuesto – contabilidad de costos |
| BudgetLines | Budget_Lines | Presupuesto – líneas |
| BusinessPlaceIENumbers | IENumbers | Lugar de negocios – números IE |
| BusinessPlaceTributaryInfos | TributaryInfos | Lugar de negocios – info tributaria |
| CashFlowAssignments | PrimaryFormItems | Asignaciones de flujo de caja |
| CheckInListParams | CheckIns | Check-ins |
| DocFreightEBooksDetails | Doc_Freight_EBooks_Doc_Details | Gastos – libros electrónicos |
| DocsInWTGroupsCollection | DocsInWTGroups | Documentos en grupos de retención |
| DocumentAdditionalExpenses | DocumentsAdditionalExpenses | Gastos adicionales del documento |
| DocumentInstallments | Document_Installments | Cuotas |
| DocumentLineAdditionalExpenses | Document_LinesAdditionalExpenses | Gastos adicionales de línea |
| DocumentLines | Document_Lines | Líneas del documento |
| DocumentReferences | DocumentReference | Referencias de documentos |
| DocumentSpecialLines | Document_SpecialLines | Líneas especiales |
| EBooksDetails | Line_EBooks_Doc_Details | Libros electrónicos |
| EmployeeAbsenceInfoLines | EmployeeAbsenceInfo | Ausencias |
| EmployeeEducationInfoLines | EmployeeEducationInfo | Formación |
| EmployeePreviousEmpoymentInfoLines | EmployeePrevEmpoymentInfo | Empleos anteriores |
| EmployeeReviewsInfoLines | EmployeeReviewsInfo | Evaluaciones |
| EmployeeRolesInfoLines | EmployeeRolesInfo | Funciones |
| EmployeeSavingsPaymentInfoLines | EmployeeSavingsPaymentInfo | Pagos de ahorro |
| FieldIDs | FormattedSearchFields | Campos de búsqueda formateada |
| InventoryCountingDocumentReferencesCollection | InventoryCountingDocumentReferences | Recuento – referencias |
| InventoryPostingDocumentReferencesCollection | InventoryPostingDocumentReferences | Contabilización de inventario – referencias |
| ItemBarCodeCollection | ItemBarCodes | Códigos de barras |
| ItemCycleCounts | ItemCycleCount | Recuentos cíclicos |
| ItemDepreciationParameters | ItemDepreciationParam | Parámetros de amortización |
| ItemDistributionRules | ItemDistributionRule | Normas de reparto |
| ItemGroupsWarehouseInfos | ItemGroups_WarehouseInfo | Grupo de artículos – almacenes |
| ItemLocalizationInfos | LocalizationInfos | Localización |
| ItemPeriodControls | ItemPeriodControl | Control de períodos |
| ItemPrices | Items_Prices | Precios del artículo |
| ItemUnitOfMeasurementCollection | ItemUnitOfMeasurement | Unidades de medida |
| ItemUoMPackageCollection | ItemUoMPackage | Paquetes por UdM |
| ItemWarehouseInfoCollection | ItemWarehouseInfo | Datos por almacén |
| JournalEntryLines | JournalEntries_Lines | Líneas de asiento |
| LineFreightEBooksDetails | Line_Freight_EBooks_Doc_Details | Gastos de línea – libros electrónicos |
| MaterialRevaluationDocumentReferencesCollection | MaterialRevaluationDocumentReferences | Revalorización – referencias |
| MaterialRevaluationLines | MaterialRevaluation_lines | Revalorización – líneas |
| PaymentAccounts | Payments_Accounts | Pagos – cuentas |
| PaymentChecks | Payments_Checks | Pagos – cheques |
| PaymentCreditCards | Payments_CreditCards | Pagos – tarjetas |
| PaymentDocumentReferencesCollection | Payments_DocumentReferences | Pagos – referencias |
| PaymentInvoices | Payments_Invoices | Pagos – facturas |
| PickListsLines | PickLists_Lines | Picking – líneas |
| ProductTreeLines | ProductTrees_Lines | Lista de materiales – líneas |
| ProductTreeStages | ProductTrees_Stages | Lista de materiales – etapas |
| ProductionOrderLines | ProductionOrders_Lines | Orden de fabricación – líneas |
| ProductionOrdersDocumentReferences | ProductionOrders_DocumentReferences | Orden de fabricación – referencias |
| ProductionOrdersSalesOrderLines | ProductionOrders_SalesOrderLines | Orden de fabricación – líneas de pedido |
| ProductionOrdersStages | ProductionOrders_Stages | Orden de fabricación – etapas |
| ProgressiveTax_Lines | WithholdingTaxCodes_ProgressiveTax_Lines | Impuesto progresivo |
| SNBLinesCollection | SNBLines | Series/lotes |
| SalesForecastLines | SalesForecast_Lines | Previsión de ventas |
| SpecialPriceDataAreas | SpecialPricesDataAreas | Precios especiales – fechas |
| SpecialPriceQuantityAreas | SpecialPricesQuantityAreas | Precios especiales – cantidades |
| StockTransferLines | StockTransfer_Lines | Transferencia – líneas |
| StockTransferTaxExtension | StockTransfer_TaxExtension | Transferencia – impuestos |
| UserPermission | UserPermissionItem | Permisos de usuario |
| WTGroupsCollection | WTGroups | Grupos de retención |
| WithholdingTaxCertificatesCollection | WithholdingTaxCertificates | Certificados de retención |
| WithholdingTaxDataCollection | WithholdingTaxData | Datos de retención |
| WithholdingTaxDataWTXCollection | WithholdingTaxDataWTX | Datos de retención WTX |

### 12.2 Business object names (plural in SL)

| Service Layer | DI API | Objeto (ES) |
|---|---|---|
| InventoryGenExits | InventoryGenExit | Salidas de mercancías |
| InventoryGenEntries | InventoryGenEntry | Entradas de mercancías |

### 12.3 Property names (suffix `Property` when equal to the containing type)

| Service Layer | DI API | Propiedad (ES) |
|---|---|---|
| BatchNumber.BatchNumberProperty | BatchNumber.BatchNumber | Número de lote |
| Activity.ActivityProperty | Activity.Activity | Actividad |
| PeriodCategory.PeriodCategoryProperty | PeriodCategory.PeriodCategory | Categoría de período |
