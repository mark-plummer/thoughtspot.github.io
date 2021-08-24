---
title: [Understanding charts]
last_updated: 2/25/2020
summary: "Charts display your search answer in a visual way."
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---
Your search needs at least [one attribute and one measure](about-attributes-and-measures.html#) to be presented as a chart. When you choose to display your answer as a chart, ThoughtSpot will assign it the best fit chart type.

{% include note.html content="Colors are maintained across searches within a session. For example, when doing a search on revenue by state, each state will keep its color assigned to it even if you change the search or chart type." %}

You can choose from a large number of chart types in ThoughtSpot. Each chart type provides you with a different visualization for your answer.

You can also [adjust the axes, labels, and view of the chart]({{ site.baseurl }}/end-user/search/change-the-chart.html).

## About chart types

You can choose from a large number of chart types in ThoughtSpot. Each chart type provides you with a different visualization for your answer.

To change the chart type of your answer:

1. Click the **Change visualization** icon ![]({{ site.baseurl }}/images/icon-chart-type-10px.png){: .inline} to get a palette of chart types you can choose from (scroll down to see more.)

   ![Click 'change visualization' to choose a different chart type.]({{ site.baseurl }}/images/chartconfig-choosevisualization.png "Click 'change visualization' to choose a different chart type.")

2. Click a different chart or visualization type.

## Choosing a chart ##

**Note:** Some chart types may not be available, depending on the columns in your search. For example, if your search does not contain at least one geographical column, then you will not be able to select any of the geo chart types. ThoughtSpot shows unavailable chart types as grayed out.

Hovering over a chart type icon tell you what columns you require before you can use it.

-   **[Column charts]({{ site.baseurl }}/end-user/search/about-column-charts.html)**<br>
The column chart is one of ThoughtSpot's simplest, yet most versatile chart types. The column chart is often the chosen default chart type, and displays data as vertical columns.
-  **[Stacked columns]({{ site.baseurl }}/end-user/search/about-column-charts.html#stacked-columns)**<br>
The stacked column combines the different secondary dimensions into a single column, stacking them. Note that the dimensions retain their relative size and color.
-   **[Bar charts]({{ site.baseurl }}/end-user/search/about-bar-charts.html)**<br>
The bar chart is nearly identical to the column chart. The primary difference is that it displays data as horizontal bars.
-  **[Stacked bar charts]({{ site.baseurl }}/end-user/search/about-bar-charts.html#stacked-bar-charts)**<br>
Just like stacked columns, stacked bars combine the different secondary dimensions into a single stacked bar.
-   **[Line charts]({{ site.baseurl }}/end-user/search/about-line-charts.html)**<br>
Like the column chart, the line chart is one of ThoughtSpot's simplest, yet most versatile chart types. More often than not the line chart will be chosen as your default chart type.
-   **[Pie charts]({{ site.baseurl }}/end-user/search/pie-charts.html)**<br>
The pie chart is a classic chart type that displays your search in a circle. The pie chart ThoughtSpot shows is in the shape of a doughnut.
-   **[Area charts]({{ site.baseurl }}/end-user/search/area-charts.html)**<br>
The area chart is based on the line chart, but has filled in regions.
-   **[Stacked area charts]({{ site.baseurl }}/end-user/search/area-charts.html#stacked-area-charts)**<br>
This option stacks the values of one dimension on top of the other, enabling you to clearly see the relative volume of data under the line. Contrast this with the presentation in the area chart, where data for different overlaps.
-   **[Scatter charts]({{ site.baseurl }}/end-user/search/about-scatter-charts.html)**<br>
The scatter chart is useful for finding correlations or outliers in your data.
-   **[Bubble charts]({{ site.baseurl }}/end-user/search/about-bubble-charts.html)**<br>
The bubble chart displays three dimensions of data with each containing a set of values.
-   **[Pareto charts]({{ site.baseurl }}/end-user/search/about-pareto-charts.html)**<br>
The pareto chart is a type of chart that contains both columns and a special type of line chart.
-   **[Waterfall charts]({{ site.baseurl }}/end-user/search/about-waterfall-charts.html)**<br>
The waterfall chart is used to show how an initial value is affected by a series of intermediate positive or negative values.
-   **[Treemap charts]({{ site.baseurl }}/end-user/search/about-treemap-charts.html)**<br>
The treemap chart displays hierarchical data as a set of nested rectangles.
-   **[Heatmap charts]({{ site.baseurl }}/end-user/search/heatmap-chart.html)**<br>
The heatmap chart displays individual data values in a matrix following a color scale.
-   **[Line column charts]({{ site.baseurl }}/end-user/search/line-column-charts.html)**<br>
The line column chart combines the column and line charts.
-   **[Funnel charts]({{ site.baseurl }}/end-user/search/about-funnel-charts.html)**<br>
The funnel chart shows a process with progressively decreasing proportions amounting to 100 percent in total.
-   **[Geo charts]({{ site.baseurl }}/end-user/search/about-geo-charts.html)**<br>
There are three geo charts that let you visualize geographical data in ThoughtSpot: Area, Bubble, and Heatmap.
-   **[Pivot tables]({{ site.baseurl }}/complex-search/about-pivoting-a-table.html)**<br>
Pivot tables in ThoughtSpot use the well known drag-and-drop interface. Creating a pivot table enables exploring alternate visualization of data in a wide table. The basic idea is that some data is easier to consume when laid out horizontally, while others, vertically.
-   **[Sankey charts]({{ site.baseurl }}/end-user/search/about-sankey-charts.html)**<br>
Sankey charts show a flow from one set of values to another, usually with visual emphasis (brighter colors or larger bandwidths) for comparison of the values (e.g., top cities in terms of sales might be emphasized).
-   **[Radar charts]({{ site.baseurl }}/end-user/search/about-radar-charts.html)**<br>
Radar charts display multivariate data on a two-dimensional chart of three or more quantitative variables that plot on axes (spokes) that originate at the same point.
-   **[Candlestick charts]({{ site.baseurl }}/end-user/search/candlestick-charts.html)**<br>
Candlestick charts efficiently collapse financial information, such as price movements on a single day, into a unified representation. A single 'candlestick' shows the _open_, _high_, _low_, and _close_ prices for the same day.

## Charts with multiple measures on the y-axis

You can have multiple measures on the y-axis of many charts, which is a great additional way of presenting information in a chart. A stacked column chart displays the measures stacked in the same column, while a column chart displays the measures side by side.

![Stacked column chart example: multiple measures on the y axis]({{ site.baseurl }}/images/chartconfig-multiplemeasures.png "Stacked column chart example: multiple measures on the y axis")

The following charts support multiple measures on the y-axis:
* Column
* Stacked Column
* Bar
* Stacked Bar
* Line
* Area
* Stacked Area
* Waterfall
* Line Column
* Line Stacked Column

To learn more, see [Configure columns for the x and y axes]({{ site.baseurl }}/end-user/search/drag-and-drop.html).
