# 4.9.1.234 XMLEXTRACT Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 389–390

Returns an XML element that matches the specified XPath query.

## Syntax

```sql
XMLEXTRACT(<XML_document>, <XPath_query> [,<NamespaceDeclarations>])
```

## Syntax Elements

#### XML_document

Specifies an XML document of type CLOB, NCLOB, VARCHAR, or NVARCHAR.

#### XPath_query

Specifies an XPath expression of type VARCHAR or NVARCHAR.

#### NamespaceDeclarations

Specifies a namespace declaration of type VARCHAR or NVARCHAR.

## Description

Returns the matching XML element. The return value is of type VARCHAR/NVARCHAR or CLOB/NCLOB depending on the type given for `<XML_document>`.

If an XML element is empty (for example, `<name></name>`), then an empty result is returned. If an XML element is not found, then the function returns an error.

## Example

The following statement returns the `<name>` element from item 2 (the example returns `<name>Jar</name>`):

```sql
SELECT XMLEXTRACT(
   '<doc>
      <item><id>1</id><name>Box</name></item>
      <item><id>2</id><name>Jar</name></item>
   </doc>',
   '/doc/item[2]/name'
) FROM DUMMY;
```

The following statement returns `<ns1:name>Jar</ns1:name>`:

```sql
SELECT XMLEXTRACT(
   '<doc xmlns:ns1="http://namespace1.sap.com" xmlns:ns2="http://
namespace2.sap.com">
      <ns1:item><ns1:id>1</ns1:id><ns1:name>Box</ns1:name></ns1:item>
      <ns1:item><ns1:id>2</ns1:id><ns1:name>Jar</ns1:name></ns1:item>
      <ns2:item><ns2:id>3</ns2:id><ns2:name>Table</ns2:name></ns2:item>
   </doc>',
   '/doc/ns1:item[2]/ns1:name',
   'xmlns:ns1="http://namespace1.sap.com" xmlns:ns2="http://namespace2.sap.com"'
) FROM DUMMY;
```

## Related Information

[XMLEXTRACTVALUE Function (Miscellaneous)](XMLEXTRACTVALUE-Function-Miscellaneous.md)
