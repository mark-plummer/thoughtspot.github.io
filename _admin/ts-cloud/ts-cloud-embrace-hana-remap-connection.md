---
title: [Remap an SAP HANA connection]
last_updated: 8/11/2020
toc: true
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---

Modify the connection parameters by editing the source mapping <code>yaml</code> file that was created when you added the connection. For example, you can remap the existing table or column to a different table or column in an existing database connection. ThoughtSpot recommends that you check the dependencies before and after you remap a table or column in a connection to ensure they display as intended.

To remap an SAP HANA connection:

1. Click **Data** in the top navigation bar.

2. Click the **Embrace** tab.

3. Click the name of the connection you want to remap.

4. Click the More icon ![more options menu icon]({{ site.baseurl }}/images/icon-ellipses.png){: .inline} and select **Remapping** on the upper-right-hand side of the page.
   ![Remap a connection]({{ site.baseurl }}/images/HANA-remapping.png "Remap a connection")

5. Click **Download** to download the source mapping file.

   !["Download the source mapping file"]({{ site.baseurl }}/images/HANA-downloadyaml.png "Download the source mapping file")

6. Edit the file, as required, and save it.
<!--   ![Edit the yaml file]({{ site.baseurl }}/images/HANA-yaml.png "Edit the yaml file") -->

7. On the Remapping page, click **Browse your files**, and upload your edited mapping file to update the mapping of your connection.

To remove a table from a connection, delete it from the connection details page. For more information, see: [Delete an SAP HANA connection]({{ site.baseurl }}/admin/ts-cloud/ts-cloud-embrace-hana-delete-connection.html).

See the [Connection reference]({{ site.baseurl }}/admin/ts-cloud/ts-cloud-embrace-hana-connection-reference.html) for details of connection parameters.
