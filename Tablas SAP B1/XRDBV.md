# XRDBV - XLR company DB version

- **Tabla:** XRDBV
- **Descripción:** XLR company DB version
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/XRDBV.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DBObjVer` | IXDBObjectsVersion | nVarChar | 20 | - |  |  |
| 2 | `DBObjVerDe` | IXDBObjectsVersionDescr | nVarChar | 254 | - |  |  |
| 3 | `DBObjVerUp` | IXDBObjectsVersionUpdated | Date | 8 | - |  |  |
| 4 | `ParVer` | PartnerVersion | nVarChar | 20 | - |  |  |
| 5 | `ParVerDesc` | PartnerVersionDescr | nVarChar | 254 | - |  |  |
| 6 | `ParVerUpd` | PartnerVersionUpdated | Date | 8 | - |  |  |
| 7 | `Partner` | Partner | nVarChar | 50 | - |  |  |
| 8 | `PartnerDBV` | PartnerDBVersion | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DBObjVer |
