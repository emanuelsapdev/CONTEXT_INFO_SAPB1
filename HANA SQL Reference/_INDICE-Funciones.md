# Índice de funciones SQL

Todas las funciones SQL de SAP HANA (sección 4.9.1), ordenadas alfabéticamente. Entre paréntesis: la categoría (String, Numeric, Datetime, Aggregate, Window, etc.).

| Función | Descripción (EN) |
| --- | --- |
| [ABAP_ALPHANUM (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ABAP_ALPHANUM-Function-String.md) | Converts a string to what would result if the string was transformed into an ALPHANUM type and then converted back to a string. |
| [ABAP_LOWER (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ABAP_LOWER-Function-String.md) | Converts all characters in a specified string to lowercase. |
| [ABAP_NUMC (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ABAP_NUMC-Function-String.md) | Converts an input string to a string of a specified length, that contains only digits. |
| [ABAP_UPPER (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ABAP_UPPER-Function-String.md) | Converts all characters in the specified string to uppercase. |
| [ABS (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ABS-Function-Numeric.md) | Returns the absolute value of a numeric argument. |
| [ACOS (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ACOS-Function-Numeric.md) | Returns the arc-cosine, in radians, of a numeric argument between -1 and 1. |
| [ADD_DAYS (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ADD_DAYS-Function-Datetime.md) | Computes the specified date, plus or minus the specified number of days. |
| [ADD_MONTHS (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ADD_MONTHS-Function-Datetime.md) | Computes the specified date plus the specified number of months. |
| [ADD_MONTHS_LAST (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ADD_MONTHS_LAST-Function-Datetime.md) | Computes the specified date plus the specified number of months, with the output date being the last day of the month if the input date is the last day of the month, even if those two dates differ. |
| [ADD_NANO100 (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ADD_NANO100-Function-Datetime.md) | Adds the specified number of 10^-7 unit of seconds to the specified TIMESTAMP value. |
| [ADD_SECONDS (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ADD_SECONDS-Function-Datetime.md) | Computes the specified time plus the specified seconds. |
| [ADD_WORKDAYS (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ADD_WORKDAYS-Function-Datetime.md) | Computes a date by adding a number of workdays to a starting date. |
| [ADD_YEARS (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ADD_YEARS-Function-Datetime.md) | Computes the specified date plus the specified years. |
| [ALLOW_PRECISION_LOSS (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ALLOW_PRECISION_LOSS-Function-Miscellaneous.md) | Allows loss of precision when aggregating decimal values using an aggregate expression. |
| [ASCII (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ASCII-Function-String.md) | Returns the integer ASCII value of the first character in a specified string. |
| [ASIN (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ASIN-Function-Numeric.md) | Returns the arc-sine, in radians, of a numeric argument. |
| [ATAN (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ATAN-Function-Numeric.md) | Returns the arc-tangent, in radians, of a numeric argument. |
| [ATAN2 (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ATAN2-Function-Numeric.md) | Returns the arc-tangent, in radians, of the ratio of two numbers. |
| [AUTO_CORR (Aggregate)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/AUTO_CORR-Function-Aggregate.md) | Computes all autocorrelation coefficients for a given input expression and returns an array of values. |
| [AVG (Aggregate)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/AVG-Function-Aggregate.md) | Returns the arithmetical mean of the expression. This function can also be used as a window function. |
| [BINNING (Window)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/BINNING-Function-Window.md) | Partitions an input set into disjoint subsets by assigning a bin number to each row. |
| [BINTOHEX (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/BINTOHEX-Function-String.md) | Converts a binary string to a VARCHAR hexadecimal value. |
| [BINTONHEX (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/BINTONHEX-Function-String.md) | Converts a binary value to a hexadecimal value as an NVARCHAR data type. |
| [BINTOSTR (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/BINTOSTR-Function-String.md) | Converts a VARBINARY string to a character string. |
| [BITAND (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/BITAND-Function-Numeric.md) | Performs an AND operation on the bits of two arguments. |
| [BITCOUNT (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/BITCOUNT-Function-Numeric.md) | Counts the number of set bits of an expression. |
| [BITNOT (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/BITNOT-Function-Numeric.md) | Performs a bitwise NOT operation on the bits of an expression. |
| [BITOR (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/BITOR-Function-Numeric.md) | This function performs an OR operation on the bits of two arguments. |
| [BITSET (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/BITSET-Function-Numeric.md) | Sets a specific number of bits to 1 in a target number from a specified 1-based index position. |
| [BITUNSET (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/BITUNSET-Function-Numeric.md) | Sets a specified number of bits to 0 in a target number from a specified 1-based index position. |
| [BITXOR (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/BITXOR-Function-Numeric.md) | Performs an XOR operation on the bits of two arguments. |
| [CARDINALITY (Array)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CARDINALITY-Function-Array.md) | Returns the number of elements in a specified array. |
| [CAST (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CAST-Function-Data-Type-Conversion.md) | Returns the value of an expression converted to a supplied data type. |
| [CEIL (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CEIL-Function-Numeric.md) | Returns the first integer that is greater than or equal to the specified value. |
| [CHAR (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CHAR-Function-String.md) | Returns the character that has the ASCII value of the specified number. |
| [COALESCE (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/COALESCE-Function-Miscellaneous.md) | Returns the first non-NULL expression from a specified list. |
| [CONCAT (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CONCAT-Function-String.md) | Returns a combined string consisting of two specified strings. |
| [CONCAT_NAZ (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CONCAT_NAZ-Function-String.md) | Returns a combined, non-null value string consisting of two specified strings. |
| [CONVERT_CURRENCY (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CONVERT_CURRENCY-Function-Miscellaneous.md) | Calculates values in different currencies. |
| [CONVERT_UNIT (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CONVERT_UNIT-Function-Miscellaneous.md) | Converts the specified source units to specified target units. |
| [CORR (Aggregate)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CORR-Function-Aggregate.md) | Computes the Pearson product momentum correlation coefficient between two columns. This function can also be used as a window function. |
| [CORR_SPEARMAN (Aggregate)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CORR_SPEARMAN-Function-Aggregate.md) | Returns the Spearman's rank correlation coefficient of the values found in the corresponding rows of two columns. This function can also be used as a window function. |
| [COS (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/COS-Function-Numeric.md) | Returns the cosine of the angle, in radians, for the specified argument. |
| [COSH (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/COSH-Function-Numeric.md) | Computes the hyperbolic cosine of the specified argument. |
| [COT (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/COT-Function-Numeric.md) | Computes the cotangent of a specified number. |
| [COUNT (Aggregate)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/COUNT-Function-Aggregate.md) | Counts the number of rows returned by a query. This function can also be used as a window function. |
| [CROSS_CORR (Aggregate)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CROSS_CORR-Function-Aggregate.md) | Computes all cross-correlation coefficients between two given expressions. |
| [CUBIC_SPLINE_APPROX (Window)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CUBIC_SPLINE_APPROX-Function-Window.md) | Replaces null values by interpolating the gaps based on calculated cubic splines and linearly extrapolating any leading or trailing null values. |
| [CUME_DIST (Window)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CUME_DIST-Function-Window.md) | Returns the relative rank of a row. |
| [CURRENT_CONNECTION (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CURRENT_CONNECTION-Function-Miscellaneous.md) | Returns the ID of the current connection. |
| [CURRENT_DATE (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CURRENT_DATE-Function-Datetime.md) | Returns the current local system date. |
| [CURRENT_IDENTITY_VALUE (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CURRENT_IDENTITY_VALUE-Function-Miscellaneous.md) | Returns the latest inserted identity value in the current session. |
| [CURRENT_MVCC_SNAPSHOT_TIMESTAMP (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CURRENT_MVCC_SNAPSHOT_TIMESTAMP-Function-Datetime.md) | Returns the timestamp of the current MVCC snapshot in SSSS format (seconds past midnight). |
| [CURRENT_OBJECT_SCHEMA (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CURRENT_OBJECT_SCHEMA-Function-Miscellaneous.md) | Returns the current schema name when creating a view. |
| [CURRENT_SCHEMA (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CURRENT_SCHEMA-Function-Miscellaneous.md) | Returns a string containing the current schema name. |
| [CURRENT_SITE_ID (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CURRENT_SITE_ID-Function-Miscellaneous.md) | Returns the ID of the site that is calling the function. This function is primarily for use in SAP HANA System Replication (HSR). |
| [CURRENT_TIME (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CURRENT_TIME-Function-Datetime.md) | Returns the local system time. |
| [CURRENT_TIMESTAMP (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CURRENT_TIMESTAMP-Function-Datetime.md) | Returns the current local system timestamp information. |
| [CURRENT_TRANSACTION_ISOLATION_LEVEL (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CURRENT_TRANSACTION_ISOLATION_LEVEL-Function-Miscellaneous.md) | Returns a string containing the current transaction isolation level. |
| [CURRENT_UPDATE_STATEMENT_SEQUENCE (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CURRENT_UPDATE_STATEMENT_SEQUENCE-Function-Miscellaneous.md) | Returns the number of write statements that have been issued in a transaction incremented by 1. |
| [CURRENT_UPDATE_TRANSACTION (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CURRENT_UPDATE_TRANSACTION-Function-Miscellaneous.md) | Returns the unique ID of the current transaction when it is in write mode. |
| [CURRENT_USER (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CURRENT_USER-Function-Miscellaneous.md) | Returns the current user name at the current statement context. |
| [CURRENT_USER_ID (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CURRENT_USER_ID-Function-Miscellaneous.md) | Returns the current user's user ID at the current statement context. |
| [CURRENT_UTCDATE (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CURRENT_UTCDATE-Function-Datetime.md) | Returns the current UTC date. |
| [CURRENT_UTCTIME (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CURRENT_UTCTIME-Function-Datetime.md) | Returns the current UTC time. |
| [CURRENT_UTCTIMESTAMP (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CURRENT_UTCTIMESTAMP-Function-Datetime.md) | Returns the current UTC timestamp. |
| [DAYNAME (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/DAYNAME-Function-Datetime.md) | Returns the weekday name for the specified date. |
| [DAYOFMONTH (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/DAYOFMONTH-Function-Datetime.md) | Returns the day of the month for the specified date. |
| [DAYOFYEAR (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/DAYOFYEAR-Function-Datetime.md) | Returns an integer representation of the day of the year for the specified date. |
| [DAYS_BETWEEN (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/DAYS_BETWEEN-Function-Datetime.md) | Computes the number of entire (24 hour) days between two dates. |
| [DENSE_RANK (Window)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/DENSE_RANK-Function-Window.md) | Performs the same ranking operation as the RANK function, except that rank numbering does not skip when ties are found. |
| [DFT (Aggregate)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/DFT-Function-Aggregate.md) | Computes expressions and returns an array with specific elements. |
| [ENCRYPTION_ROOT_KEYS_EXTRACT_ALL_KEYS_FOR_DATABASE (Security)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ENCRYPTION_ROOT_KEYS_EXTRACT_ALL_KEYS_FOR_DATABASE-Function.md) | Extracts all the encryption root keys of a database and sends them to a client session as a CLOB. |
| [ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS (Security)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS-Function-Security.md) | Extracts root keys and sends them to a client session as a CLOB. |
| [ENCRYPTION_ROOT_KEYS_HAS_BACKUP_PASSWORD (Security)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ENCRYPTION_ROOT_KEYS_HAS_BACKUP_PASSWORD-Function-Security.md) | Returns a value that indicates whether the root key backup password is set. |
| [ESCAPE_DOUBLE_QUOTES (Security)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ESCAPE_DOUBLE_QUOTES-Function-Security.md) | Escapes double quotes in the specified string. |
| [ESCAPE_SINGLE_QUOTES (Security)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ESCAPE_SINGLE_QUOTES-Function-Security.md) | Escapes single quotes in the specified string. |
| [EXP (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/EXP-Function-Numeric.md) | Returns the result of the base of the natural logarithms e raised to the power of the specified argument. |
| [EXPRESSION_MACRO (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/EXPRESSION_MACRO-Function-Miscellaneous.md) | Returns aggregated results from a query. |
| [EXTRACT (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/EXTRACT-Function-Datetime.md) | Returns the requested portion of a specified date. |
| [FIRST_VALUE (Aggregate)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/FIRST_VALUE-Function-Aggregate.md) | Returns the value of the first element of an expression. This function can also be used as a window function. |
| [FLOOR (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/FLOOR-Function-Numeric.md) | Returns the largest integer that is not greater than the specified numeric argument. |
| [GENERATE_PASSWORD (Security)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/GENERATE_PASSWORD-Function-Security.md) | Generates a password. |
| [GREATEST (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/GREATEST-Function-Miscellaneous.md) | Returns the greatest value among the specified arguments. |
| [GROUPING (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/GROUPING-Function-Miscellaneous.md) | Determines whether a specified column is used in grouping. |
| [GROUPING_ID (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/GROUPING_ID-Function-Miscellaneous.md) | Returns an integer value to identify which grouping set each row belongs to. |
| [HAMMING_DISTANCE (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/HAMMING_DISTANCE-Function-String.md) | Performs a bitwise or bytewise comparison between two arguments and returns the hamming distance. |
| [HASH_MD5 (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/HASH_MD5-Function-Miscellaneous.md) | Returns a 32 byte hash value of the concatenated arguments. |
| [HASH_SHA256 (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/HASH_SHA256-Function-Miscellaneous.md) | Returns a 32 byte hash value of the concatenated arguments. |
| [HEXTOBIN (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/HEXTOBIN-Function-String.md) | Converts a string of hexadecimal characters to a VARBINARY value. |
| [HEXTONUM (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/HEXTONUM-Function-String.md) | Converts a hexadecimal value to a BIGINT string value. |
| [HOUR (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/HOUR-Function-Datetime.md) | Returns an integer representation of the hour portion of the specified time. |
| [IFNULL (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/IFNULL-Function-Miscellaneous.md) | Returns the first non-NULL input expression. |
| [INDEXING_ERROR_CODE (Fulltext)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/INDEXING_ERROR_CODE-Function-Fulltext.md) | Returns the indexing error codes for values in a column that has a fulltext index on it. |
| [INDEXING_ERROR_MESSAGE (Fulltext)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/INDEXING_ERROR_MESSAGE-Function-Fulltext.md) | Returns the indexing error messages for values in a column that has a fulltext index on it. |
| [INDEXING_STATUS (Fulltext)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/INDEXING_STATUS-Function-Fulltext.md) | Returns the indexing status of values in a column that has a fulltext index. |
| [INITCAP (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/INITCAP-Function-String.md) | Converts the first character of each word in a specified string to uppercase and converts remaining characters to lowercase. |
| [IS_SQL_INJECTION_SAFE (Security)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/IS_SQL_INJECTION_SAFE-Function-Security.md) | Checks a specified SQL identifier for possible SQL injection risks. |
| [ISOWEEK (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ISOWEEK-Function-Datetime.md) | Returns the ISO year and week number for a specified date. |
| [JSON_QUERY (JSON)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/JSON_QUERY-Function-JSON.md) | Extracts JSON text from a JSON context item by using a SQL/JSON path expression. |
| [JSON_TABLE (JSON)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/JSON_TABLE-Function-JSON.md) | Queries a JSON text and presents it as a relational table. |
| [JSON_VALUE (JSON)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/JSON_VALUE-Function-JSON.md) | Extracts an SQL value of a predefined type from a JSON value. |
| [LAG (Window)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/LAG-Function-Window.md) | Returns the value of the offset rows before the current row. |
| [LANGUAGE (Fulltext)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/LANGUAGE-Function-Fulltext.md) | Returns the language of the specified column entries. |
| [LAST_DAY (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/LAST_DAY-Function-Datetime.md) | Returns the date of the last day of the month that contains the specified date. |
| [LAST_VALUE (Aggregate)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/LAST_VALUE-Function-Aggregate.md) | Returns the value of the last element of an expression. This function can also be used as a window function. |
| [LCASE (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/LCASE-Function-String.md) | Converts all characters in a string to lowercase. |
| [LEAD (Window)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/LEAD-Function-Window.md) | Returns the offset of rows after the current row. The `<offset>` should be non-negative and its default is 1. |
| [LEAST (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/LEAST-Function-Miscellaneous.md) | Returns the lesser value of two specified arguments. |
| [LEFT (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/LEFT-Function-String.md) | Returns the specified number of characters or bytes of a string, starting from the left side. |
| [LENGTH (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/LENGTH-Function-String.md) | Returns the number of characters in a string. |
| [LINEAR_APPROX (Window)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/LINEAR_APPROX-Function-Window.md) | Operates on an entire series to produce a new series that replaces missing values by interpolating between adjacent non-NULL values and extrapolating any leading or trailing null values. |
| [LN (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/LN-Function-Numeric.md) | Returns the natural logarithm of a number. |
| [LOCALTOUTC (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/LOCALTOUTC-Function-Datetime.md) | A timestamp parameter holding the time to be converted between UTC and local time. |
| [LOCATE (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/LOCATE-Function-String.md) | Returns the position of a substring within a string. |
| [LOCATE_REGEXPR (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/LOCATE_REGEXPR-Function-String.md) | Searches a string for a regular expression pattern and returns an integer indicating the beginning position, or the ending position plus 1, of one occurrence of the matched substring. |
| [LOG (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/LOG-Function-Numeric.md) | Returns the natural logarithm of a specified number and base. |
| [LOWER (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/LOWER-Function-String.md) | Converts all characters in a string to lowercase. |
| [LPAD (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/LPAD-Function-String.md) | Left-pads a string with spaces, or a specified pattern, to make a string of a specified number of characters in length. |
| [LTRIM (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/LTRIM-Function-String.md) | Returns a string, trimmed of all leading spaces. |
| [MAP (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/MAP-Function-Miscellaneous.md) | Searches for an expression within a set of values and returns a specified result. |
| [MAX (Aggregate)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/MAX-Function-Aggregate.md) | Returns the maximum value of the expression. This function can also be used as a window function. |
| [MEDIAN (Aggregate)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/MEDIAN-Function-Aggregate.md) | Finds the statistical median of an input expression with a numeric data type. This function can also be used as a window function. |
| [MEMBER_AT (Array)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/MEMBER_AT-Function-Array.md) | Returns values from a specified array position. |
| [MIMETYPE (Fulltext)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/MIMETYPE-Function-Fulltext.md) | Returns the MIME type of a value in a column that has a fulltext index. |
| [MIN (Aggregate)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/MIN-Function-Aggregate.md) | Returns the minimum value of the expression. This function can also be used as a window function. |
| [MINUTE (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/MINUTE-Function-Datetime.md) | Returns an integer representation of the minute for the specified time. |
| [MOD (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/MOD-Function-Numeric.md) | Returns the remainder of a specified number divided by a specified divisor. |
| [MONTH (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/MONTH-Function-Datetime.md) | Returns the number of the month from the specified date. |
| [MONTHNAME (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/MONTHNAME-Function-Datetime.md) | Returns the name of the month for the specified date. |
| [MONTHS_BETWEEN (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/MONTHS_BETWEEN-Function-Datetime.md) | Computes the number of months between two dates. |
| [NANO100_BETWEEN (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/NANO100_BETWEEN-Function-Datetime.md) | Computes the time difference between two dates to the precision of 0.1 microseconds. |
| [NCHAR (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/NCHAR-Function-String.md) | Returns the Unicode character with the specified code number. |
| [NDIV0 (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/NDIV0-Function-Numeric.md) | Returns 0 when divided by 0; otherwise, it returns the result of the division. |
| [NEWUID (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/NEWUID-Function-Miscellaneous.md) | Creates a unique identifier within an SAP HANA database. |
| [NEXT_DAY (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/NEXT_DAY-Function-Datetime.md) | Returns the date of the day following the specified date. |
| [NORMALIZE (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/NORMALIZE-Function-String.md) | Applies a normalizing format to a character value expression and returns a normalized string. |
| [NOW (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/NOW-Function-Datetime.md) | Returns the current timestamp. |
| [NTH_VALUE (Aggregate)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/NTH_VALUE-Function-Aggregate.md) | Returns the value of an element at a specific position in an expression. This function can also be used as a window function. |
| [NTILE (Window)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/NTILE-Function-Window.md) | Distributes rows into a specified number of buckets and assigns the bucket number starting from 1 to each row in the bucket. |
| [NULLIF (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/NULLIF-Function-Miscellaneous.md) | Determines whether two expressions are equal. |
| [NUMTOHEX (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/NUMTOHEX-Function-String.md) | Converts a numeric value to a hexadecimal value. |
| [OCCURRENCES_REGEXPR (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/OCCURRENCES_REGEXPR-Function-String.md) | Returns the number of matches of a regular expression search within a string. |
| [PERCENT_RANK (Window)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/PERCENT_RANK-Function-Window.md) | Calculates the percentage of values that are either less than or greater than the current value, per the ORDER BY specification for the window. |
| [PERCENTILE_CONT (Window)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/PERCENTILE_CONT-Function-Window.md) | Returns an interpolated value using the percentile value of a constant. |
| [PERCENTILE_DISC (Window)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/PERCENTILE_DISC-Function-Window.md) | Returns the first value whose cumulative distribution value is greater than or equal to the percentile value of a constant. |
| [PLAINTEXT (Fulltext)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/PLAINTEXT-Function-Fulltext.md) | Returns the plain text representation of a value in a column that has a full text index. |
| [POWER (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/POWER-Function-Numeric.md) | Calculates a specified base number raised to the power of a specified exponent. |
| [QUARTER (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/QUARTER-Function-Datetime.md) | Returns the quarter for the specified date. |
| [RAND (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/RAND-Function-Numeric.md) | Returns a pseudo-random DOUBLE value. |
| [RAND_SECURE (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/RAND_SECURE-Function-Numeric.md) | Returns a pseudo-random value that is safe for cryptographic or security purposes. |
| [RANDOM_PARTITION (Window)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/RANDOM_PARTITION-Function-Window.md) | Partitions an input set randomly into three disjoint subsets by assigning a set number to each row of the input set. |
| [RANK (Window)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/RANK-Function-Window.md) | Returns rank of a row within a partition, starting from 1. |
| [RECORD_COMMIT_TIMESTAMP (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/RECORD_COMMIT_TIMESTAMP-Function-Miscellaneous.md) | Returns a COMMIT timestamp for the specified row of the given table. |
| [RECORD_ID (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/RECORD_ID-Function-Miscellaneous.md) | Generates an ID for each row of the results. |
| [REPLACE (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/REPLACE-Function-String.md) | Searches within a string for all occurrences of a specified string and replaces them with another specified string. |
| [REPLACE_REGEXPR (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/REPLACE_REGEXPR-Function-String.md) | Searches a string for a regular expression pattern and returns the string with either one or every occurrence of the regular expression pattern that is replaced using a replacement string. |
| [RESULT_CACHE_ID (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/RESULT_CACHE_ID-Function-Miscellaneous.md) | Returns the cache ID of a result cache entry. |
| [RESULT_CACHE_REFRESH_TIME (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/RESULT_CACHE_REFRESH_TIME-Function-Miscellaneous.md) | Returns the last cache refresh time of a result cache entry. |
| [RIGHT (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/RIGHT-Function-String.md) | Returns the specified number of characters/bytes of a string, starting from the right side. |
| [ROUND (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ROUND-Function-Numeric.md) | Rounds the specified argument to the specified amount of places after the decimal point. |
| [ROW_NUMBER (Window)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ROW_NUMBER-Function-Window.md) | Sequentially numbers the rows within a partition of a result set, with the first row of each partition assigned as 1. |
| [RPAD (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/RPAD-Function-String.md) | Right-pads a string with spaces or a specified pattern to make a string that is a specified number of characters in length. |
| [RTRIM (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/RTRIM-Function-String.md) | Returns a string trimmed of all trailing spaces. |
| [SCORE (Fulltext)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/SCORE-Function-Fulltext.md) | Returns the relevance of a record that has been found. |
| [SECOND (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/SECOND-Function-Datetime.md) | Returns the second portion of a specified time. |
| [SECONDS_BETWEEN (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/SECONDS_BETWEEN-Function-Datetime.md) | Computes the number of seconds between two specified dates. |
| [SERIES_DISAGGREGATE (Series Data)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/SERIES_DISAGGREGATE-Function-Series-Data.md) | Generates a complete series table with rows disaggregated into defined partitions. |
| [SERIES_ELEMENT_TO_PERIOD (Series Data)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/SERIES_ELEMENT_TO_PERIOD-Function-Series-Data.md) | Returns the series period value associated with the specified one-based series element number. |
| [SERIES_FILTER (Window)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/SERIES_FILTER-Function-Window.md) | Performs a filtered calculation on a series of data. |
| [SERIES_GENERATE (Series Data)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/SERIES_GENERATE-Function-Series-Data.md) | Generates a complete series table based on the specified series definition. |
| [SERIES_PERIOD_TO_ELEMENT (Series Data)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/SERIES_PERIOD_TO_ELEMENT-Function-Series-Data.md) | Returns the one-based series element number that the given period value is associated with. |
| [SERIES_ROUND (Series Data)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/SERIES_ROUND-Function-Series-Data.md) | Rounds a specified value to the series value using the specified rounding settings. |
| [SESSION_CONTEXT (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/SESSION_CONTEXT-Function-Miscellaneous.md) | Returns the value of the specified session variable assigned to the current user. |
| [SESSION_USER (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/SESSION_USER-Function-Miscellaneous.md) | Returns the user name of the current session. |
| [SIGN (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/SIGN-Function-Numeric.md) | Returns the sign (positive or negative) of the specified numeric argument. |
| [SIN (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/SIN-Function-Numeric.md) | Returns the sine of an angle expressed in radians. |
| [SINH (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/SINH-Function-Numeric.md) | Returns the hyperbolic sine of an angle expressed in radians. |
| [SOUNDEX (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/SOUNDEX-Function-String.md) | Converts alphabet characters into a sound code that represents their sound. |
| [SQRT (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/SQRT-Function-Numeric.md) | Returns the square root of the specified argument. |
| [STDDEV (Aggregate)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/STDDEV-Function-Aggregate.md) | Returns the standard deviation of the given expression as the square root of the VAR function. This function can also be used as a window function. |
| [STDDEV_POP (Aggregate)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/STDDEV_POP-Function-Aggregate.md) | Returns the standard deviation of a given expression as the square root of the VAR_POP function. |
| [STDDEV_SAMP (Aggregate)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/STDDEV_SAMP-Function-Aggregate.md) | Returns the standard deviation of the given expression as the square root of VAR_SAMP function. |
| [STRING_AGG (Aggregate)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/STRING_AGG-Function-Aggregate.md) | Returns the concatenation string of the specified expression. |
| [STRTOBIN (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/STRTOBIN-Function-String.md) | Converts all characters in a string into a binary encoding using the specified codepage. |
| [SUBARRAY (Array)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/SUBARRAY-Function-Array.md) | Returns a subset of values from the specified array beginning from the specified start position. |
| [SUBSTR_AFTER (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/SUBSTR_AFTER-Function-String.md) | Returns a substring from a specified string that follows the first occurrence of the specified pattern. |
| [SUBSTR_BEFORE (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/SUBSTR_BEFORE-Function-String.md) | Returns a substring from a specified string before the first occurrence of the specified pattern. |
| [SUBSTRING (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/SUBSTRING-Function-String.md) | Returns a substring from an input value, starting from a specified position within the input value. |
| [SUBSTRING_REGEXPR (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/SUBSTRING_REGEXPR-Function-String.md) | Searches a string for a regular expression pattern and returns one occurrence of the matching substring. |
| [SUM (Aggregate)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/SUM-Function-Aggregate.md) | Returns the sum of the expression. This function can also be used as a window function. |
| [SYSUUID (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/SYSUUID-Function-Miscellaneous.md) | Returns a new universally unique identifier that is generated by the connected SAP HANA instance. |
| [TAN (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TAN-Function-Numeric.md) | Returns the tangent of a specified number, where the argument is an angle expressed in radians. |
| [TANH (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TANH-Function-Numeric.md) | Returns the hyperbolic tangent of the specified numeric argument. |
| [TO_ALPHANUM (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TO_ALPHANUM-Function-Data-Type-Conversion.md) | Converts a given value to an ALPHANUM data type. |
| [TO_BIGINT (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TO_BIGINT-Function-Data-Type-Conversion.md) | Converts a value to a BIGINT data type. |
| [TO_BINARY (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TO_BINARY-Function-Data-Type-Conversion.md) | Converts a value to a BINARY data type. |
| [TO_BLOB (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TO_BLOB-Function-Data-Type-Conversion.md) | Converts a binary string or (N)CLOB data type to a BLOB data type. |
| [TO_BOOLEAN (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TO_BOOLEAN-Function-Data-Type-Conversion.md) | Converts a value to a BOOLEAN data type. |
| [TO_CLOB (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TO_CLOB-Function-Data-Type-Conversion.md) | Converts a value to a CLOB data type. |
| [TO_DATE (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TO_DATE-Function-Data-Type-Conversion.md) | Converts a date string into a DATE data type. |
| [TO_DATS (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TO_DATS-Function-Data-Type-Conversion.md) | Converts a date string into an ABAP DATE string. |
| [TO_DECIMAL (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TO_DECIMAL-Function-Data-Type-Conversion.md) | Converts a value to a DECIMAL data type. |
| [TO_DOUBLE (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TO_DOUBLE-Function-Data-Type-Conversion.md) | Converts a value to a DOUBLE data type. |
| [TO_FIXEDCHAR (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TO_FIXEDCHAR-Function-Data-Type-Conversion.md) | Converts a specified number of characters from a string starting at the first character in the string. |
| [TO_INT (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TO_INT-Function-Data-Type-Conversion.md) | Converts a value to an INT data type. |
| [TO_INTEGER (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TO_INTEGER-Function-Data-Type-Conversion.md) | Converts the `<value>` to an INTEGER data type. |
| [TO_JSON_BOOLEAN (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TO_JSON_BOOLEAN-Data-Type-Conversion.md) | Converts a given `<value>` to a boolean value in JSON format. |
| [TO_NCLOB (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TO_NCLOB-Function-Data-Type-Conversion.md) | Converts a `<value>` to an NCLOB data type. |
| [TO_NVARCHAR (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TO_NVARCHAR-Function-Data-Type-Conversion.md) | Converts a given value to an NVARCHAR data type, with an option to format the output value. |
| [TO_REAL (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TO_REAL-Function-Data-Type-Conversion.md) | Converts a `<value>` to a REAL data type. |
| [TO_SECONDDATE (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TO_SECONDDATE-Function-Data-Type-Conversion.md) | Converts a specified date string to a SECONDDATE data type. |
| [TO_SMALLDECIMAL (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TO_SMALLDECIMAL-Function-Data-Type-Conversion.md) | Converts the specified value to a SMALLDECIMAL data type. |
| [TO_SMALLINT (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TO_SMALLINT-Function-Data-Type-Conversion.md) | Converts a value to a SMALLINT data type. |
| [TO_TIME (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TO_TIME-Function-Data-Type-Conversion.md) | Converts a specified time string to a TIME data type. |
| [TO_TIMESTAMP (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TO_TIMESTAMP-Function-Data-Type-Conversion.md) | Converts a date string to a TIMESTAMP data type. |
| [TO_TINYINT (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TO_TINYINT-Function-Data-Type-Conversion.md) | Converts a value to a TINYINT data type. |
| [TO_VARCHAR (Data Type Conversion)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TO_VARCHAR-Function-Data-Type-Conversion.md) | Converts a given value to an NVARCHAR data type, with an option to format the output value. It is a synonym of the TO_NVARCHAR function. |
| [TRIM (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TRIM-Function-String.md) | Returns a string after removing leading and trailing spaces. |
| [TRIM_ARRAY (Array)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/TRIM_ARRAY-Function-Array.md) | Removes the specified number of elements from the end of an array. |
| [UCASE (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/UCASE-Function-String.md) | Converts all characters in the specified string to uppercase. |
| [UMINUS (Numeric)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/UMINUS-Function-Numeric.md) | Returns the negated value of the specified numeric argument. |
| [UNICODE (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/UNICODE-Function-String.md) | Returns an integer containing the Unicode code point of the first character in the specified string. |
| [UPPER (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/UPPER-Function-String.md) | Converts all characters in a string to uppercase. |
| [UTCTOLOCAL (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/UTCTOLOCAL-Function-Datetime.md) | Converts the specified timestamp between UTC and local time. |
| [VAR (Aggregate)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/VAR-Function-Aggregate.md) | Returns the variance of the given expression as the square of the standard deviation. This function can also be used as a window function. |
| [VAR_POP (Aggregate)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/VAR_POP-Function-Aggregate.md) | Returns the population variance of an expression. |
| [VAR_SAMP (Aggregate)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/VAR_SAMP-Function-Aggregate.md) | Returns the sample variance of an expression. |
| [WEEK (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/WEEK-Function-Datetime.md) | Returns a week number between 1 and 54 for the specified date. |
| [WEEKDAY (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/WEEKDAY-Function-Datetime.md) | Returns the day of the week for the specified date. |
| [WEIGHTED_AVG (Window)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/WEIGHTED_AVG-Function-Window.md) | Computes a weighted moving average by using arithmetically decreasing weights. |
| [WIDTH_BUCKET (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/WIDTH_BUCKET-Function-Miscellaneous.md) | Returns the bucket number that has been assigned to the result of a specified expression. |
| [WORKDAYS_BETWEEN (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/WORKDAYS_BETWEEN-Function-Datetime.md) | Computes the number of workdays between a specified start date and a specified end date. |
| [XMLEXTRACT (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/XMLEXTRACT-Function-Miscellaneous.md) | Returns an XML element that matches the specified XPath query. |
| [XMLEXTRACTVALUE (Miscellaneous)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/XMLEXTRACTVALUE-Function-Miscellaneous.md) | Returns an XML value that matches the specified XPath query. |
| [XMLTABLE (String)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/XMLTABLE-Function-String.md) | Creates a relational table from an XML string. |
| [YEAR (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/YEAR-Function-Datetime.md) | Returns the year number of a specified date. |
| [YEARS_BETWEEN (Datetime)](4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/YEARS_BETWEEN-Function-Datetime.md) | Computes the number of years between two specified dates. |
