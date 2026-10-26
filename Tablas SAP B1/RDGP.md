# RDGP - Development Groups

- **Tabla:** RDGP
- **Descripción:** Development Groups
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RDGP.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Num` | Group Number | Int | 11 | - |  |  |
| 2 | `GroupCode` | Development Group Code | nVarChar | 3 | - |  |  |
| 3 | `GroupName` | Development Group Name | nVarChar | 20 | - |  |  |
| 4 | `Lcaliztion` | Localization of Dev Group | nVarChar | 2 | - |  |  |
| 5 | `IdtRngStrt` | Unique Id Range - Start | Int | 11 | - |  |  |
| 6 | `IdRngEnd` | Unique Id Range - End | Int | 11 | - |  |  |
| 7 | `FrmRngStrt` | Forms Editing Range - Start | Int | 11 | - |  |  |
| 8 | `FrmRngEnd` | Forms Editing Range - End | Int | 11 | - |  |  |
| 9 | `MtxRngStrt` | Matrixes Editing Range - Start | Int | 11 | - |  |  |
| 10 | `MtxRngEnd` | Matrixes Editing Range - End | Int | 11 | - |  |  |
| 11 | `StrRngStrt` | String Lists Range - Start | Int | 11 | - |  |  |
| 12 | `StrRngEnd` | String Lists Range - End | Int | 11 | - |  |  |

## Claves e índices (10)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | GroupCode |
| NUM | Yes | Num |
| ID_START | Yes | IdtRngStrt |
| ID_END | Yes | IdRngEnd |
| FORM_START | Yes | FrmRngStrt |
| FORM_END | Yes | FrmRngEnd |
| MTX_START | Yes | MtxRngStrt |
| MTX_END | Yes | MtxRngEnd |
| STRL_START | Yes | StrRngStrt |
| STRL_END | Yes | StrRngEnd |
