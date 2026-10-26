# OVTP - Vendor Type

- **Tabla:** OVTP
- **Descripción:** Vendor Type
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OVTP.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ABSEntry` | Primary Key | Int | 11 | - |  |  |
| 2 | `VendorType` | Vendor Type | nVarChar | 32 | - |  |  |
| 3 | `Descript` | Description | nVarChar | 120 | - |  |  |
| 4 | `Locked` | Locked | VarChar | 1 | - | N |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ABSEntry |
| TYPE | No | VendorType |
