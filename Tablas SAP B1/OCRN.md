# OCRN - Currency Codes

- **Tabla:** OCRN
- **Descripción:** Currency Codes
- **Cantidad de campos:** 28
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCRN.html

## Campos (28)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CurrCode` | Currency Code | nVarChar | 3 | - |  |  |
| 2 | `CurrName` | Currency | nVarChar | 20 | - |  |  |
| 3 | `ChkName` | Name on Printed Checks | nVarChar | 20 | - |  |  |
| 4 | `Chk100Name` | Name of 100's on checks | nVarChar | 20 | - |  |  |
| 5 | `DocCurrCod` | Name on Printed Docs. | nVarChar | 3 | - |  |  |
| 6 | `FrgnName` | English | nVarChar | 20 | - |  |  |
| 7 | `F100Name` | English Hundredth Name | nVarChar | 20 | - |  |  |
| 8 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 10 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 11 | `RoundSys` | Rounding | Int | 6 | - | 0 | `0` = No Rounding<br>`4` = Round to Five Hundredth<br>`1` = Round to Ten Hundredth<br>`2` = Round to One<br>`3` = Round to Ten |
| 12 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 13 | `Decimals` | Decimals | Int | 6 | - | -1 | `-1` = Default<br>`0` = Without Decimals<br>`1` = 1 Digit<br>`2` = 2 Digits<br>`3` = 3 Digits<br>`4` = 4 Digits<br>`5` = 5 Digits<br>`6` = 6 Digits |
| 14 | `ISRCalc` | ISR Calculation | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 15 | `RoundPym` | Rounding in Pmnt | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 16 | `ConvUnit` | Is a Conventional Unit | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 17 | `BaseCurr` | Base Currency for Conv. Unit | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 18 | `Factor` | Factor | Num | 19.6 | - |  |  |
| 19 | `ChkNamePl` | Plural for Int.Description | nVarChar | 20 | - |  |  |
| 20 | `Chk100NPl` | Plural for Hundredth Name | nVarChar | 20 | - |  |  |
| 21 | `FrgnNamePl` | Plural for English | nVarChar | 20 | - |  |  |
| 22 | `F100NamePl` | Plural for Eng. Hundredth Name | nVarChar | 20 | - |  |  |
| 23 | `ISOCurrCod` | ISO Currency Code | nVarChar | 3 | - |  | `AED` = United Arab Emirates, Dirhams<br>`AFN` = Afghanistan, Afghanis<br>`ALL` = Albania, Leke<br>`AMD` = Armenia, Drams<br>`ANG` = Netherlands Antilles, Guilders (also called Florins)<br>`AOA` = Angola, Kwanzas<br>`ARS` = Argentina, Pesos<br>`AUD` = Australia, Dollars<br>`AWG` = Aruba, Guilders (also called Florins)<br>`AZM` = Azerbaijan, Manats [obsolete]<br>`AZN` = Azerbaijan, New Manats<br>`BAM` = Bosnia and Herzegovina, Convertible Marks<br>`BBD` = Barbados, Dollars<br>`BDT` = Bangladesh, Taka<br>`BGN` = Bulgaria, Leva<br>`BHD` = Bahrain, Dinars<br>`BIF` = Burundi, Francs<br>`BMD` = Bermuda, Dollars<br>`BND` = Brunei, Ringgits<br>`BOB` = Bolivia, Bolivianos<br>`BRL` = Brazil, Brazilian Reals<br>`BSD` = Bahamas, Dollars<br>`BTN` = Bhutan, Ngultrum<br>`BWP` = Botswana, Pulas<br>`BYN` = Belarus, Rubles<br>`BYR` = Belarus, Rubles<br>`BZD` = Belize, Dollars<br>`CAD` = Canada, Dollars<br>`CDF` = Congo/Kinshasa, Congolese Francs<br>`CHF` = Switzerland, Francs<br>`CLP` = Chile, Pesos<br>`CNY` = China, Yuan Renminbi<br>`COP` = Colombia, Pesos<br>`CRC` = Costa Rica, Colones<br>`CUP` = Cuba, Pesos<br>`CVE` = Cape Verde, Escudos<br>`CYP` = Cyprus, Pounds<br>`CZK` = Czech Republic, Koruny<br>`DJF` = Djibouti, Francs<br>`DKK` = Denmark, Kroner<br>`DOP` = Dominican Republic, Pesos<br>`DZD` = Algeria, Algerian Dinars<br>`EEK` = Estonia, Krooni<br>`EGP` = Egypt, Pounds<br>`ERN` = Eritrea, Nakfa<br>`ETB` = Ethiopia, Birr<br>`EUR` = EU Member Countries, Euro<br>`FJD` = Fiji, Dollars<br>`FKP` = Falkland Islands (Malvinas), Pounds<br>`GBP` = United Kingdom, Pounds<br>`GEL` = Georgia, Lari<br>`GGP` = Guernsey, Pounds<br>`GHC` = Ghana, Cedis<br>`GHS` = Ghana, Cedis<br>`GIP` = Gibraltar, Pounds<br>`GMD` = Gambia, Dalasi<br>`GNF` = Guinea, Francs<br>`GTQ` = Guatemala, Quetzales<br>`GYD` = Guyana, Dollars<br>`HKD` = Hong Kong, Dollars<br>`HNL` = Honduras, Lempiras<br>`HRK` = Croatia, Kuna<br>`HTG` = Haiti, Gourdes<br>`HUF` = Hungary, Forint<br>`IDR` = Indonesia, Rupiahs<br>`ILS` = Israel, New Shekels<br>`IMP` = Isle of Man, Pounds<br>`INR` = India, Rupees<br>`IQD` = Iraq, Dinars<br>`IRR` = Iran, Rials<br>`ISK` = Iceland, Kronur<br>`JEP` = Jersey, Pounds<br>`JMD` = Jamaica, Dollars<br>`JOD` = Jordan, Dinars<br>`JPY` = Japan, Yen<br>`KES` = Kenya, Shillings<br>`KGS` = Kyrgyzstan, Soms<br>`KHR` = Cambodia, Riels<br>`KMF` = Comoros, Francs<br>`KPW` = Korea (North), Won<br>`KRW` = Korea (South), Won<br>`KWD` = Kuwait, Dinars<br>`KYD` = Cayman Islands, Dollars<br>`KZT` = Kazakhstan, Tenge<br>`LAK` = Laos, Kips<br>`LBP` = Lebanon, Pounds<br>`LKR` = Sri Lanka, Rupees<br>`LRD` = Liberia, Dollars<br>`LSL` = Lesotho, Maloti<br>`LTL` = Lithuania, Litai<br>`LVL` = Latvia, Lati<br>`LYD` = Libya, Dinars<br>`MAD` = Morocco, Dirhams<br>`MDL` = Moldova, Lei<br>`MGA` = Madagascar, Ariary<br>`MKD` = Macedonia, Denars<br>`MMK` = Myanmar (Burma), Kyats<br>`MNT` = Mongolia, Tugriks<br>`MOP` = Macau, Patacas<br>`MRO` = Mauritania, Ouguiyas<br>`MTL` = Malta, Liri<br>`MUR` = Mauritius, Rupees<br>`MVR` = Maldives (Maldive Islands), Rufiyaa<br>`MWK` = Malawi, Kwachas<br>`MXN` = Mexico, Pesos<br>`MYR` = Malaysia, Ringgits<br>`MZM` = Mozambique, Meticais [obsolete]<br>`MZN` = Mozambique, Meticais [newer unit, same name]<br>`NAD` = Namibia, Dollars<br>`NGN` = Nigeria, Nairas<br>`NIO` = Nicaragua, Cordobas<br>`NOK` = Norway, Krone<br>`NPR` = Nepal, Nepal Rupees<br>`NZD` = New Zealand, Dollars<br>`OMR` = Oman, Rials<br>`PAB` = Panama, Balboa<br>`PEN` = Peru, Nuevos Soles<br>`PGK` = Papua New Guinea, Kina<br>`PHP` = Philippines, Pesos<br>`PKR` = Pakistan, Rupees<br>`PLN` = Poland, Zlotych<br>`PYG` = Paraguay, Guarani<br>`QAR` = Qatar, Rials<br>`ROL` = Romania, Lei [obsolete]<br>`RON` = Romania, New Lei<br>`RSD` = Serbia, Dinars<br>`RUB` = Russia, Rubles<br>`RWF` = Rwanda, Rwandan Francs<br>`SAR` = Saudi Arabia, Riyals<br>`SBD` = Solomon Islands, Dollars<br>`SCR` = Seychelles, Rupees<br>`SDD` = Sudan, Dinars [obsolete]<br>`SDG` = Sudan, Pounds<br>`SEK` = Sweden, Kronor<br>`SGD` = Singapore, Dollars<br>`SHP` = Saint Helena, Pounds<br>`SIT` = Slovenia, Tolars [obsolete]<br>`SKK` = Slovakia, Koruny<br>`SLL` = Sierra Leone, Leones<br>`SOS` = Somalia, Shillings<br>`SPL` = Seborga, Luigini<br>`SRD` = Suriname, Dollars<br>`STD` = Sao Tome and Principe, Dobras<br>`SVC` = El Salvador, Colones<br>`SYP` = Syria, Pounds<br>`SZL` = Swaziland, Emalangeni<br>`THB` = Thailand, Baht<br>`TJS` = Tajikistan, Somoni<br>`TMT` = Turkmenistan, Manats<br>`TND` = Tunisia, Dinars<br>`TOP` = Tonga, Pa'anga<br>`TRY` = Turkey, New Lira<br>`TTD` = Trinidad and Tobago, Dollars<br>`TVD` = Tuvalu, Tuvalu Dollars<br>`TWD` = Taiwan, New Dollars<br>`TZS` = Tanzania, Shillings<br>`UAH` = Ukraine, Hryvnia<br>`UGX` = Uganda, Shillings<br>`USD` = United States of America, Dollars<br>`UYU` = Uruguay, Pesos<br>`UZS` = Uzbekistan, Sums<br>`VEB` = Venezuela, Bolivares<br>`VND` = Viet Nam, Dong<br>`VUV` = Vanuatu, Vatu<br>`WST` = Samoa, Tala<br>`XAF` = Communaute Financiere Africaine BEAC, Francs<br>`XAG` = Silver, Ounces<br>`XAU` = Gold, Ounces<br>`XCD` = East Caribbean Dollars<br>`XCG` = Caribbean Guilder<br>`XDR` = International Monetary Fund (IMF) Special Drawing Rights<br>`XOF` = Communaute Financiere Africaine BCEAO, Francs<br>`XPD` = Palladium Ounces<br>`XPF` = Comptoirs Francais du Pacifique Francs<br>`XPT` = Platinum, Ounces<br>`YER` = Yemen, Rials<br>`ZAR` = South Africa, Rand<br>`ZMW` = Zambia, Kwacha<br>`ZMK` = Zambia, Kwacha<br>`ZWD` = Zimbabwe, Zimbabwe Dollars |
| 24 | `MaxInDiff` | Incoming Amt Diff. Allowed | Num | 19.6 | - |  |  |
| 25 | `MaxOutDiff` | Outgoing Amt Diff. Allowed | Num | 19.6 | - |  |  |
| 26 | `MaxInPcnt` | Incoming % Diff. Allowed | Num | 19.6 | - |  |  |
| 27 | `MaxOutPcnt` | Outgoing % Diff. Allowed | Num | 19.6 | - |  |  |
| 28 | `ISOCurrNum` | ISO Currency Number | nVarChar | 3 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CurrCode |
| CUR_NAME | No | CurrName |
