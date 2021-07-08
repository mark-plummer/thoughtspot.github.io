---
title: [Hide a column or define a synonym]
last_updated: tbd
summary: "Hide a column from users or make it easier to find by assigning a synonym."
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---

You can hide columns from users in ThoughtSpot without dropping them from the
database. It is common to hide a column when its data contains identifier
columns that are used to join tables, but which do not have any meaning to
users.

Alternatively, rather than hiding a column, you can make it easier to find by
creating synonyms for it. This is helpful, for example, when different
departments refer to the data using different terminology.

## Hide a column

As the number of columns in the dataset increases, the search experience
requires more effort. Users have to navigate through larger numbers of columns
to choose the correct one. There might also be some columns in the dataset that
you don’t want to expose to the users.

When you hide a worksheet, table, or view column, you only hide it from users without *edit* privileges on the object. Administrators and users with edit privileges on the object can still see and interact with the hidden column. Users without edit privileges for the object cannot see or interact with the hidden column.

To hide a column, change the **HIDDEN** (UI)/**Hide** (model file) setting. By
default, all columns in a data source appear in ThoughtSpot. To hide these
columns, set the **HIDDEN** setting to `YES`.

1. Find the **HIDDEN** (UI)/**Hide** (model file) setting for a column.
2. Set its value to `YES`.
3. Save your changes.

## Create synonyms for a column

When users search a data source, they might try typing different words to try to
retrieve a particular column. This could be due to different groups in your
organization using different terms for the same data. Or maybe your users just
intuitively use different words when searching for that item. Using synonyms
allows them to access the data even if the term they choose isn't the same as
the actual column name.

You can set column synonyms for columns in tables, user imported data, and
worksheets. The returned table or chart uses the _actual column name_,
but the search bar reflects the term the user typed in (the synonym).

To create a synonym for a column:

1. Find the column for which you want to add synonyms.
2. Select its **Synonyms**.
3. Enter a comma-separated list of the synonyms.

   If a synonym is more than one word, enclose it in double quotes. If
   you are using the Web interface, you would type:

    ```
    profit,"gross profit"
    ```

    If you are using the model file, the list of synonyms must be enclosed in
    square brackets:

    ```
    [profit, "gross profit"]
    ```

4. Save your changes.


## Related information  

[Model the data for searching]({{ site.baseurl }}/admin/data-modeling/about-data-modeling-intro.html)
