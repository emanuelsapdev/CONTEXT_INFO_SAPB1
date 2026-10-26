# 4.10.1.75 CREATE VIRTUAL PROCEDURE Statement (Procedural)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 872–875

Creates a virtual procedure using the specified programming language that allows execution of the procedure body at the specified remote source.

## Syntax

```sql
CREATE VIRTUAL PROCEDURE <proc_name> [(<parameter_clause>)]
  [SQL SECURITY <mode>]
  [<package_clause>] LANGUAGE <lang>
   AT <source_name>
[AS
  BEGIN
          <procedure_body>
   END
   ]
```

## Syntax Elements

#### proc_name

Specifies the virtual procedure name, with optional name.

```sql
<proc_name> ::= [<schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

#### parameter_clause

Specifies the input and output parameters for the procedure.

```sql
<parameter_clause> ::= <parameter> [{,<parameter>}...]
```

#### SQL SECURITY mode

Specifies the security mode of the virtual procedure.

```sql
<mode> ::= DEFINER | INVOKER
```

##### DEFINER

Performs the execution of the virtual procedure with the privileges of the definer of the procedure. DEFINER is the default.

##### INVOKER

Performs the execution of the virtual procedure with the privileges of the invoker of the procedure.

#### LANGUAGE

Specifies the programming language that is used in the procedure body.

```sql
LANGUAGE <lang>
<lang> ::= SCALASPARK
```

In this case, `SCALASPARK` implies that the procedure body will be in the Scala programming language.

#### package_clause

(Hadoop Integration only) This optional parameter defines the identifier of the virtual package containing the external library files used to execute the Scala code in the procedure body.

```sql
<package_clause> ::= PACKAGE <schema>.<jobPackage>
<schema> ::= <identifier>
<jobPackage> ::= <identifier>
```

#### AT source_name

Specifies the remote source for which the procedure is created and executed.

#### procedure_body

Defines the source code for the virtual procedure. Run complex algorithms on both structured (such as tables) and non-structured (such as log files) data using the specified language. Currently, Scala is the only supported language.

## Description

Creates a virtual procedure using the specified programming language that allows execution of the procedure body at the specified remote source.

## Permissions

This statement requires the CREATE VIRTUAL PROCEDURE object privilege.

## Example

```sql
CREATE VIRTUAL PROCEDURE SYSTEM.FINDNGRAMS(
IN N INT,
OUT NGRAMS TABLE(STR TEXT)
)
LANGUAGE SCALASPARK
AT SPARK_OAKL
AS
BEGIN
import sqlContext.implicits._
import scala.collection.mutable.WrappedArray
import org.apache.spark.ml.feature.NGram
    // $example on$
    val wordDataFrame = sqlContext.createDataFrame(Seq(
      (0, Array("Hi", "I", "heard", "about", "Spark")),
      (1, Array("I", "wish", "Java", "could", "use", "case", "classes")),
      (2, Array("Logistic", "regression", "models", "are", "neat"))
    )).toDF("id", "words")
    val ngram = new NGram().setN(N).setInputCol("words").setOutputCol("ngrams")
    val ngramDataFrame = ngram.transform(wordDataFrame)
    ngramDataFrame.select("ngrams").show(false)

    NGRAMS = ngramDataFrame.select("ngrams").
                        map(y=>y(0).asInstanceOf[WrappedArray[_]].
                        mkString(",")).toDF
END;
CALL FINDNGRAMS(6, ?);
```

## Related Information

VIRTUAL_PACKAGES System View [→](../../../6-System-Views-Reference/6.01-System-Views/VIRTUAL_PACKAGES-System-View.md) VIRTUAL_PROCEDURES System View [→](../../../6-System-Views-Reference/6.01-System-Views/VIRTUAL_PROCEDURES-System-View.md)
