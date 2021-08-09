---
title: [Splice Machine connection reference]
summary: Learn about the fields used to create a Splice Machine connection with ThoughtSpot DataFlow.
last_updated: 07/7/2020
redirect_from:
- /7.0.0.mar.sw/data-integrate/dataflow/dataflow-splice-machine-reference.html
- /7.0.1.jun.sw/data-integrate/dataflow/dataflow-splice-machine-reference.html
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---

Here is a list of the fields for a Splice Machine connection in ThoughtSpot DataFlow. You need specific information to establish a seamless and secure connection.

## Connection properties

<dl id="dataflow-splice-machine-connection-properties">
<dlentry id="dataflow-splice-machine-conn-connection-name"><dt>Connection name</dt><dd id="connection-name-description">Name your connection.</dd><dd id="connection-name-required">Mandatory field.</dd><dd id="connection-name-example"><strong>Example:</strong><br/>SpliceMachineConnection</dd></dlentry>
<dlentry id="dataflow-splice-machine-conn-connection-type"><dt>Connection type</dt><dd id="connection-type-description">Choose the Splice Machine connection type.</dd><dd id="connection-type-required">Mandatory field.</dd><dd id="connection-type-example"><strong>Example:</strong><br/>Splice Machine</dd></dlentry>
<dlentry id="dataflow-splice-machine-conn-host"><dt>Host</dt><dd id="host-description">Specify the hostname or the IP address of the Splice Machine system</dd><dd id="host-required">Mandatory field.</dd><dd id="host-example"><strong>Example:</strong><br/>www.example.com</dd></dlentry>
<dlentry id="dataflow-splice-machine-conn-port"><dt>Port</dt><dd id="port-description">Specify the port associated with the Splice Machine system</dd><dd id="port-required">Mandatory field.</dd><dd id="port-example"><strong>Example:</strong><br/>1234</dd></dlentry>
<dlentry id="dataflow-splice-machine-conn-user"><dt>User</dt><dd id="user-description">Specify the user id that will be used to connect to the Splice Machine system. This user should have necessary privileges to access the data in the databases.</dd><dd id="user-required">Mandatory field.</dd><dd id="user-example"><strong>Example:</strong><br/>userdi</dd></dlentry>
<dlentry id="dataflow-splice-machine-conn-password"><dt>Password</dt><dd id="password-description">Specify the password for the User</dd><dd id="password-required">Mandatory field.</dd><dd id="password-example"><strong>Example:</strong><br/>pswrd234%!</dd></dlentry>
<dlentry id="dataflow-splice-machine-conn-database"><dt>Database</dt><dd id="database-description">Collection of information that is organized so that it can be easily accessed, managed and updated.</dd><dd id="database-required">Mandatory field.</dd><dd id="database-example"><strong>Example:</strong><br/>splicedb</dd></dlentry>
<dlentry id="dataflow-splice-machine-conn-hadoop-version"><dt>Hadoop version</dt><dd id="hadoop-version-description">Specify the version of Hadoop you are using</dd><dd id="hadoop-version-required">Mandatory field.</dd><dd id="hadoop-version-example"><strong>Example:</strong><br/>HDP_2.6.4</dd></dlentry>
<dlentry id="dataflow-splice-machine-sync-hdfs-host"><dt>HDFS host</dt><dd id="hdfs-host-description">Specify the hostname or the IP address of the HDFS</dd><dd id="hdfs-host-required">Optional field.</dd><dd id="hdfs-host-example"><strong>Example:</strong><br/>www.example.com</dd><dd id="hdfs-host-other"><strong>Other notes:</strong><br/>Advanced configuration</dd></dlentry>
<dlentry id="dataflow-splice-machine-sync-hdfs-port"><dt>HDFS port</dt><dd id="hdfs-port-description">Specify the port associated to the HDFS</dd><dd id="hdfs-port-required">Optional field.</dd><dd id="hdfs-port-example"><strong>Example:</strong><br/>1235</dd><dd id="hdfs-port-other"><strong>Other notes:</strong><br/>Advanced configuration</dd></dlentry>
<dlentry id="dataflow-splice-machine-sync-hdfs-temp-location"><dt>HDFS temp location</dt><dd id="hdfs-temp-location-description">Specify the HDFS location for creating temp directory</dd><dd id="hdfs-temp-location-required">Optional field.</dd><dd id="hdfs-temp-location-example"><strong>Example:</strong><br/>/user/splice/tmp</dd><dd id="hdfs-temp-location-other"><strong>Other notes:</strong><br/>Advanced configuration</dd></dlentry>
<dlentry id="dataflow-splice-machine-conn-jdbc-options"><dt>JDBC options</dt><dd id="jdbc-options-description">Specify the options associated with the JDBC URL.</dd><dd id="jdbc-options-required">Optional field.</dd><dd id="jdbc-options-example"><strong>Example:</strong><br/><code>jdbc:sqlserver://[serverName[\instanceName][:portNumber]]</code></dd><dd id="jdbc-options-other"><strong>Other notes:</strong><br/>Advanced configuration</dd></dlentry>

