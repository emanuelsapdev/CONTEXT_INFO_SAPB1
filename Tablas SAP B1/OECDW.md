# OECDW - ECD Wizard

- **Tabla:** OECDW
- **Descripción:** ECD Wizard
- **Cantidad de campos:** 40
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OECDW.html

## Campos (40)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `RunName` | Wizard Run Name | nVarChar | 100 | - |  |  |
| 3 | `RunDate` | Wizard Run Date | Date | 8 | - |  |  |
| 4 | `RunTime` | Wizard Run Time | Int | 6 | - |  |  |
| 5 | `Status` | Status | VarChar | 1 | - |  | `S` = Saved<br>`E` = Executed |
| 6 | `UserSign` | User Signature | Int | 11 | [OUSR](OUSR.md) |  |  |
| 7 | `DateFrom` | Date From | Date | 8 | - |  |  |
| 8 | `DateTo` | Date To | Date | 8 | - |  |  |
| 9 | `DecenInd` | Decentralized Indicator | VarChar | 1 | - |  | `C` = Relat�rio Consolidado<br>`H` = Matriz - Descentralizado<br>`B` = Filial - Descentralizado |
| 10 | `Branch` | Branch | Int | 11 | [OUBR](OUBR.md) | -2 |  |
| 11 | `InstCode` | Institution Code | nVarChar | 2 | - |  | `00` = Nenhuma inscri��o em outras entidades<br>`01` = Banco Central do Brasil<br>`02` = Superintend�ncia de Seguros Privados (Susep)<br>`03` = Comiss�o de Valores Mobili�rios (CVM)<br>`04` = Ag�ncia Nacional de Transportes Terrestres (ANTT)<br>`AC` = Secretaria da Fazenda do Estado do Acre, ou equivalente<br>`AL` = Secretaria da Fazenda de Alagoas, ou equivalente<br>`AM` = Secretaria da Fazenda de Amazonas, ou equivalente<br>`AP` = Secretaria da Fazenda do Amap�, ou equivalente<br>`BA` = Secretaria da Fazenda da Bahia, ou equivalente<br>`DF` = Secretaria da Fazenda do Distrito Federal, ou equivalente<br>`CE` = Secretaria da Fazenda do Cear� , ou equivalente<br>`ES` = Secretaria da Fazenda do Esp�rito Santo, ou equivalente<br>`GO` = Secretaria da Fazenda de Goi�s, ou equivalente<br>`MA` = Secretaria da Fazenda do Maranh�o, ou equivalente<br>`MT` = Secretaria da Fazenda do Mato Grosso, ou equivalente<br>`MS` = Secretaria da Fazenda do Mato Grosso do Sul, ou equivalente<br>`MG` = Secretaria da Fazenda de Minas Gerais, ou equivalente<br>`PA` = Secretaria da Fazenda do Par�, ou equivalente<br>`PB` = Secretaria da Fazenda da Para�ba, ou equivalente<br>`PE` = Secretaria da Fazenda de Pernambuco, ou equivalente<br>`PR` = Secretaria da Fazenda do Paran�, ou equivalente<br>`PI` = Secretaria da Fazenda do Piau�, ou equivalente<br>`RJ` = Secretaria da Fazenda do Rio de Janeiro, ou equivalente<br>`RN` = Secretaria da Fazenda do Rio Grande do Norte, ou equivalente<br>`RS` = Secretaria da Fazenda do Rio Grande do Sul, ou equivalente<br>`RR` = Secretaria da Fazenda de Roraima, ou equivalente<br>`RO` = Secretaria da Fazenda de Rond�nia, ou equivalente<br>`SC` = Secretaria da Fazenda de Santa Catarina, ou equivalente<br>`SP` = Secretaria da Fazenda de S�o Paulo, ou equivalente<br>`SE` = Secretaria da Fazenda de Sergipe, ou equivalente<br>`TO` = Secretaria da Fazenda de Tocantins, ou equivalente |
| 12 | `EntIdCode` | Entry Identification Code | nVarChar | 32 | - |  |  |
| 13 | `SituatInd` | Situation Indicator | VarChar | 1 | - |  | `0` = Opening (abertura)<br>`1` = Split-up/ Split-off (Cis�o parcial/ cis�o total)<br>`2` = Merger (Fus�o)<br>`3` = Downstream merger/ Upstream merger (Incorpora��o)<br>`4` = Extinction (Extin��o)<br>`5` = Transformation (Transforma��o) |
| 14 | `ReportType` | Report Type | VarChar | 1 | - |  | `G` = Livro Di�rio<br>`R` = Livro Di�rio com Escritura��o Resumida<br>`A` = Livro Di�rio Auxiliar ao Di�rio com Escritura��o Resumida<br>`B` = Livro Balancetes Di�rios e Balan�os (matriz) |
| 15 | `CmpName` | Company Name | nVarChar | 200 | - |  |  |
| 16 | `CmpState` | Company State | nVarChar | 2 | - |  |  |
| 17 | `CmpCntCode` | Company County Code | nVarChar | 10 | - |  |  |
| 18 | `CmpCNPJ` | Company CNPJ | nVarChar | 32 | - |  |  |
| 19 | `CmpIE` | Company IE | nVarChar | 32 | - |  |  |
| 20 | `CmpCity` | Company City | nVarChar | 32 | - |  |  |
| 21 | `BrnState` | Branch State | nVarChar | 2 | - |  |  |
| 22 | `BrnCntCode` | Branch County Code | nVarChar | 10 | - |  |  |
| 23 | `BrnCNPJ` | Branch CNPJ | nVarChar | 32 | - |  |  |
| 24 | `BrnIE` | Branch IE | nVarChar | 32 | - |  |  |
| 25 | `BrnCity` | Branch City | nVarChar | 32 | - |  |  |
| 26 | `AccStIden` | Account Statement Identification | VarChar | 1 | - |  | `1` = Relat�rio apenas da empresa<br>`2` = Relat�rio consolidado da matriz e filiais, afiliadas e empresas associadas |
| 27 | `AccStRem` | Account Statement Remark | Text | 16 | - |  |  |
| 28 | `BookPurp` | Book Purpose | nVarChar | 80 | - |  |  |
| 29 | `JrnlNum` | Journal Number | Int | 11 | - |  |  |
| 30 | `PeriodSitu` | Indicator of Initial Period Situation | VarChar | 1 | - |  | `0` = Normal (In�cio no primeiro dia do ano)<br>`1` = Abertura<br>`2` = Resultante de cis�o/fus�o ou remanescente de cis�o, ou realizou incorpora��o<br>`3` = In�cio de obrigatoriedade da entrega da ECD no curso do ano calend�rio |
| 31 | `BkPrpsInd` | Bookkeeping Purpose Indicator | VarChar | 1 | - |  | `0` = Original<br>`1` = Substituta com NIRE<br>`2` = Substituta sem NIRE<br>`3` = Substituta com troca de NIRE |
| 32 | `NIREind` | NIRE Indicator | VarChar | 1 | - |  | `0` = Empresa n�o possui registro na Junta Comercial (n�o possui NIRE)<br>`1` = Empresa possui registro na Junta Comercial (possui NIRE) |
| 33 | `SubBkNIRE` | Substitute Bookkeeping NIRE | nVarChar | 11 | - |  |  |
| 34 | `SubBkHash` | Substitute Bookkeeping Hash | nVarChar | 40 | - |  |  |
| 35 | `BalanTemp` | Balance Sheet Template | Int | 11 | [OFRT](OFRT.md) |  |  |
| 36 | `PrLosTemp` | Profit and Loss Statement Template | Int | 11 | [OFRT](OFRT.md) |  |  |
| 37 | `BalanRefF` | Balance Sheet Reference Fields | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 38 | `BalanUdfF` | Balance Sheet User-Defined Fields | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 39 | `PrLosRefF` | Profit and Loss Statement Reference Fields | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 40 | `PrLosUdfF` | Profit and Loss Statement User-Defined Fields | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
