# AUSR - Users - History

- **Tabla:** AUSR
- **Descripción:** Users - History
- **Cantidad de campos:** 140
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AUSR.html

## Campos (140)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `USERID` | User Signature | Int | 6 | - |  |  |
| 2 | `PASSWORD` | User Password | nVarChar | 254 | - | 0 |  |
| 3 | `PASSWORD1` | User Password | nVarChar | 8 | - |  |  |
| 4 | `PASSWORD2` | User Password | nVarChar | 8 | - |  |  |
| 5 | `INTERNAL_K` | Internal Number | Int | 6 | - |  |  |
| 6 | `USER_CODE` | User Code | nVarChar | 25 | - |  |  |
| 7 | `U_NAME` | User Name | nVarChar | 155 | - |  |  |
| 8 | `GROUPS` | Authorization Group | Int | 6 | - | 0 |  |
| 9 | `PASSWORD4` | Password | nVarChar | 254 | - |  |  |
| 10 | `ALLOWENCES` | User Confirmation | Text | 16 | - |  |  |
| 11 | `SUPERUSER` | Superuser | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `DISCOUNT` | Max. Discount | Num | 19.6 | - |  |  |
| 13 | `PASSWORD3` | User Password | nVarChar | 8 | - |  |  |
| 14 | `Info1File` | Info1File | nVarChar | 4 | - |  |  |
| 15 | `Info1Field` | Info1Field | Int | 6 | - |  |  |
| 16 | `Info2File` | Info2File | nVarChar | 4 | - |  |  |
| 17 | `Info2Field` | Info2Field | Int | 6 | - |  |  |
| 18 | `Info3File` | Info3File | nVarChar | 4 | - |  |  |
| 19 | `Info3Field` | Info3Field | Int | 6 | - |  |  |
| 20 | `Info4File` | Info4File | nVarChar | 4 | - |  |  |
| 21 | `Info4Field` | Info4Field | Int | 6 | - |  |  |
| 22 | `dType` | dType | VarChar | 1 | - | S | `Y` = Yes<br>`N` = No<br>`X`<br>`H` = SHA1<br>`S` = SHA256 |
| 23 | `E_Mail` | E-Mail | nVarChar | 100 | - |  |  |
| 24 | `PortNum` | Mobile Phone Number | nVarChar | 50 | - |  |  |
| 25 | `OutOfOffic` | Out of the Office | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 26 | `SendEMail` | Send E-Mail | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 27 | `SendSMS` | Send SMS | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 28 | `DfltsGroup` | Default | nVarChar | 8 | [OUDG](OUDG.md) |  |  |
| 29 | `CashLimit` | Cash Amount Limit | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 30 | `MaxCashSum` | Max. Cash Total | Num | 19.6 | - |  |  |
| 31 | `Fax` | Fax Number | nVarChar | 50 | - |  |  |
| 32 | `SendFax` | Send Fax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 33 | `Locked` | User Confirmation | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 34 | `Department` | Department | Int | 6 | [OUDP](OUDP.md) | -2 |  |
| 35 | `Branch` | Branch | Int | 6 | [OUBR](OUBR.md) | -2 |  |
| 36 | `UserPrefs` | User Preferences | Text | 16 | - |  |  |
| 37 | `Language` | Language | Int | 11 | - |  |  |
| 38 | `Charset` | Font Language | Int | 6 | - |  |  |
| 39 | `OpenCdt` | Open Window for Credit Vouchers Ref. Update | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 40 | `CdtPrvDays` | Vouchers from Last Days | Int | 11 | - | 1 |  |
| 41 | `DsplyRates` | Display Rates Table on Startup | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 42 | `AuImpRates` | Import Currency Exchange Rates Automatically | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 43 | `OpenDps` | Open Postdated Checks Window | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 44 | `RcrFlag` | Display Scheduled Recurring Postings | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 45 | `CheckFiles` | Perform Data Check | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 46 | `OpenCredit` | Open Window for Postdated Credit Vouchers | VarChar | 1 | - | N | `Y` = Always<br>`N` = No<br>`D` = By Date |
| 47 | `CreditDay1` | Handle Postdated Credit Day 1 | Int | 6 | - | 1 |  |
| 48 | `CreditDay2` | Handle Postdated Credit Day 2 | Int | 6 | - | 15 |  |
| 49 | `WallPaper` | Wallpaper | Text | 16 | - |  |  |
| 50 | `WllPprDsp` | Wallpaper Display | Int | 6 | - | 1 | `1` = Centralized<br>`2` = Full Screen<br>`3` = Tile |
| 51 | `AdvImagePr` | Extended Image Processing | VarChar | 1 | - | N | `N` = Yes<br>`O` = No<br>`Y` = Full |
| 52 | `ContactLog` | Today's Activity Alert | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 53 | `LastWarned` | Last Warned Date | Date | 8 | - |  |  |
| 54 | `AlertPolFr` | Message Check Frequency (Min.) | Int | 6 | - | 5 |  |
| 55 | `ScreenLock` | Screen Lock Delay | Int | 6 | - | 30 |  |
| 56 | `ShowNewMsg` | Display Message/Alert on Arrival | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 57 | `Picture` | Picture | nVarChar | 200 | - |  |  |
| 58 | `Position` | Position | nVarChar | 90 | - |  |  |
| 59 | `Address` | Address | nVarChar | 254 | - |  |  |
| 60 | `Country` | Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 61 | `Tel1` | Telephone 1 | nVarChar | 50 | - |  |  |
| 62 | `Tel2` | Telephone 2 | nVarChar | 50 | - |  |  |
| 63 | `GENDER` | Gender | VarChar | 1 | - | F | `F` = Female<br>`M` = Male |
| 64 | `Birthday` | Date of Birth | Date | 8 | - |  |  |
| 65 | `EnbMenuFlt` | Enable Forbidden Menu Items | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 66 | `objType` | Object Type | nVarChar | 20 | - | 12 |  |
| 67 | `logInstanc` | Log Instance | Int | 11 | - |  |  |
| 68 | `userSign` | Creating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 69 | `createDate` | Creation Date | Date | 8 | - |  |  |
| 70 | `userSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 71 | `updateDate` | Update Date | Date | 8 | - |  |  |
| 72 | `OneLogPwd` | At first logon change password | VarChar | 1 | - | N | `N` = Do not change password at first login<br>`Y` = At first logon change password |
| 73 | `lastLogin` | Last Logon Date | Date | 8 | - |  |  |
| 74 | `LastPwds` | Last Passwords 1 | Text | 16 | - |  |  |
| 75 | `LastPwds2` | Last Passwords 2 | nVarChar | 254 | - | 0 |  |
| 76 | `LastPwdSet` | Last Password Change | Date | 8 | - |  |  |
| 77 | `FailedLog` | Failed Login Count | Int | 11 | - | 0 |  |
| 78 | `PwdNeverEx` | Password Never Expires | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 79 | `SalesDisc` | Max. Sales Discount | Num | 19.6 | - |  |  |
| 80 | `PurchDisc` | Max. Purchase Discount | Num | 19.6 | - |  |  |
| 81 | `LstLogoutD` | Last Logoff Date | Date | 8 | - |  |  |
| 82 | `LstLoginT` | Last Logon Time | Int | 11 | - |  |  |
| 83 | `LstLogoutT` | Last Logoff Time | Int | 11 | - |  |  |
| 84 | `LstPwdChT` | Last Password Change Time | Int | 11 | - |  |  |
| 85 | `LstPwdChB` | Last Password Changed By | nVarChar | 25 | - |  |  |
| 86 | `RclFlag` | Display Recurring Transactions | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 87 | `MobileUser` | Mobile User | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 88 | `MobileIMEI` | Mobile IMEI | nVarChar | 64 | - |  |  |
| 89 | `PrsWkCntEb` | Personal Work Center Enable | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 90 | `SnapShotId` | Snapshot ID | Int | 11 | - | 0 |  |
| 91 | `STData` | User Password Salt | nVarChar | 40 | - |  |  |
| 92 | `SupportUsr` | Support User | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 93 | `NoSTPwdNum` | Password encrypted w/o Salt (cryptography) | Int | 6 | - | 0 |  |
| 94 | `DomainUser` | Domain user name bound in SLD | nVarChar | 50 | - |  |  |
| 95 | `CUSAgree` | CUS Agreement | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 96 | `EmailSig` | E-Mail Signature | Text | 16 | - |  |  |
| 97 | `TPLId` | Template ID | Int | 6 | [UICU](UICU.md) |  |  |
| 98 | `DigCrtPath` | Digital Certificate Path | Text | 16 | - |  |  |
| 99 | `ShowNewTsk` | Open Worklist on Task Arrival | VarChar | 1 | - | Y | `N` = No<br>`Y` = Yes |
| 100 | `IntgrtEb` | Enable Setting Integration | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 101 | `AllBrnchF` | Allow Viewing of All (Including Unassigned To) Branches in Financial Reports | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 102 | `EvtNotify` | Allow Event Notification | VarChar | 1 | - | Y |  |
| 103 | `IgnDtOwn` | Ignore Data Ownership for this user | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 104 | `EnterAsTab` | Use Numeric Keypad Enter Key as Tab Key | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 105 | `DotAsSep` | Use Del Key As Separator | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 106 | `MouseOnly` | Document Operation by Mouse Only | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 107 | `Color` | Company Color | Int | 6 | - |  | `0` = Combined<br>`1` = Classic<br>`2` = Gray<br>`3` = Violet<br>`4` = Blue<br>`5` = Green<br>`6` = Yellow<br>`7` = Orange<br>`8` = Red<br>`9` = Brown |
| 108 | `SkinType` | Skin Type | nVarChar | 254 | - |  |  |
| 109 | `Font` | Font | nVarChar | 50 | - |  |  |
| 110 | `FontSize` | Font Size | Int | 11 | - |  |  |
| 111 | `NaturalPer` | Natural Person | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 112 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased<br>`B` = Blocked<br>`U` = Unblocked |
| 113 | `AutoAsnBPL` | Auto. Assign Branches | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 114 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 115 | `HandleEDoc` | Can Process Electronic Documents | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 116 | `ShowLicBal` | Show License Balloon | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 117 | `LicBaHDate` | License Balloon Hiding Date | Date | 8 | - |  |  |
| 118 | `ShowFstMsg` | Show Only Part of Message | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 119 | `ShowMsgNum` | The Number of Message to Show | Int | 11 | - | 100 |  |
| 120 | `LastClean` | Last Cleanup Date | Date | 8 | - |  |  |
| 121 | `CleanChb` | Checkbox of Message Cleanup | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 122 | `CleanIbx` | Checkbox of Cleanup Inbox | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 123 | `CleanObx` | Checkbox of Cleanup Outbox | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 124 | `CleanSnt` | Checkbox of Cleanup Sent | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 125 | `validFor` | Active | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 126 | `validFrom` | Active From | Date | 8 | - |  |  |
| 127 | `validTo` | Active To | Date | 8 | - |  |  |
| 128 | `frozenFor` | Inactive | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 129 | `frozenFrom` | Inactive From | Date | 8 | - |  |  |
| 130 | `frozenTo` | Inactive To | Date | 8 | - |  |  |
| 131 | `ValidComm` | Remarks for Active Period | nVarChar | 30 | - |  |  |
| 132 | `FrozenComm` | Remarks for Inactive Period | nVarChar | 30 | - |  |  |
| 133 | `AprvDsnc` | Approval Decision Notification | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 134 | `ReqAprvl` | Requests for Approval Notification | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 135 | `RnwBlktA` | Renew Blanket Agreement Reminders Notification | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 136 | `SvcClRem` | Service Call Reminders Notification | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 137 | `SvcClAsn` | Service Call Assignments Notification | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 138 | `WzdTsk` | Wizard Tasks Notification | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 139 | `RoPermMsg` | Pop up permission override for read-only forms | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 140 | `SvCnRnRm` | Service Contract Renewal Reminders | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | USERID, logInstanc |
