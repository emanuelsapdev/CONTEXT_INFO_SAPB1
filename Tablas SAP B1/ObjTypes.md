# Lista de ObjTypes – SAP Business One

Referencia de tablas, claves primarias y Object Type (ObjType) de SAP Business One.

Fuente: https://freeconsulit.com/2023/07/06/list-objtype-sap-b1/ (Free Consul IT, publicado el 06/07/2023). Datos transcriptos tal cual figuran en la fuente; verificar contra la versión de B1 en uso.

| Tabla | Descripción | Description | Primary Key | ObjType |
|---|---|---|---|---|
| OACT | Cuentas de mayor | G/L Accounts | AcctCode | 1 |
| OCRD | Socios de negocios | Business Partner | CardCode | 2 |
| ODSC | Códigos bancarios | Bank Codes | AbsEntry | 3 |
| OITM | Artículos | Items | ItemCode | 4 |
| OVTG | Definición de impuestos | Tax Definition | Code | 5 |
| OPLN | Listas de precios | Price Lists | ListNum | 6 |
| OSPP | Precios especiales | Special Prices | CardCode, ItemCode | 7 |
| OITG | Propiedades de artículo | Item Properties | ItmsTypCod | 8 |
| ORTM | Diferencias de cambio | Rate Differences | LineNum, IsSysCurr | 9 |
| OCRG | Grupos de socios de negocios | Card Groups | GroupCode | 10 |
| OCPR | Personas de contacto | Contact Persons | CntctCode | 11 |
| OUSR | Usuarios | Users | USERID | 12 |
| OINV | Factura de clientes | A/R Invoice | DocEntry | 13 |
| ORIN | Nota de crédito de clientes | A/R Credit Memo | DocEntry | 14 |
| ODLN | Entrega | Delivery | DocEntry | 15 |
| ORDN | Devoluciones | Returns | DocEntry | 16 |
| ORDR | Orden de venta | Sales Order | DocEntry | 17 |
| OPCH | Factura de proveedores | A/P Invoice | DocEntry | 18 |
| ORPC | Nota de crédito de proveedores | A/P Credit Memo | DocEntry | 19 |
| OPDN | Recepción de mercancía | Goods Receipt PO | DocEntry | 20 |
| ORPD | Devolución de mercancía | Goods Return | DocEntry | 21 |
| OPOR | Orden de compra | Purchase Order | DocEntry | 22 |
| OQUT | Cotización de venta | Sales Quotation | DocEntry | 23 |
| ORCT | Pago recibido | Incoming Payment | DocEntry | 24 |
| ODPS | Depósito | Deposit | DeposId | 25 |
| OMTH | Historial de conciliación | Reconciliation History | MthAcctCod, IsInternal, MatchNum | 26 |
| OCHH | Registro de cheques | Check Register | CheckKey | 27 |
| OBTF | Entrada de asiento de diario | Journal Voucher Entry | BatchNum, TransId | 28 |
| OBTD | Lista de asientos de diario | Journal Vouchers List | BatchNum | 29 |
| OJDT | Asiento de diario | Journal Entry | TransId | 30 |
| OITW | Artículos – Almacén | Items – Warehouse | ItemCode, WhsCode | 31 |
| OADP | Preferencias de impresión | Print Preferences | PrintId | 32 |
| OCLG | Actividades | Activities | ClgCode | 33 |
| ORCR | Contabilidad recurrente | Recurring Postings | RcurCode, Instance | 34 |
| ONNM | Numeración de documentos | Document Numbering | ObjectCode, DocSubType | 35 |
| OCRC | Tarjetas de crédito | Credit Cards | CreditCard | 36 |
| OCRN | Códigos de moneda | Currency Codes | CurrCode | 37 |
| OIDX | Códigos de índice CPI | CPI Codes | IdexCode | 38 |
| OADM | Administración | Administration | Code | 39 |
| OCTG | Términos de pago | Payment Terms | GroupNum | 40 |
| OPRF | Preferencias | Preferences | FormNumber, UserSign | 41 |
| OBNK | Extracto bancario externo | External Bank Statement Received | AcctCode, Sequence | 42 |
| OMRC | Fabricantes | Manufacturers | FirmCode | 43 |
| OCQG | Propiedades de socios de negocios | Card Properties | GroupCode | 44 |
| OTRC | Códigos de entrada de diario | Journal Entry Codes | TrnsCode | 45 |
| OVPM | Pagos salientes | Outgoing Payments | DocEntry | 46 |
| OSRL | Números de serie | Serial Numbers | ItemCode, SerialNum | 47 |
| OALC | Gastos de carga | Loading Expenses | AlcCode | 48 |
| OSHP | Tipos de entrega | Delivery Types | TrnspCode | 49 |
| OLGT | Unidades de longitud | Length Units | UnitCode | 50 |
| OWGT | Unidades de peso | Weight Units | UnitCode | 51 |
| OITB | Grupos de artículos | Item Groups | ItmsGrpCod | 52 |
| OSLP | Empleado de ventas | Sales Employee | SlpCode | 53 |
| OFLT | Criterios de selección de informes | Report – Selection Criteria | FormNum, UserSign, FilterName | 54 |
| OTRT | Plantillas de contabilización | Posting Templates | TrtCode | 55 |
| OARG | Grupos de aduana | Customs Groups | CstGrpCode | 56 |
| OCHO | Cheques de pago | Checks for Payment | CheckKey | 57 |
| OINM | Diario de almacén | Whse Journal | TransNum, Instance | 58 |
| OIGN | Recepción de mercancía | Goods Receipt | DocEntry | 59 |
| OIGE | Emisión de mercancía | Goods Issue | DocEntry | 60 |
| OPRC | Centro de costos | Cost Center | PrcCode | 61 |
| OOCR | Tasa de costos | Cost Rate | OcrCode | 62 |
| OPRJ | Códigos de proyecto | Project Codes | PrjCode | 63 |
| OWHS | Almacenes | Warehouses | WhsCode | 64 |
| OCOG | Grupos de comisión | Commission Groups | GroupCode | 65 |
| OITT | Árbol | Product Tree | Code | 66 |
| OWTR | Traslados | Inventory Transfer | DocEntry | 67 |
| OWKO | Etapas de trabajos | Production Instructions | OrderNum | 68 |
| OIPF | Factura de proveedores independientes | Landed Costs | DocEntry | 69 |
| OCRP | Métodos de pagos | Payment Methods | CrTypeCode | 70 |
| OCDT | Pago con tarjeta de crédito | Credit Card Payment | Code | 71 |
| OCRH | Gestión de tarjetas de crédito | Credit Card Management | AbsId, Instance | 72 |
| OSCN | Número de catálogo de cliente/proveedor | Customer/Vendor Cat. No. | ItemCode, CardCode, Substitute | 73 |
| OCRV | Pagos con tarjeta de crédito | Credit Payments | AbsId, PayId, Instance | 74 |
| ORTT | Tasas de CPI y FC | CPI and FC Rates | RateDate, Currency | 75 |
| ODPT | Depósito con fecha futura | Postdated Deposit | DeposId | 76 |
| OBGT | Presupuesto | Budget | AbsId | 77 |
| OBGD | Método de asignación de costos de presupuesto | Budget Cost Assess. Mthd | BgdCode | 78 |
| ORCN | Cadenas minoristas | Retail Chains | ChainCode | 79 |
| OALT | Plantilla de alertas | Alerts Template | Code | 80 |
| OALR | Alertas | Alerts | Code | 81 |
| OAIB | Alertas recibidas | Received Alerts | AlertCode, UserSign | 82 |
| OAOB | Mensaje enviado | Message Sent | AlertCode, UserSign | 83 |
| OCLS | Asuntos de actividad | Activity Subjects | Code | 84 |
| OSPG | Precios especiales para grupos | Special Prices for Groups | CardCode, ObjType, ObjKey | 85 |
| SPRG | Inicio de aplicación | Application Start | LineNum, UserCode | 86 |
| OMLS | Lista de distribución | Distribution List | Code | 87 |
| OENT | Tipos de envío | Shipping Types | DocEntry | 88 |
| OSAL | Saliente | Outgoing | DocEntry | 89 |
| OTRA | Transición | Transition | DocEntry | 90 |
| OBGS | Escenario de presupuesto | Budget Scenario | AbsId | 91 |
| OIRT | Tasas de interés | Interest Prices | Numerator | 92 |
| OUDG | Valores predeterminados del usuario | User Defaults | Code | 93 |
| OSRI | Números de serie para artículos | Serial Numbers for Items | ItemCode, SysSerial | 94 |
| OFRT | Plantillas de informe financiero | Financial Report Templates | AbsId | 95 |
| OFRC | Categorías de informes financieros | Financial Report Categories | TemplateId, CatId | 96 |
| OOPR | Oportunidad | Opportunity | OpprId | 97 |
| OOIN | Interés | Interest | Num | 98 |
| OOIR | Nivel de interés | Interest Level | Num | 99 |
| OOSR | Fuente de información | Information Source | Num | 100 |
| OOST | Etapa de oportunidad | Opportunity Stage | Num | 101 |
| OOFR | Causa de defecto | Defect Cause | Num | 102 |
| OCLT | Tipos de actividad | Activity Types | Code | 103 |
| OCLO | Ubicación de reuniones | Meetings Location | Code | 104 |
| OISR | Llamadas de servicio | Service Calls | RequestNum | 105 |
| OIBT | Lote para artículo | Batch No. for Item | ItemCode, BatchNum, WhsCode | 106 |
| OALI | Artículos alternativos 2 | Alternative Items 2 | OrigItem, AltItem | 107 |
| OPRT | Socios | Partners | PrtId | 108 |
| OCMT | Competidores | Competitors | CompetId | 109 |
| OUVV | Validaciones de usuario | User Validations | IndexID, LineNum | 110 |
| OFPR | Período de contabilización | Posting Period | AbsEntry | 111 |
| ODRF | Borradores | Drafts | DocEntry | 112 |
| OSRD | Lotes y números de serie | Batches and Serial Numbers | ItemCode, DocType, DocEntry, DocLineNum | 113 |
| OUDC | Categoría de visualización de usuario | User Display Cat. | CodeID | 114 |
| OPVL | Prestamista – Pelecard | Lender – Pelecard | Code | 115 |
| ODDT | Jerarquía de deducción de impuestos retenidos | Withholding Tax Deduction Hierarchy | Numerator | 116 |
| ODDG | Grupos de deducción de impuestos retenidos | Withholding Tax Deduction Groups | Numerator | 117 |
| OUBR | Sucursales | Branches | Code | 118 |
| OUDP | Departamentos | Departments | Code | 119 |
| OWST | Nivel de confirmación | Confirmation Level | WstCode | 120 |
| OWTM | Plantillas de aprobación | Approval Templates | WtmCode | 121 |
| OWDD | Documentos de confirmación | Docs. for Confirmation | WddCode | 122 |
| OCHD | Cheques para borradores de pago | Checks for Payment Drafts | CheckKey | 123 |
| CINF | Información de la empresa | Company Info | Version | 124 |
| OEXD | Configuración de flete | Freight Setup | ExpnsCode | 125 |
| OSTA | Autoridades fiscales de venta | Sales Tax Authorities | Code, Type | 126 |
| OSTT | Tipo de autoridades fiscales de venta | Sales Tax Authorities Type | AbsId | 127 |
| OSTC | Códigos de impuestos de venta | Sales Tax Codes | Code | 128 |
| OCRY | Países | Countries | Code | 129 |
| OCST | Estados | States | Country, Code | 130 |
| OADF | Formatos de dirección | Address Formats | Code | 131 |
| OCIN | Factura de corrección de cuentas por cobrar | A/R Correction Invoice | DocEntry | 132 |
| OCDC | Descuento por pronto pago | Cash Discount | Code | 133 |
| OQCN | Categorías de consulta | Query Catagories | CategoryId | 134 |
| OIND | Acuerdo triangular | Triangular Deal | Code | 135 |
| ODMW | Migración de datos | Data Migration | Code | 136 |
| OCSTN | ID de estación de trabajo | Workstation ID | Code | 137 |
| OIDC | Indicador | Indicator | Code | 138 |
| OGSP | Envío de mercancías | Goods Shipment | Code | 139 |
| OPDF | Borrador de pago | Payment Draft | DocEntry | 140 |
| OQWZ | Asistente de consulta | Query Wizard | Code | 141 |
| OASG | Segmentación de cuentas | Account Segmentation | AbsId | 142 |
| OASC | Categorías de segmentación de cuentas | Account Segmentation Categories | SegmentId, Code | 143 |
| OLCT | Ubicación | Location | Code | 144 |
| OTNN | Formularios 1099 | 1099 Forms | FormCode | 145 |
| OCYC | Ciclo | Cycle | Code | 146 |
| OPYM | Métodos de pago para asistente de pago | Payment Methods for Payment Wizard | PayMethCod | 147 |
| OTOB | Saldo inicial 1099 | 1099 Opening Balance | VendCode, Form1099, Box1099 | 148 |
| ORIT | Tasa de interés de reclamación | Dunning Interest Rate | Code | 149 |
| OBPP | Prioridades de socios de negocio | BP Priorities | PrioCode | 150 |
| ODUN | Cartas de reclamación | Dunning Letters | LineNum | 151 |
| CUFD | Campos de usuario – Descripción | User Fields – Description | TableID, FieldID | 152 |
| OUTB | Tablas de usuario | User Tables | TableName | 153 |
| OCUMI | Elementos de menú personalizados | My Menu Items | UserSign, Id_ | 154 |
| OPYD | Ejecución de pago | Payment Run | Code | 155 |
| OPKL | Lista de selección | Pick List | AbsEntry | 156 |
| OPWZ | Asistente de pago | Payment Wizard | IdNumber | 157 |
| OPEX | Resultados de pago | Payment Results Table | AbsEntry | 158 |
| OPYB | Bloqueo de pago | Payment Block | AbsEntry | 159 |
| OUQR | Consultas | Queries | IntrnalKey, Qcategory | 160 |
| OCBI | Indicadores bancarios centrales | Central Bank Ind. | Indicator | 161 |
| OMRV | Revalorización de inventario | Inventory Revaluation | DocEntry | 162 |
| OCPI | Factura de corrección de cuentas por pagar | A/P Correction Invoice | DocEntry | 163 |
| OCPV | Reverso de factura de corrección de cuentas por pagar | A/P Correction Invoice Reversal | DocEntry | 164 |
| OCSI | Factura de corrección de cuentas por cobrar | A/R Correction Invoice | DocEntry | 165 |
| OCSV | Reverso de factura de corrección de cuentas por cobrar | A/R Correction Invoice Reversal | DocEntry | 166 |
| OSCS | Estados de llamadas de servicio | Service Call Statuses | statusID | 167 |
| OSCT | Tipos de llamadas de servicio | Service Call Types | callTypeID | 168 |
| OSCP | Tipos de problema de llamadas de servicio | Service Call Problem Types | prblmTypID | 169 |
| OCTT | Plantilla de contrato | Contract Template | TmpltName | 170 |
| OHEM | Empleados | Employees | empID | 171 |
| OHTY | Tipos de empleado | Employee Types | typeID | 172 |
| OHST | Estados de empleado | Employee Status | statusID | 173 |
| OHTR | Motivo de terminación | Termination Reason | reasonID | 174 |
| OHED | Tipos de educación | Education Types | edType | 175 |
| OINS | Tarjeta de equipo de cliente | Customer Equipment Card | insID | 176 |
| OAGP | Nombre del agente | Agent Name | AgentCode | 177 |
| OWHT | Retención de impuestos | Withholding Tax | WTCode | 178 |
| ORFL | Informes de impuestos 347, 349 y WTax ya mostrados | Already Displayed 347, 349 and WTax Reports | DocEntry, ReportType, DocType, LineNum, TaxCode, OrdinalNum | 179 |
| OVTR | Informe de impuestos | Tax Report | AbsEntry | 180 |
| OBOE | Letra de cambio para pago | Bill of Exchange for Payment | BoeKey | 181 |
| OBOT | Transacción de letra de cambio | Bill Of Exchang Transaction | AbsEntry | 182 |
| OFRM | Formato de archivo | File Format | AbsEntry | 183 |
| OPID | Indicador de período | Period Indicator | Indicator | 184 |
| ODOR | Deudas | Doubtful Debts | AbsEntry | 185 |
| OHLD | Tabla de días festivos | Holiday Table | HldCode | 186 |
| OCRB | Cuenta bancaria de socio de negocio | BP – Bank Account | Country, BankCode, Account, CardCode | 187 |
| OSST | Estados de solución de llamadas de servicio | Service Call Solution Statuses | Number | 188 |
| OSLT | Soluciones de llamadas de servicio | Service Call Solutions | SltCode | 189 |
| OCTR | Contratos de servicio | Service Contracts | ContractID | 190 |
| OSCL | Llamadas de servicio | Service Calls | callID | 191 |
| OSCO | Orígenes de llamadas de servicio | Service Call Origins | originID | 192 |
| OUKD | Descripción de clave de usuario | User Key Description | TableName, KeyId | 193 |
| OQUE | Cola | Queue | queueID | 194 |
| OIWZ | Asistente de inflación | Inflation Wizard | AbsEntry | 195 |
| ODUT | Términos de reclamación | Dunning Terms | TermCode | 196 |
| ODWZ | Asistente de reclamación | Dunning Wizard | WizardId | 197 |
| OFCT | Pronóstico de ventas | Sales Forecast | AbsID | 198 |
| OMSN | Escenarios de MRP | MRP Scenarios | AbsEntry | 199 |
| OTER | Territorios | Territories | territryID | 200 |
| OOND | Industrias | Industries | IndCode | 201 |
| OWOR | Orden de producción | Production Order | DocEntry | 202 |
| ODPI | Pago anticipado de cuentas por cobrar | A/R Down Payment | DocEntry | 203 |
| ODPO | Pago anticipado de cuentas por pagar | A/P Down Payment | DocEntry | 204 |
| OPKG | Tipos de paquete | Package Types | PkgCode | 205 |
| OUDO | Objeto definido por el usuario | User-Defined Object | Code | 206 |
| ODOW | Propietarios de datos – Objetos | Data Ownership – Objects | Object, SubObject | 207 |
| ODOX | Excepciones de propiedad de datos | Data Ownership – Exceptions | QueryId, Object, SubObject | 208 |
| OHPS | Puesto de empleado | Employee Position | posID | 210 |
| OHTM | Equipos de empleado | Employee Teams | teamID | 211 |
| OORL | Relaciones | Relationships | OrlCode | 212 |
| ORCM | Datos de recomendación | Recommendation Data | DocEntry | 213 |
| OUPT | Árbol de autorización de usuario | User Autorization Tree | AbsId | 214 |
| OPDT | Texto predefinido | Predefined Text | AbsEntry | 215 |
| OBOX | Definición de caja | Box Definition | BoxCode, ReportType, BosCode | 216 |
| OCLA | Estado de actividad | Activity Status | statusID | 217 |
| OCSHS | Valores definidos por el usuario | User-Defined Values | IndexID | 219 |
| OACP | Categoría de periodos | Periods Category | AbsEntry | 220 |
| OATC | Adjuntos | Attachments | AbsEntry | 221 |
| OGFL | Filtro de cuadrícula | Grid Filter | FormID, GridID, UserCode | 222 |
| OLNG | Tabla de idioma de usuario | User Language Table | Code | 223 |
| OMLT | Traducción multilingüe | Multi-Language Translation | TranEntry | 224 |
| SDIS | Interfaz dinámica (cadenas) | Dynamic Interface (Strings) | FormId, ItemId, ColumnId, Language | 229 |
| OSVR | Conciliaciones guardadas | Saved Reconciliations | acctCode | 230 |
| DSC1 | Cuentas bancarias de casa | House Bank Accounts | AbsEntry | 231 |
| RDOC | Documento | Document | DocCode | 232 |
| ODGP | Conjuntos de parámetros de generación de documentos | Document Generation Parameter Sets | AbsEntry | 233 |
| OACG | Categoría de cuenta | Account Category | AbsId | 238 |
| OBCA | Códigos de asignación de cargos bancarios | Bank Charges Allocation Codes | Code | 239 |
| OCFT | Transacciones de flujo de efectivo – Filas | Cash Flow Transactions – Rows | CFTId | 241 |
| OCFW | Ítem de línea de flujo de efectivo | Cash Flow Line Item | CFWId | 242 |
| OBPL | Lugar de negocio | Business Place | BPLId | 247 |
| OJPE | Calendario de era local | Local Era Calendar | Code | 250 |
| ODIM | Dimensión de contabilidad de costos | Cost Accounting Dimension | DimCode | 251 |
| OSCD | Tabla de códigos de servicio | Service Code Table | AbsEntry | 254 |
| OSGP | Grupo de servicio para Brasil | Service Group for Brazil | AbsEntry | 255 |
| OMGP | Grupo de materiales | Material Group | AbsEntry | 256 |
| ONCM | Código NCM | NCM Code | AbsEntry | 257 |
| OCFP | CFOP para Nota Fiscal | CFOP for Nota Fiscal | ID | 258 |
| OTSC | Código CST para Nota Fiscal | CST Code for Nota Fiscal | ID | 259 |
| OUSG | Uso de Nota Fiscal | Usage of Nota Fiscal | ID | 260 |
| OCDP | Procedimiento de fecha de cierre | Closing Date Procedure | ClsDateNum | 261 |
| ONFN | Numeración de Nota Fiscal | Nota Fiscal Numbering | ObjectCode, DocSubType | 263 |
| ONFT | Categoría de impuestos de Nota Fiscal (Brasil) | Nota Fiscal Tax Category (Brazil) | AbsId | 264 |
| OCNT | Países | Counties | AbsId | 265 |
| OTCD | Determinación de código de impuesto | Tax Code Determination | AbsId | 266 |
| ODTY | Tipo de documento de letra de cambio | BoE Document Type | AbsEntry | 267 |
| OPTF | Portafolio de letra de cambio | BoE Portfolio | AbsEntry | 268 |
| OIST | Instrucción de letra de cambio | BoE Instruction | AbsEntry | 269 |
| OTPS | Parámetro de impuesto | Tax Parameter | AbsId | 271 |
| OTFC | Combinación de tipos de impuesto | Tax Type Combination | AbsId | 275 |
| OFML | Tabla maestra de fórmulas de impuestos | Tax Formula Master Table | AbsId | 276 |
| OCNA | Código CNAE | CNAE Code | AbsId | 278 |
| OTSI | Factura de impuestos de venta | Sales Tax Invoice | DocEntry | 280 |
| OTPI | Factura de impuestos de compra | Purchase Tax Invoice | DocEntry | 281 |
| OCCD | Números de declaración de aduana de carga | Cargo Customs Declaration Numbers | CCDNum | 283 |
| ORSC | Recursos | Resources | ResCode | 290 |
| ORSG | Propiedades de recursos | Resource Properties | ResTypCod | 291 |
| ORSB | ResGrpCod | ResGrpCod | ResGrpCod | 292 |
| OITR | Conciliación interna | Internal Reconciliation | ReconNum | 321 |
| OPOS | Datos maestros de Punto de Venta (POS) | POS Master Data | EquipNo | 541 |
| ODRF | Borrador de transferencia de stock | Stock Transfer Draft | DocEntry | 1179 |
| OMSG | Configuración del servicio de mensajería | Messaging Service Settings | USERID | 10000105 |
| OBTN | Datos maestros de números de lote | Batch Numbers Master Data | AbsEntry | 10000044 |
| OSRN | Datos maestros de números de serie | Serial Numbers Master Data | AbsEntry | 10000045 |
| OIVK | Claves IVL vs OINM | IVL Vs OINM Keys | TransSeq | 10000062 |
| OIQR | Contabilización de inventario | Inventory Posting | DocEntry | 10000071 |
| OFYM | Año fiscal maestro | Financial Year Master | AbsId | 10000073 |
| OSEC | Secciones | Sections | AbsId | 10000074 |
| OCSN | Series de certificados | Certificate Series | AbsId | 10000075 |
| ONOA | Naturaleza del contribuyente | Nature of Assessee | AbsId | 10000077 |
| RTYP | Lista de tipos de documento | Document Type List | CODE | 10000196 |
| OUGP | Grupo de unidades de medida | UoM Group | UgpEntry | 10000197 |
| OUOM | Datos maestros de unidades de medida | UoM Master Data | UomEntry | 10000199 |
| OBFC | Configuración de campo de ubicación | Bin Field Configuration | AbsEntry | 10000203 |
| OBAT | Atributo de ubicación de contenedor | Bin Location Attribute | AbsEntry | 10000204 |
| OBSL | Subnivel de almacén | Warehouse Sublevel | AbsEntry | 10000205 |
| OBIN | Ubicación de contenedor | Bin Location | AbsEntry | 10000206 |
| ODNF | Código DNF | DNF Code | AbsEntry | 140000041 |
| OUGR | Grupo de autorización | Authorization Group | GroupId | 231000000 |
| OEGP | Grupo de correo electrónico | E-Mail Group | EmlGrpCode | 234000004 |
| OGPC | Código de pago gubernamental | Government Payment Code | AbsId | 243000001 |
| OIQI | Saldo inicial de inventario | Inventory Opening Balance | DocEntry | 310000001 |
| OBTW | Atributos de lote en ubicación | Batch Attributes in Location | AbsEntry | 310000008 |
| OLLF | Formato de lista legal | Legal List Format | AbsEntry | 410000005 |
| OHET | Transferencia de empleado de Recursos Humanos | Object: HR Employee Transfer | TransferID | 480000001 |
| OTCX | Determinación de código de impuesto | Tax Code Determination | DocEntry | 540000005 |
| OPQT | Cotización de compra | Purchase Quotation | DocEntry | 540000006 |
| ORCP | Plantilla de transacción recurrente | Recurring Transaction Template | AbsEntry | 540000040 |
| OCCT | Tipo de centro de costo | Cost Center Type | CctCode | 540000042 |
| OACR | Tipo de acumulación | Accrual Type | Code | 540000048 |
| ONFM | Modelo de Nota Fiscal | Nota Fiscal Model | AbsEntry | 540000056 |
| OBFI | Indexador de combustible de Brasil | Brazil Fuel Indexer | ID | 540000067 |
| OBBI | Indexador de bebidas de Brasil | Brazil Beverage Indexer | ID | 540000068 |
| OCPT | Tabla principal de cockpit | Cockpit Main Table | AbsEntry | 1210000000 |
| OWTQ | Solicitud de transferencia de inventario | Inventory Transfer Request | DocEntry | 1250000001 |
| OOAT | Acuerdo marco | Blanket Agreement | AbsID | 1250000025 |
| OKPI | Paquete de indicadores clave de rendimiento | Key Performance Indicator Package | AbsEntry | 1320000000 |
| OTGG | Grupo objetivo | Target Group | TargetCode | 1320000002 |
| OCPN | Campaña | Campaign | CpnNo | 1320000012 |
| OROC | Códigos de operación de retorno | Retorno Operation Codes | AbsEntry | 1320000028 |
| OPSC | Código de origen de producto | Product Source Code | Code | 1320000039 |
| ODTP | Tipos de depreciación de activos fijos | Fixed Assets Depreciation Types | Code | 1470000000 |
| OADT | Determinación de cuentas de activos fijos | Fixed Assets Account Determination | Code | 1470000002 |
| ODPA | Áreas de depreciación de activos fijos | Fixed Asset Depreciation Areas | Code | 1470000003 |
| ODPP | Piscinas de tipos de depreciación | Depreciation Type Pools | Code | 1470000004 |
| OACS | Clases de activos | Asset Classes | Code | 1470000032 |
| OAGS | Grupos de activos | Asset Groups | Code | 1470000046 |
| ODMC | Criterios de determinación de cuenta de mayor – Inventario | G/L Account Determination Criteria – Inventory | DmcId | 1470000048 |
| OACQ | Capitalización | Capitalization | DocEntry | 1470000049 |
| OGAR | Reglas avanzadas de cuenta de mayor | G/L Account Advanced Rules | AbsEntry | 1470000057 |
| OACD | Nota de crédito | Credit Memo | DocEntry | 1470000060 |
| OBCD | Datos maestros de código de barras | Bar Code Master Data | BcdEntry | 1470000062 |
| OINC | Conteo de inventario | Inventory Counting | DocEntry | 1470000065 |
| OEDG | Grupos de descuento | Discount Groups | AbsEntry | 1470000077 |
| OCCS | Determinación de recuento cíclico | Cycle Count Determination | WhsCode | 1470000092 |
| OPRQ | Solicitud de compra | Purchase Request | DocEntry | 1470000113 |
| OWLS | Detalles de tarea de flujo de trabajo | Workflow – Task Details | TaskID | 1620000000 |

## Observaciones sobre la fuente

- **ObjType 112 y 1179** comparten la tabla ODRF (Borradores / Stock Transfer Draft).
- **ObjType 132 y 165** figuran con el mismo nombre ("A/R Correction Invoice"), en OCIN y OCSI.
- **ObjType 129 y 265:** OCRY es "Countries" y OCNT figura como "Counties" (en español "Países" en ambos).
- **ORSB (292)** tiene como descripción el propio nombre del campo (`ResGrpCod`); en la fuente no hay descripción real.
- Los ObjType 209, 218, 225–228, 234–237, etc. no figuran en la lista.
- Los nombres en español son traducciones de la fuente y pueden diferir de los de la interfaz de B1.
