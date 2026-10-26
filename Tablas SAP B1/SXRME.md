# SXRME - XLR Members

- **Tabla:** SXRME
- **Descripción:** XLR Members
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SXRME.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `MemberId` | MemberId | Identity | 11 | - |  |  |
| 2 | `RoleId` | RoleId | nVarChar | 16 | - |  |  |
| 3 | `DomainType` | DomainType | Int | 11 | - | 0 |  |
| 4 | `MemberType` | MemberType | Int | 11 | - | 0 |  |
| 5 | `Name` | Name | nVarChar | 244 | - |  |  |
| 6 | `Domain` | Domain | nVarChar | 244 | - |  |  |
| 7 | `Descriptio` | Description | nVarChar | 254 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | MemberId |
| second | Yes | RoleId, DomainType, Name, Domain |
