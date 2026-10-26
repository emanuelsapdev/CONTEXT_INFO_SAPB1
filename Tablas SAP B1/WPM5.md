# WPM5 - Process Map Assigned User

- **Tabla:** WPM5
- **Descripción:** Process Map Assigned User
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WPM5.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PrcMapId` | Process Map ID | nVarChar | 40 | [OWPM](OWPM.md) |  |  |
| 2 | `Guid` | Guid of Assigend User | nVarChar | 40 | - |  |  |
| 3 | `UserId` | User ID | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | PrcMapId, Guid |
