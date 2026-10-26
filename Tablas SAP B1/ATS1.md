# ATS1 - Transporter - Transportations

- **Tabla:** ATS1
- **Descripción:** Transporter - Transportations
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ATS1.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Transporter Abs. Entry | Int | 11 | - |  |  |
| 2 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 3 | `TransMode` | Mode | Int | 11 | [OETM](OETM.md) |  |  |
| 4 | `VehicleTyp` | Vehicle Type | nVarChar | 2 | [OEVT](OEVT.md) |  |  |
| 5 | `VehicleNo` | Vehicle Number | nVarChar | 15 | - |  |  |
| 6 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum, LogInstanc |
