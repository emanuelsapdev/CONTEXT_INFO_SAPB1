# OBDC - B1i DI Configuration

- **Tabla:** OBDC
- **Descripción:** B1i DI Configuration
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBDC.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | Int | 11 | - |  |  |
| 2 | `Server` | Server | nVarChar | 254 | - |  |  |
| 3 | `License` | License Server | nVarChar | 254 | - |  |  |
| 4 | `Company` | Company | nVarChar | 128 | - |  |  |
| 5 | `DBType` | DB Type | Int | 11 | - |  |  |
| 6 | `DBUser` | DB User | nVarChar | 254 | - |  |  |
| 7 | `DBPassword` | DB Password | nVarChar | 254 | - |  |  |
| 8 | `Username` | User Name | nVarChar | 254 | - |  |  |
| 9 | `UPassword` | User Password | nVarChar | 254 | - |  |  |
| 10 | `DBTrusted` | DB Trusted | VarChar | 1 | - |  |  |
| 11 | `JCOPath` | Java Connector Path | nVarChar | 254 | - |  |  |
| 12 | `Language` | Language | Int | 11 | - |  |  |
| 13 | `AddOnIF` | Add-On Identifier | nVarChar | 254 | - |  |  |
| 14 | `StateFder` | Bank Statement Folder | nVarChar | 254 | - |  |  |
| 15 | `FormatFder` | Bank Format Folder | nVarChar | 254 | - |  |  |
| 16 | `FileFolder` | Bank File Folder | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
