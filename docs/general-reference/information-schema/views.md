---
layout: default
title: Views
nav_order: 4
parent: Information schema and usage views
grand_parent: General reference
---

# Information schema for views
You can use the `information_schema.views` view to return information about each view in a database. The view is available for each database and contains one row for each view in the database. You can use a `SELECT` query to return information about each view as shown in the example below.

```sql
SELECT
  *
FROM
  information_schema.views;
```

## Columns in information_schema.views

Each row has the following columns with information about each view.

| Name                        | Data Type   | Description |
| :---------------------------| :-----------| :-----------|
| table_catalog               | STRING      | Name of the catalog. Firebolt offers a single ‘default’ catalog. |
| table_schema                | STRING      | The name of the database. |
| table_name                  | STRING      | The name of the view. |
| ddl                         | STRING      | The query statement that defines the view. |
| view_definition             | STRING      | The query statement that defines the view. |
| check_option                | NULL        | Not applicable for Firebolt. |
| is_updatable                | NULL        | Not applicable for Firebolt. |
| insertable_into             | NULL        | Not applicable for Firebolt. |
| created                     | TIMESTAMP   | The time that the view was created. |
| last_altered                | TIMESTAMP   | The time that the view was last changed. |
| description                 | NULL        | Not applicable for Firebolt. |
