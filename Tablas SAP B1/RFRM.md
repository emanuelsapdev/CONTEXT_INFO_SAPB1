# RFRM - FORM resource

- **Tabla:** RFRM
- **Descripción:** FORM resource
- **Cantidad de campos:** 40
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RFRM.html

## Campos (40)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Created` | Creation date | Date | 8 | - |  |  |
| 2 | `Updated` | Update date | Date | 8 | - |  |  |
| 3 | `Language` | Language code | Int | 11 | - |  |  |
| 4 | `Name` | Form name | nVarChar | 64 | - |  |  |
| 5 | `Num` | Form number | Int | 11 | - |  |  |
| 6 | `Title` | Title | nVarChar | 64 | - |  |  |
| 7 | `TitleUpd` | Title update | Date | 8 | - |  |  |
| 8 | `TitleLen` | Title length | Int | 11 | - |  |  |
| 9 | `Type` | Form type | Int | 11 | - | 0 | `0` = Resize Document<br>`1` = Dialog Box<br>`3` = No Title Document<br>`4` = Fixed Document<br>`5` = Resize No Title Document<br>`6` = Toolbar |
| 10 | `CloseBox` | Close box | VarChar | 1 | - | 1 | `0` = Yes<br>`1` = No |
| 11 | `DfltButton` | Default button | Int | 11 | - | 0 |  |
| 12 | `_Top` | Top | Int | 11 | - | 1 |  |
| 13 | `_Bottom` | Bottom | Int | 11 | - |  |  |
| 14 | `_Left` | Left | Int | 11 | - |  |  |
| 15 | `_Right` | Right | Int | 11 | - |  |  |
| 16 | `DoColor` | Use color table | VarChar | 1 | - | 1 | `0` = Yes<br>`1` = No |
| 17 | `CT_SEED` | CT_SEED | Int | 11 | - |  |  |
| 18 | `CT_RESERVE` | CT_RESERVE | Int | 11 | - |  |  |
| 19 | `CT_SIZE` | CT_SIZE | Int | 11 | - |  |  |
| 20 | `CT_S0_VAL` | CT_S0_VALUE | Int | 11 | - |  |  |
| 21 | `CT_S0_RED` | CT_S0_RED | Int | 11 | - |  |  |
| 22 | `CT_S0_GRN` | CT_S0_GREEN | Int | 11 | - |  |  |
| 23 | `CT_S0_BLUE` | CT_S0_BLUE | Int | 11 | - |  |  |
| 24 | `CT_S1_VAL` | CT_S1_VALUE | Int | 11 | - |  |  |
| 25 | `CT_S1_RED` | CT_S1_RED | Int | 11 | - |  |  |
| 26 | `CT_S1_GRN` | CT_S1_GREEN | Int | 11 | - |  |  |
| 27 | `CT_S1_BLUE` | CT_S1_BLUE | Int | 11 | - |  |  |
| 28 | `CT_S2_VAL` | CT_S2_VALUE | Int | 11 | - |  |  |
| 29 | `CT_S2_RED` | CT_S2_RED | Int | 11 | - |  |  |
| 30 | `CT_S2_GRN` | CT_S2_GREEN | Int | 11 | - |  |  |
| 31 | `CT_S2_BLUE` | CT_S2_BLUE | Int | 11 | - |  |  |
| 32 | `CT_S3_VAL` | CT_S3_VALUE | Int | 11 | - |  |  |
| 33 | `CT_S3_RED` | CT_S3_RED | Int | 11 | - |  |  |
| 34 | `CT_S3_GRN` | CT_S3_GREEN | Int | 11 | - |  |  |
| 35 | `CT_S3_BLUE` | CT_S3_BLUE | Int | 11 | - |  |  |
| 36 | `CT_S4_VAL` | CT_S4_VALUE | Int | 11 | - |  |  |
| 37 | `CT_S4_RED` | CT_S4_RED | Int | 11 | - |  |  |
| 38 | `CT_S4_GRN` | CT_S4_GREEN | Int | 11 | - |  |  |
| 39 | `CT_S4_BLUE` | CT_S4_BLUE | Int | 11 | - |  |  |
| 40 | `MaxUnique` | Max Unique | Int | 11 | - |  |  |

## Claves e índices (4)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Language, Name |
| NUM | Yes | Language, Num |
| M_NAME | No | Name |
| M_NUM | No | Num |
