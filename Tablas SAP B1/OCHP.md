# OCHP - India Chapter ID

- **Tabla:** OCHP
- **Descripción:** India Chapter ID
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCHP.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | - |  |  |
| 2 | `Chapter` | Chapter | nVarChar | 20 | - |  |  |
| 3 | `Heading` | Tariff Heading | nVarChar | 20 | - |  |  |
| 4 | `SubHeading` | Tariff Subheading | nVarChar | 20 | - |  |  |
| 5 | `Dscription` | Description for Tariff Heading | nVarChar | 120 | - |  |  |
| 6 | `ChapterID` | Chapter ID | nVarChar | 64 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| CHAPTERID | Yes | ChapterID |
| CHAPTER | No | Chapter, Heading, SubHeading |
