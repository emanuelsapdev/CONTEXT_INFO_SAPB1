# 6.2.198 M_PASSWORD_POLICY System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1922–1924

Defines effective password policy settings.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |

PROPERTY VARCHAR(128) Displays the configuration property.

The following describes the contents of the individual lines of the monitor view (`VALUE`), as identified by `PROPERTY`:

**force_first_password_change** Dis plays if a user is forced to change their administrator-given password before being allowed to work any further. This property is only appli cable to users connecting using their SAP HANA database user name and password. **last_used_passwords** Displays the number of recently used pass words of a user, which they cannot reuse.

###### maximum_invalid_connect_at

**tempts** Displays the maximum number of allowed invalid connect attempts before a user is locked out. **maximum_password_lifetime** Dis plays the number of days that a password stays valid.

###### maximum_unused_initial_pass

**word_lifetime** Displays the num ber of days that an unused admin istrator-given password stays valid.

> **Note**
>
> In SAP HANA 1.0 SP 12 and earlier, the parameter name is

|   |   | `maximum_unused_inita l_password_lifetime` (note the missing 'i' in 'initial'). Use of the previous spelling is supported, but it is recommended that you update your |
| --- | --- | --- |

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
|   |   | configuration to use the correct spelling.<br>**maximum_unused_productive_password_lifetime** Displays the number of days that an unused user-given password stays valid. **minimal_password_length** Displays the minimum number of characters required by a valid password. **minimum_password_lifetime** Displays the minimum number of days before a user-given password can be changed by that user. **password_expire_warning_time** Displays that warnings about nearly expired passwords are shown at the configured number of days before expiration. **password_layout** Describes the kind(s) of characters that the pass word must consist of. **password_lock_time** Displays the number of minutes the user is locked out after too many invalid connect attempts. |
| VALUE | VARCHAR(128) | Displays the value. |

> **Note**
>
>

## Related Information

CREATE USERGROUP Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-USERGROUP-Statement-Access-Control.md) ALTER USERGROUP Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-USERGROUP-Statement-Access-Control.md) M_EFFECTIVE_PASSWORD_POLICY System View [→](M_EFFECTIVE_PASSWORD_POLICY-System-View.md)
