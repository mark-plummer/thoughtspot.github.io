---
title: [Results that are tables]
last_updated: 3/13/2020
summary: "Tables display your answer in a format similar to an Excel spreadsheet."
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---
In the table view, your search identifies attributes and/or columns, and presents them as a table. ThoughtSpot aggregates the results based on the level of aggregation that you specify in the search. For example, if you only type `revenue`, you see the total sum of revenue as a single number. If you include the keyword `monthly`, the results are broken down by month. From the column header, you can rename the column, or sort or filter the column. You can rearrange the column order of your table by dragging and dropping the columns. You can also change the column widths.

## Rearrange column order

You can rearrange the column order of your table after adding all of your search terms.

To rearrange the column order:

1. While viewing your answer as a table, click the column header you would like to move.
2. Drag it across to its new position.

## Resize column widths

You can resize the column widths of your table after adding all of your search
terms. Any adjustments you make to the column widths of your table are saved
when you pin the table to a pinboard. To resize the column widths:

1. While viewing your answer as a table, hover over a column border in the column header row.
2. Click and drag the border to create your preferred column width.

{: id="clip-wrap-text"}
## Clip or wrap text
You can clip or wrap long text in a table cell, or on a table header.

When you clip long text, the table cells show only the beginning of the text. The rest appears if you increase the column width.

When you wrap long text, the table shows all the text in its cells by increasing the number of lines in the cells.

![Wrap or clip long text]({{ site.baseurl }}/images/chart-config-text.gif "Wrap or clip long text")

## Sort columns

You can sort a table by column values by clicking on the column title. If you
hold down the SHIFT key you can click multiple heads and sort on them in
turn.

{% include tip.html content="This same functionality is available on tables you
see elsewhere in ThoughtSpot. For example, a table in the **Data** page is also
sortable in this manner."%}

## About headlines (summary information)

Headlines display summary information of a table result. Headlines contain
summary information for each column of a table. They appear at the bottom of the
table in individual boxes.

 ![]({{ site.baseurl }}/images/chartconfig-headlines.png "Headlines at the bottom of a table")

ThoughtSpot automatically creates up to 10 headlines for each table. Your
ThoughtSpot configuration can be changed to accommodate more if needed. Headlines are not available for tables with more than 15000 rows, unless the data comes from an [Embrace connection]({{ site.baseurl }}/data-integrate/embrace/embrace-intro.html).

You can modify how you'd like the value to be displayed by clicking the dropdown
on a headline and selecting a different type of aggregation. The usual available
aggregations are total, average, standard deviation, variance, minimum, and
maximum. There are also unique count and total count values available for the
appropriate columns.

To add a headline to a pinboard, hover over the headline and click the **Pin** icon.

 ![Add a headline to a pinboard]({{ site.baseurl }}/images/pin_headline.png "Add a headline to a pinboard")

 You can decide whether or not to display headlines in your table results. To
 customize headlines, click the ellipsis icon ![]({{ site.baseurl }}/images/icon-more-10px.png){: .inline} and select **Customize Summaries**.

### Table aggregate headline

 The Table Aggregate headline option is available when an aggregate function is used either through a formula or a search bar query like average of a measure. It recalculates the function for the entire table. In such cases, Table Aggregate is shown by default in a headline under the table, instead of the “Avg” option, which does a second level of aggregation on top of the existing aggregation.

 In the following example, the table aggregate is shown as a result of the Average Profit formula `sum ( profit ) / count ( ship mode )` which divides the total profit of each ship mode by the sum total count for that ship mode. ThoughtSpot recalculates that function for the entire table, taking the sum total profits of all ship modes and dividing it by the sum total count of all ship modes. Here, that results in a table aggregate average profit of 28.7. The `average` headline option, by comparison, sums the average profit for all ship modes and divides it by the number of ship modes (4), providing a less accurate average.

![Table aggregate headline]({{ site.baseurl }}/images/table-aggregate.png "Table aggregate headline")
