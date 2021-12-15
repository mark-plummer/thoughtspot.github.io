---
title: [Add a Starburst connection]
last_updated: 9/21/2020
toc: true
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---
To connect to Starburst, follow these steps:

1. Click **Data** in the top navigation bar.

2. Click the **Connections** tab at the top of the page, and click **+ Add connection** at the upper-right-hand side of the page.

   <!--![Click "+ Add connection"]({{ site.baseurl }}/images/redshift-addconnection.png "Click "+ add connection"") -->
   <!--![]({{ site.baseurl }}/images/new-connection.png "New db connect") -->

3. Create a name for your connection, a description (optional), then select the Starburst connection type, and click **Continue**.

   ![Add a Starburst connection]({{ site.baseurl }}/images/starburst-connectiontype.png "Add a Starburst connection")

4. Enter the connection details for your Starburst data source.

   ![Enter connection details]({{ site.baseurl }}/images/starburst-connectiondetails.png "Enter connection details")

   Refer to the [Starburst connection reference]({{ site.baseurl }}/data-integrate/embrace/embrace-starburst-reference.html#) for more information on each of the specific attributes you must enter for your connection.

5. (Optional) Provide additional key-value pairs that you need to set up your connection to Starburst, by doing the following:
    1. Click the **Advanced Config** menu to reveal the **Key** and **Value** fields.
    2. Enter your key and value information.
    3. To add more keys and values, click the plus sign (+), and enter them.

    {% include note.html content="Any key-value pairs that you enter must be defined in your Starburst data source. Key-value pairs are case-sensitive." %}

6. Click **Continue**.      

7. Select tables (on the left) and the columns from each table (on the right), and then click **Create connection**.

    ![Select tables and columns for your connection]({{ site.baseurl }}/images/snowflake-selecttables.png "Select tables and columns for your connection")
   <!--![Select tables and columns for your connection]({{ site.baseurl }}/images/Trino-selecttables.png "Select tables and columns for your connection") -->

    A message appears indicating the number of tables and columns that will be added to your connection.

8. Click **Confirm**.   

    Once the connection is added, you can search your Starburst database right away by clicking **Search now**.

    ![The "Connection created" screen]({{ site.baseurl }}/images/starburst-connectioncreated.png "The "Connection created" screen")

    Your new connection appears on the **Data** > **Connections** page. You can click the name of your connection to view the tables and columns in your connection.   

The connection you just created is a link to the external data source. If there are any joins in the selected tables of the external data source, those are imported into ThoughtSpot.

You can now perform a live query on the selected tables and columns of your connection. Because the selected tables and columns in your connection are linked, it may take a while to initially render the search results. This is because ThoughtSpot does not cache linked data. With linked data, ThoughtSpot queries the external database directly, which is slower than querying data that is stored in ThoughtSpot's database.

You can modify a Snowflake connection in the following ways:

- [Edit a Starburst connection]({{ site.baseurl }}/admin/ts-cloud/ts-cloud-embrace-starburst-edit-connection.html)
- [Remap a Starburst connection]({{ site.baseurl }}/admin/ts-cloud/ts-cloud-embrace-starburst-remap-connection.html)
- [Delete a table from a Starburst connection]({{ site.baseurl }}/admin/ts-cloud/ts-cloud-embrace-starburst-delete-table.html)
- [Delete a table with dependent objects]({{ site.baseurl }}/admin/ts-cloud/ts-cloud-embrace-starburst-delete-table-dependencies.html)

You can also [Delete a Starburst connection]({{ site.baseurl }}/admin/ts-cloud/ts-cloud-embrace-trino-delete-connection.html).

See the [Connection reference]({{ site.baseurl }}/admin/ts-cloud/ts-cloud-embrace-trino-connection-reference.html) for details of connection parameters.
