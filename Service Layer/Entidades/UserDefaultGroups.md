# UserDefaultGroups — Grupos de valores predeterminados de usuario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `UserDefaultGroups`
- **Descripción (ES):** Grupos de valores predeterminados de usuario
- **Entity type:** `UserDefaultGroup` (open type: accepts dynamic/UDF properties)
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [OUDG](../../Tablas%20SAP%20B1/OUDG.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 32 · **Navigation properties:** 8 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/UserDefaultGroups?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/UserDefaultGroups/$count` | Contar |
| Get by key | `GET /b1s/v2/UserDefaultGroups('value')` | Obtener por clave |
| Create | `POST /b1s/v2/UserDefaultGroups` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/UserDefaultGroups('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/UserDefaultGroups('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/UserDefaultGroups('value')` (only if the B1 object allows removal) | Borrar |

## Properties (32)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `Warehouse` | Edm.String | Yes | Warehouse | Almacén |
| 4 | `SalesEmployee` | Edm.Int32 | Yes | Sales Employee | Empleado de ventas |
| 5 | `BPforInvoicePayment` | Edm.String | Yes | B Pfor Invoice Payment | Socio de negocios para pago de factura |
| 6 | `CashAccount` | Edm.String | Yes | Cash Account | Cuenta de caja |
| 7 | `CheckingAcct` | Edm.String | Yes | Checking Account | Cuenta de verificación |
| 8 | `PrintReceipt` | [BoPrintReceiptEnum](../Enums/BoPrintReceiptEnum.md) | Yes | Print Receipt | Imprimir recibo |
| 9 | `PrintInvoiceandPaymentinS` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Print Invoiceand Paymentin S | Imprimir factura y pago en el mismo documento |
| 10 | `WindowsColor` | Edm.Int32 | Yes | Windows Color | Color de ventanas |
| 11 | `Address` | Edm.String | Yes | Address | Dirección |
| 12 | `Country` | Edm.String | Yes | Country | País |
| 13 | `PrintingHeader` | Edm.String | Yes | Printing Header | Encabezado de impresión |
| 14 | `PhoneNumber1` | Edm.String | Yes | Phone Number 1 | Número de teléfono 1 |
| 15 | `PhoneNumber2` | Edm.String | Yes | Phone Number 2 | Número de teléfono 2 |
| 16 | `FaxNumber` | Edm.String | Yes | Fax Number | Número de fax |
| 17 | `eMail` | Edm.String | Yes | E Mail | Correo electrónico |
| 18 | `AddressinForeignLanguage` | Edm.String | Yes | Addressin Foreign Language | Dirección en idioma extranjero |
| 19 | `PrintingHeaderInForeignLangu` | Edm.String | Yes | Printing Header In Foreign Langu | Encabezado de impresión en idioma extranjero |
| 20 | `PhoneNumber1ForeignLang` | Edm.String | Yes | Phone Number 1 Foreign Lang | Número de teléfono 1 (idioma extranjero) |
| 21 | `PhoneNumber2ForeignLang` | Edm.String | Yes | Phone Number 2 Foreign Lang | Número de teléfono 2 (idioma extranjero) |
| 22 | `FaxNumberForeignLang` | Edm.String | Yes | Fax Number Foreign Lang | Número de fax (idioma extranjero) |
| 23 | `DefaultTaxCode` | Edm.String | Yes | Default Tax Code | Indicador de impuesto predeterminado |
| 24 | `AdditionalIdNumber` | Edm.String | Yes | Additional ID Number | Número de identificación adicional |
| 25 | `UserSignature` | Edm.Int32 | Yes | User Signature | Firma del usuario |
| 26 | `UseTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Use Tax | Impuesto de uso |
| 27 | `UseWarehouseAddressinAPD` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Use Warehouse Addressin APD | Usar dirección del almacén en documentos de compras |
| 28 | `BPLID` | Edm.Int32 | Yes | BPLID | ID de sucursal |
| 29 | `AssetInDoc` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Asset In Document | Activo en documento |
| 30 | `LanguageCode` | [BoSuppLangs](../Enums/BoSuppLangs.md) | Yes | Language Code | Código de idioma |
| 31 | `DefaultDocuments` | Collection([DefaultDocument](../Tipos-Complejos/DefaultDocument.md)) | Yes | Default Documents | Documentos predeterminados |
| 32 | `DefaultCreditCards` | Collection([DefaultCreditCard](../Tipos-Complejos/DefaultCreditCard.md)) | Yes | Default Credit Cards | Tarjetas de crédito predeterminadas |

## Navigation properties (8)

Use `GET /b1s/v2/UserDefaultGroups('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Warehouse2` | [Warehouse](../Entidades/Warehouses.md) | [Warehouses](Warehouses.md) | Warehouse → WarehouseCode | Almacenes |
| `SalesPerson` | [SalesPerson](../Entidades/SalesPersons.md) | [SalesPersons](SalesPersons.md) | SalesEmployee → SalesEmployeeCode | Empleado de ventas |
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | BPforInvoicePayment → CardCode | Socio de negocios |
| `Country2` | [Country](../Entidades/Countries.md) | [Countries](Countries.md) | Country → Code | Países/Regiones |
| `SalesTaxCode` | [SalesTaxCode](../Entidades/SalesTaxCodes.md) | [SalesTaxCodes](SalesTaxCodes.md) | DefaultTaxCode → Code | Códigos del impuesto sobre ventas |
| `User` | [User](../Entidades/Users.md) | [Users](Users.md) | UserSignature → InternalKey | Usuario |
| `BusinessPlace` | [BusinessPlace](../Entidades/BusinessPlaces.md) | [BusinessPlaces](BusinessPlaces.md) | BPLID → BPLID | Lugar de negocios |
| `UserLanguage` | [UserLanguage](../Entidades/UserLanguages.md) | [UserLanguages](UserLanguages.md) | LanguageCode → Code | Idiomas de usuario |