</dl>

## Sync properties

<dl id="dataflow-splice-machine-sync-properties">
<dlentry id="dataflow-splice-machine-sync-data-extraction-mode"><dt>Data extraction mode</dt><dd id="data-extraction-mode-description">Specify the extraction type.</dd><dd id="data-extraction-mode-required">Mandatory field.</dd><dd id="data-extraction-mode-example"><strong>Example:</strong><br/>JDBC</dd><dd id="data-extraction-mode-valid-values"><strong>Valid Values:</strong><br/>JDBC, BULK Export</dd><dd id="data-extraction-mode-default"><strong>Default:</strong><br/>JDBC</dd></dlentry>
<dlentry id="dataflow-splice-machine-sync-column-delimiter"><dt>Column delimiter</dt><dd id="column-delimiter-description">Specify the column delimiter character.</dd><dd id="column-delimiter-required">Mandatory field.</dd><dd id="column-delimiter-example"><strong>Example:</strong><br/>1</dd><dd id="column-delimiter-valid-values"><strong>Valid Values:</strong><br/>Any printable ASCII character or decimal value for ASCII character</dd><dd id="column-delimiter-default"><strong>Default:</strong><br/>1</dd></dlentry>
<dlentry id="dataflow-splice-machine-sync-enclosing-character"><dt>Enclosing character</dt><dd id="enclosing-character-description">Specify if the text columns in the source data needs to be enclosed in quotes.</dd><dd id="enclosing-character-required">Optional field.</dd><dd id="enclosing-character-example"><strong>Example:</strong><br/>DOUBLE</dd><dd id="enclosing-character-valid-values"><strong>Valid Values:</strong><br/>SINGLE, DOUBLE</dd><dd id="enclosing-character-default"><strong>Default:</strong><br/>DOUBLE</dd><dd id="enclosing-character-other"><strong>Other notes:</strong><br/>This is required if the text data has newline character or delimiter character.</dd></dlentry>
<dlentry id="dataflow-splice-machine-sync-escape-character"><dt>Escape character</dt><dd id="escape-character-description">Specify the escape character if using a text qualifier in the source data.</dd><dd id="escape-character-required">Optional field.</dd><dd id="escape-character-example"><strong>Example:</strong><br/>\"</dd><dd id="escape-character-valid-values"><strong>Valid Values:</strong><br/>Any ASCII character</dd><dd id="escape-character-default"><strong>Default:</strong><br/>\"</dd></dlentry>
<dlentry id="dataflow-splice-machine-sync-fetch-size"><dt>Fetch size</dt><dd id="fetch-size-description">Specify the number of rows at a time to fetch and process in memory. If you specify zero, the system extracts all rows at once.</dd><dd id="fetch-size-required">Mandatory field.</dd><dd id="fetch-size-example"><strong>Example:</strong><br/>1000</dd><dd id="fetch-size-valid-values"><strong>Valid Values:</strong><br/>Any numeric value</dd><dd id="fetch-size-default"><strong>Default:</strong><br/>1000</dd></dlentry>
<dlentry id="dataflow-splice-machine-sync-ts-load-options"><dt>TS load options</dt><dd id="ts-load-options-description">Specifies the parameters passed with the <code>tsload</code> command, in addition to the commands already included by the application. The format for these parameters is:<br/><code> --&lt;param_1_name&gt; &lt;optional_param_1_value&gt;</code><br/><code> --&lt;param_2_name&gt; &lt;optional_param_2_value&gt;</code></dd><dd id="ts-load-options-required">Optional field.</dd><dd id="ts-load-options-example"><strong>Example:</strong><br/>--max_ignored_rows 0</dd><dd id="ts-load-options-valid-values"><strong>Valid Values:</strong><br/>--user "dbuser" --password "$DIWD" --target_database "ditest" --target_schema "falcon_schema"</dd><dd id="ts-load-options-default"><strong>Default:</strong><br/>--max_ignored_rows 0</dd><dd id="reference"><strong>Reference:</strong><br/><a href="{{ site.baseurl }}/reference/data-importer-ref.html">tsload flag reference</a></dd></dlentry></dl>

## Related Information

[Dataflow tips]({{ site.baseurl }}/data-integrate/data-flow-tips.html)
