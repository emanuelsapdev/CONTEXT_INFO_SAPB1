# SCFG - SCFG

- **Tabla:** SCFG
- **Descripción:** SCFG
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SCFG.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PFlags` | Protect settings flags | Text | 16 | - |  |  |
| 2 | `B1iEnabled` | Is B1i enabled? | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 3 | `LstBckupTo` | Last backup Timeout | Int | 11 | - | 60 |  |
| 4 | `SkinStyle` | Skin Style | VarChar | 1 | - | H |  |
| 5 | `IsPALInit` | Is PAL Initialize or Not | VarChar | 1 | - | N |  |
| 6 | `PANAVer` | Pervasive Version | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | B1iEnabled |
