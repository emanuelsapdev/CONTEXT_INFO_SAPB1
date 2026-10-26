# 4.10.1.51 CREATE GRAPH WORKSPACE Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 719–721

Creates a graph workspace.

## Syntax

```sql
CREATE GRAPH WORKSPACE <workspace_name>
   EDGE TABLE <edge_table_name>
      SOURCE COLUMN <source_column_name>
      TARGET COLUMN <target_column_name>
      KEY COLUMN <edge_key_column_name>
   VERTEX TABLE <vertex_table_name>
      KEY COLUMN <vertex_key_column_name>
```

## Syntax Elements

#### workspace_name

Specifies a name for the workspace.

#### edge_table_name

Specifies the name of the table containing the relationships between vertices (edge table).

```sql
<edge_table_name> ::= [<schema_name>.]<identifier>
```

#### source_column_name

Specifies the source column for an edge in the graph.

```sql
<source_column_name> ::= <identifier>
```

#### target_column_name

Specifies the target column for an edge in the graph.

```sql
<target_column_name> ::= <identifier>
```

#### edge_key_column_name

Specifies unique IDs for the edges in the graph.

```sql
<edge_key_column_name> ::= <identifier>
```

#### vertex_table_name

Specifies the name of the table containing the vertices (members) of the graph.

```sql
<vertex_table_name> ::= [<schema_name>.]<identifier>
```

#### vertex_key_column_name

Specifies unique IDs for the vertices in the graph.

```sql
<vertex_key_column_name> ::= <identifier>
```

## Description

A graph is modeled as a set of vertices and a set of edges. An edge connects two vertices; one vertex is denoted as source and the other as target. There might be two or more edges connecting the same two vertices. The set of vertices is stored in a vertex table and the set of edges is stored in an edge table. One of the vertex columns needs to uniquely identify vertices. Such column is also referred to as vertex key. Similarly, one of the edge columns needs to uniquely identify edges and is referred to as edge key. The edge table contains two additional columns referencing the key column of the vertex table. One of them identifies the source vertex and the other identifies the target vertex.

Key columns of the edge and vertex columns must be UNIQUE and NOT NULL. The target and source columns must be NOT NULL and of the same type as the vertex key column. The data types VARCHAR, NVARCHAR and INT can be used for key columns.

Extensive documentation on using graphs is found in the SAP HANA Graph Reference.

## Example

Create the graph workspace "FAMILY_TREE.GENEALOGY" by defining the vertices and edges for the family tree.

```sql
CREATE SCHEMA "FAMILY_TREE";
CREATE COLUMN TABLE "FAMILY_TREE"."VERTICES" ("KEY" VARCHAR(1024) NOT NULL
UNIQUE);
CREATE COLUMN TABLE "FAMILY_TREE"."EDGES" ("SOURCE" VARCHAR(1024) NOT NULL,
"TARGET" VARCHAR(1024) NOT NULL, "ID" INT NOT NULL UNIQUE);
CREATE GRAPH WORKSPACE FAMILY_TREE.GENEALOGY
        EDGE TABLE FAMILY_TREE.EDGES
          SOURCE COLUMN "SOURCE"
          TARGET COLUMN "TARGET"
          KEY COLUMN ID
        VERTEX TABLE FAMILY_TREE.VERTICES
            KEY COLUMN "KEY";
```
