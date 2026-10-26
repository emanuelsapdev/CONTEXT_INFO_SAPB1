# DefaultDocument — Documentos predeterminados

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DefaultDocument`
- **Descripción (ES):** Documentos predeterminados
- **Description (EN):** Default Document
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 12

## Properties (12)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AddExport` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Add Export | Exportación adicional |
| 2 | `AddPrint` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Add Print | Impresión adicional |
| 3 | `Code` | Edm.String | Yes | Code | Código |
| 4 | `EnglishKeyboardEnteringBPC` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | English Keyboard Entering BPC | Teclado inglés al ingresar código de socio de negocios |
| 5 | `NoofCopies` | Edm.Int32 | Yes | Noof Copies | Cantidad de copias |
| 6 | `NoofCopiesforManualDoc` | Edm.Int32 | Yes | Noof Copiesfor Manual Document | Cantidad de copias para documento manual |
| 7 | `ObjectType` | Edm.String | Yes | Object Type | Tipo de objeto |
| 8 | `PermanentRemark` | Edm.String | Yes | Permanent Remark | Comentario permanente |
| 9 | `PrintDiscountData` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Print Discount Data | Imprimir datos de descuento |
| 10 | `PrintToals` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Print Toals | Imprimir totales |
| 11 | `PrintVendorCatalogNo` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Print Vendor Catalog Number | Imprimir N.º de catálogo del proveedor |
| 12 | `TotalsRounding` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Totals Rounding | Redondeo de totales |

## Used by (properties)

- [UserDefaultGroup](../Entidades/UserDefaultGroups.md).`DefaultDocuments`
