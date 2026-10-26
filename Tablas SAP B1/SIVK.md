# SIVK - IVL Vs OINM Keys

- **Tabla:** SIVK
- **Descripción:** IVL Vs OINM Keys
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SIVK.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TransSeq` | Transaction Sequence No. | Int | 11 | - |  |  |
| 2 | `LayerID` | Layer ID | Int | 11 | - |  |  |
| 3 | `RootID` | Root ID | Int | 11 | - |  |  |
| 4 | `TransNum` | Transaction Number | Int | 11 | - |  |  |
| 5 | `Instance` | Instance | Int | 11 | - | 0 |  |
| 6 | `INMTransSe` | INM_Transaction Sequence No. | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | INMTransSe |
| TRANSSEQ | Yes | TransSeq, LayerID |
