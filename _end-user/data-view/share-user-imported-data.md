---
title: [Share uploaded data]
last_updated: 11/04/2021
summary: When you upload data to ThoughtSpot, you can share it with others.
toc: false
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---
![Share data]({{ site.baseurl }}/images/sharing-data.gif "Share data")
<!--{% include image.html file="sharing-data.gif" title="Share data" alt="Learn how to share data." caption="Share data" %}-->

If you upload a spreadsheet, you can share **Can View** or **Can Edit**
privileges with other people, who can further share them with others.

## Understand data sharing

Data that you upload from a Web browser is only visible to you and to the
administrator. You can share the entire uploaded table, or only some of its
columns.

By default, if you share only some table columns, users with access to those columns cannot see the other columns' data in their searches. However, the data can become visible if a worksheet or Liveboard that _also contains_ those columns is shared with these users.

If you want to prevent other users from revealing your excluded columns,
you can ask your administrator to enable a stricter behavior.

You can share data [from the **Data** tab](#share-datatab), or [from within the table, worksheet, or view](#share-dataset) that you want to share.

{% include content/share-data.md %}
