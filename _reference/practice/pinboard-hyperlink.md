---
title: [Add a hyperlink to a Search]
last_updated: 10/11/2021
summary: “Learn how to add a hyperlink to a search.”
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---

You can add a hyperlink directly within a Search. Using the concat formula, you can create an external hyperlink, or link your Answer to another Pinboard. 

## How to add a basic hyperlink

To add an external hyperlink in a search, follow these steps:

1. Start a new Search.<br/>
Alternatively, choose to edit an existing Answer from a Pinboard.

2. If the Answer shows a chart, switch to **Table View**.
![Switch to table view]({{ site.baseurl }}/images/changeview-chartortable.png "Switch to table view"){: .inline}

3. In the upper-right side of the table, click the **More** menu icon ![more options menu icon]({{ site.baseurl }}/images/icon-ellipses.png){: .inline}, and select **Add formula**.<br/>

![Create a new formula in an answer]({{ site.baseurl }}/images/formula-add-to-search.png "Create a new formula in an answer"){: .inline}

4. Name your formula.
5. Enter your formula, following the basic syntax: <br/>
```
concat({caption}value{/caption}link)
```
  1. For a data set that does not contain properly formed urls, your formula should include the url in full. <br/>
  For example, to link from the Product Category column to a Google search, use the following syntax to reference the `product category` column, and a Google search using its values: <br/>
  ```
  concat("{caption}",product category ,"{/caption}","https://www.google.com/search?q=",product category)
  ```
  2. For a data set that contains properly formed urls, you can simplify the formula. <br/>
  For example, to link from the `Fruit` column to the `url`, use the following syntax to reference the two columns, `fruit` and `url`: <br/>
  ```
  concat("{caption}",fruit,"{/caption}",url)
  ```
6. Click **Save**.

## How to link to another Pinboard

To add a hyperlink to another Pinboard, follow these steps:

1. Start a new Search.<br/>
Alternatively, choose to edit an existing Answer from a Pinboard.

2. Choose the target Pinboard for the link.

3. Open your target Pinboard and copy the web address.

4. Within your Search, switch to **Table View**.

5. In the upper-right side of the table, click the **More** menu icon ![more options menu icon]({{ site.baseurl }}/images/icon-ellipses.png){: .inline}  and select **Add formula**.<br/>

![Create a new formula in an answer]({{ site.baseurl }}/images/formula-add-to-search.png "Create a new formula in an answer")

6. Name your formula.

7. Enter your formula, following the basic syntax:<br/>
```
concat(“{caption}pinboard{/caption}http://<thoughtspot_server>:<port>/?<runtime filter>,column name)
```
For example, the formula to link between a search on fruit sales and a Pinboard based on the same data with url <code>https://<thoughtspot-instance>.com/#/pinboard/e510f946-f9ce-48ad-a4af-1a40a9cf8add</code> would be:
<code>concat("{caption}pinboard{/caption}https://<thoughtspot-instance>.com/#/pinboard/e510f946-f9ce-48ad-a4af-1a40a9cf8add/?col1=fruit&op1=eq&val1=",fruit)</code> <br/>

Here, the runtime filter is operating on the column “fruit,” and will only return values that are equal (EQ) to the fruits listed in the columns. To learn more about runtime filters, see [About Runtime Filters]({{site.baseurl }}/app-integrate/runtime-filters/about-runtime-filters.html).

8. Click **Save**.
