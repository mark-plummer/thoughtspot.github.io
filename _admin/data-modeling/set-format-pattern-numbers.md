---
title: [ "Set number, date, and currency formats" ]
last_updated: 07/07/2021
summary: "Learn how to set key formats for column values."
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---
You can set number, date, and currency display formats. These formats define how
these value types display in tables and charts.

{% include note.html content="ThoughtSpot supports number, currency, and percent formatting, at the data source level and at the answer level. The <code>format pattern</code> option combines number and percent formatting. You can override data source (“custom” in the UI) formatting at the answer level. In source level/ custom formatting, you can only define the format pattern (number and percent formatting) or currency option. If you set them both, the format pattern overrides your currency formatting." %}

## Number formats

You can set a format for how numbers are displayed in tables and charts. For
example, you can display numbers with a different number of digits after the
decimal point, based on the data modeling setting **Format Pattern**. You can
use any of the supported number formats for delimiters and number of digits to
show using [Java Decimal
Notation](http://docs.oracle.com/javase/7/docs/api/java/text/DecimalFormat.html).
Currency symbols are not supported.

The system has default values which are:

| `#,###` | For integer data types `INT` and `BIGINT`. As you can see, these can only contain numbers, alpha characters are not permitted. |
| `#,###.00` | for decimal data types `DOUBLE` and `FLOAT`. |

These are some examples of formats you can use:

|Stored Value|Format Pattern|Display Value|
|------------|--------------|-------------|
|12345.6789|`#,##0.##`|12,345.68|
|12345.6789|`#,##0.###`|12,345.679|
|12345.6789|`#,##0.00000`|12,345.67890|
|12345.6789|`#,##0`|12,346|
|12345.6789|`#,##0.00`|12,345.68|
|12345|`#,##0.##`|12,345|
|12345|`#,##0.00`|12,345.00|

### Profile-based number formatting

Number formatting is set by default based on your ThoughtSpot profile's
**Preferred locale** setting. You can set this value to accommodate your
geographic locations.

![]({{ site.baseurl }}/images/profile-locale.png "Specify Profile locale")


For example, if you are using ThoughtSpot in the US, the number formatting
should look like this: `xxx,xxx.xx`. And in Europe, it should look like this:
`xxx.xxx,xx`.

## Date formats

The **Format Pattern** option in the UI or in the model file allows you to specify how ThoughtSpot should display dates in tables and charts. For example, you can display dates in a standard European or US format based on the data modeling setting **Format Pattern**.
These are some examples of formats you can use:

{% include content/data-modeling-strings.md %}

You can change the date format used to display a column's values [for a single
table or Worksheet]({{ site.baseurl }}/admin/data-modeling/model-data-in-UI.html) or, by
editing the data model, for [the entire ThoughtSpot instance]({{ site.baseurl
}}/admin/data-modeling/edit-model-file.html). To edit the data model file, you must have administrative privileges. To change the date format, follow these steps:

1. Decide if the change is for a specific table or Worksheet, or for the entire instance.

2. Find the **Format Pattern** for the column.

   This is either a column in a single table or Worksheet or a column in the data modeling file.

3. In the column, enter the format you want to use.

4. Save your changes.

   If you are using a data-modeling file you must upload the new file to your installation.

{% include note.html content="You can see this custom date formatting when you use the <code>date detailed</code> keyword. Other date buckets, such as <code>monthly</code> or <code>weekly</code>, use the standard format. For daily dates, ThoughtSpot uses each user's locale to determine whether to display <code>mm/dd/yyyy</code> or <code>dd/mm/yyyy</code>." %}

## Set currency type

You can set a format for how currencies display in tables and charts when
using the ThoughtSpot Data API or embedding. For example, you can display
currencies in a standard European Euro or US Dollar format, based on the data
modeling setting **Currency Type**.

You can change the currency format used to display a column's values [for a
single table]({{ site.baseurl }}/admin/data-modeling/model-data-in-UI.html).
When you specify the currency type of your data in the **Columns** settings, your
currency data will only display the correct format and currency code in the
embedded use case. Currency specific symbols are available in the non-embedded
use case as well, but they are not localized.

All users are treated as if they are in `en-US` locale unless they are in embed
mode and their browser configuration tells ThoughtSpot that they are in some
other locale. For example, `100 Polish Zloty` appears as `100zł` to a user in
Poland, but without localization enabled, it appears as `PLN 100`.

This subtle difference can be seen when you use the REST API. See the
ThoughtSpot Application Integration Guide for more information on the API.

1. Find the **Currency Type** for the column whose display format you want to change.

2. Click it to open the **Specify Currency Type** menu.

     ![]({{ site.baseurl }}/images/specify_currency_type.png "Specify Currency Type")

3. Select one of the following ways you would like to change the format.

    | Option                  | Description |
    | ------------------------|----------|
    | **Infer From Browser** | Your currency data will be modeled upon the locale of your browser setting. |
    | **From a column** | Your currency data will be modeled upon the existing currency information in the selected column. This option is disabled if there is no `VARCHAR` column to choose from.
    | **Specify ISO Code** | Your currency data will be modeled upon your selection from the available currency code choices. |

4. Click **Ok** to save your changes.


## Related information  

[Model the data for searching]({{ site.baseurl }}/admin/data-modeling/about-data-modeling-intro.html)
