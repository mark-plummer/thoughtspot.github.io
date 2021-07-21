---
title: [Data modeling]
last_updated: 07/21/2021
summary: "Modeling, tagging, and adding links between your data sources can make the data even easier to search."
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---
Data modeling allows you to define metadata and other aspects of your data.  For
example, you can give data columns search friendly names or predefine how they
can be explored and aggregated. Metadata include such information as **Column
Names**, **Column Visibility**, **Column** and **Data Definition**, **Column
Rank** and so forth.

When you load data, most of this data modeling metadata is set up for you automatically. However, since you know your data best, you can adjust the modeling settings to improve the experience for your users. After
loading data, you can start searching your data without doing any data modeling,
creating relationships, or tagging. However, since you know your data best, you
can customize the modeling settings. Putting some thought into these will make
the data even easier and more intuitive to search for your end users.


## User interfaces for modeling data

Data modeling is a very lightweight process compared to what you may have
experienced in other tools. It enables you to change some of the settings (or properties) of the data so that it becomes more searchable. You can configure the model [for an individual data table]({{ site.baseurl }}/admin/data-modeling/model-data-in-UI.html) or you can view and configure all the system data [using a modeling file]({{ site.baseurl }}/admin/data-modeling/edit-model-file.html).
Editing the data model file requires that you have administrative privileges.

The model file contains a row for each column in your data set. It isn't unusual
to have tens of thousand of rows in this file. This means that editing this file is
equivalent to editing all the tables simultaneously. When you add new data to your
system, this file expands to accommodate the new data columns you have added.

Both of these methods have the same effect: they improve search. Moreover,
while they have different effects of scale, they use the same mechanisms to
accomplish these effects.

## Modeling topics

The following topics explain how to model your data:

- **[Change a table's data model]({{ site.baseurl }}/admin/data-modeling/model-data-in-UI.html)**  
Explains how to make modeling settings for a table you've just loaded, or to make a quick change to existing settings.
- **[Edit the system-wide data model]({{ site.baseurl }}/admin/data-modeling/edit-model-file.html)**  
Explains how to define a default data model to use for data system-wide.
- **[Data modeling settings]({{ site.baseurl }}/admin/data-modeling/data-modeling-settings.html)**  
Explains the possible data model settings and their accepted values. These are the same for a table or the system.
- **[Link tables using relationships]({{ site.baseurl }}/admin/data-modeling/about-relationships.html)**  
Linked tables can be searched together or combined into a worksheet for easy searching. Tables that have no relationship between their columns can not be combined in a single search.
- **[About tags]({{ site.baseurl }}/admin/data-modeling/tags.html)**  
 You can create tags to make it easier for people to find data sources and pinboards.
- **[Manage experts or add an expert to your data]({{ site.baseurl }}/admin/data-modeling/add-expert.html)**
