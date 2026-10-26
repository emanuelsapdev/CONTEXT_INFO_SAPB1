# MLS1 - Distribution Lists - Recipients

- **Tabla:** MLS1
- **Descripción:** Distribution Lists - Recipients
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MLS1.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | Int | 11 | [OMLS](OMLS.md) |  |  |
| 2 | `LineNum` | Addressee Number | Int | 11 | - |  |  |
| 3 | `ObjType` | Object | nVarChar | 20 | - |  |  |
| 4 | `ObjCode` | Object Code | nVarChar | 50 | - |  |  |
| 5 | `ObjName` | Name | nVarChar | 155 | - |  |  |
| 6 | `E_Mail` | E-Mail | nVarChar | 100 | - |  |  |
| 7 | `PortNum` | Mobile Phone Number | nVarChar | 50 | - |  |  |
| 8 | `Fax` | Fax Number | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, LineNum |
