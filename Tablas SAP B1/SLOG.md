# SLOG - SLOG

- **Tabla:** SLOG
- **Descripción:** SLOG
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SLOG.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `LogConfig` | Log configuration | Text | 16 | - |  |  |
| 2 | `UseDBConf` | Use DB configuration | VarChar | 1 | - |  |  |
| 3 | `ActLog` | Activate Log | VarChar | 1 | - |  |  |
| 4 | `ModDate` | DB log modification date | Date | 8 | - |  |  |
| 5 | `LogDefConf` | Log Default configuration | Text | 16 | - |  |  |
| 6 | `ReposConf` | Log Repository Configuration | Text | 16 | - |  |  |
| 7 | `AbsKey` | Primary Key | Identity | 11 | - |  |  |
| 8 | `ModTime` | DB log modification time | Int | 6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsKey |
