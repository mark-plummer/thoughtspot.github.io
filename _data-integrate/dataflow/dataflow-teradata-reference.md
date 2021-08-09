---
title: [Teradata connection reference]
summary: Learn about the fields used to create a Teradata connection with ThoughtSpot DataFlow.
last_updated: 07/7/2020
redirect_from:
- /7.0.0.mar.sw/data-integrate/dataflow/dataflow-teradata-reference.html
- /7.0.1.jun.sw/data-integrate/dataflow/dataflow-teradata-reference.html
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---

Here is a list of the fields for a Teradata connection in ThoughtSpot DataFlow. You need specific information to establish a seamless and secure connection.

## Connection properties

<dl id="dataflow-teradata-connection-properties">
<dlentry id="dataflow-teradata-conn-connection-properties"><dt>Connection Properties</dt><dd id="connection-properties-description">Name your connection.</dd><dd id="connection-properties-required">Mandatory field.</dd><dd id="connection-properties-example"><strong>Example:</strong><br/>TeradataConnection</dd></dlentry>
<dlentry id="dataflow-teradata-conn-connection-type"><dt>Connection type</dt><dd id="connection-type-description">Choose the Teradata connection type.</dd><dd id="connection-type-required">Mandatory field.</dd><dd id="connection-type-example"><strong>Example:</strong><br/>Teradata</dd></dlentry>
<dlentry id="dataflow-teradata-conn-host"><dt>Host</dt><dd id="host-description">Specify the hostname or the IP address of the Teradata system</dd><dd id="host-required">Mandatory field.</dd><dd id="host-example"><strong>Example:</strong><br/>www.example.com</dd></dlentry>
<dlentry id="dataflow-teradata-conn-port"><dt>Port</dt><dd id="port-description">Specify the port associated to the Teradata system</dd><dd id="port-required">Mandatory field.</dd><dd id="port-example"><strong>Example:</strong><br/>1234</dd></dlentry>
<dlentry id="dataflow-teradata-conn-user"><dt>User</dt><dd id="user-description">Specify the user id that will be used to connect to the Teradata system. This user should have necessary privileges to access the data in the databases.</dd><dd id="user-required">Mandatory field.</dd><dd id="user-example"><strong>Example:</strong><br/>userdi</dd></dlentry>
<dlentry id="dataflow-teradata-conn-password"><dt>Password</dt><dd id="password-description">Specify the password for the User</dd><dd id="password-required">Mandatory field.</dd><dd id="password-example"><strong>Example:</strong><br/>pswrd234%!</dd></dlentry>
<dlentry id="dataflow-teradata-conn-version"><dt>Version</dt><dd id="version-description">Specify the version of Teradata you are using</dd><dd id="version-required">Optional field.</dd><dd id="version-example"><strong>Example:</strong><br/>14.2</dd><dd id="version-other"><strong>Other notes:</strong><br/>Advanced configuration</dd></dlentry>
<dlentry id="dataflow-teradata-conn-jdbc-options"><dt>JDBC options</dt><dd id="jdbc-options-description">Specify the options associated with the JDBC URL.</dd><dd id="jdbc-options-required">Optional field.</dd><dd id="jdbc-options-example"><strong>Example:</strong><br/><code>jdbc:sqlserver://[serverName[\instanceName][:portNumber]]</code></dd><dd id="jdbc-options-other"><strong>Other notes:</strong><br/>Advanced configuration</dd></dlentry>
</dl>

## Sync properties

<dl id="dataflow-teradata-sync-properties">
<dlentry id="dataflow-teradata-sync-data-extraction-mode"><dt>Data extraction mode</dt><dd id="data-extraction-mode-description">Specify the extraction type.</dd><dd id="data-extraction-mode-required">Mandatory field.</dd><dd id="data-extraction-mode-example"><strong>Example:</strong><br/>JDBC</dd><dd id="data-extraction-mode-valid-values"><strong>Valid Values:</strong><br/>JDBC, TPT</dd><dd id="data-extraction-mode-default"><strong>Default:</strong><br/>JDBC</dd></dlentry>
<dlentry id="dataflow-teradata-sync-column-delimiter"><dt>Column delimiter</dt><dd id="column-delimiter-description">Specify the column delimiter character.</dd><dd id="column-delimiter-required">Mandatory field.</dd><dd id="column-delimiter-example"><strong>Example:</strong><br/>1</dd><dd id="column-delimiter-valid-values"><strong>Valid Values:</strong><br/>Any printable ASCII character or decimal value for ASCII character</dd><dd id="column-delimiter-default"><strong>Default:</strong><br/>1</dd></dlentry>
<dlentry id="dataflow-teradata-sync-null-value"><dt>Null value</dt><dd id="null-value-description">Specifies the string literal that indicates the null value in the extracted data. During the data load, the column value matching this string loads as null in the target.</dd><dd id="null-value-required">Optional field.</dd><dd id="null-value-example"><strong>Example:</strong><br/>NULL</dd><dd id="null-value-valid-values"><strong>Valid Values:</strong><br/>Any string literal</dd><dd id="null-value-default"><strong>Default:</strong><br/>NULL</dd></dlentry>
<dlentry id="dataflow-teradata-sync-enclosing-character"><dt>Enclosing character</dt><dd id="enclosing-character-description">Specify if the text columns in the source data needs to be enclosed in quotes.</dd><dd id="enclosing-character-required">Optional field.</dd><dd id="enclosing-character-example"><strong>Example:</strong><br/>DOUBLE</dd><dd id="enclosing-character-valid-values"><strong>Valid Values:</strong><br/>SINGLE, DOUBLE</dd><dd id="enclosing-character-default"><strong>Default:</strong><br/>DOUBLE</dd><dd id="enclosing-character-other"><strong>Other notes:</strong><br/>This is required if the text data has newline character or delimiter character.</dd></dlentry>
<dlentry id="dataflow-teradata-sync-escape-character"><dt>Escape character</dt><dd id="escape-character-description">Specify the escape character if using a text qualifier in the source data.</dd><dd id="escape-character-required">Optional field.</dd><dd id="escape-character-example"><strong>Example:</strong><br/>\"</dd><dd id="escape-character-valid-values"><strong>Valid Values:</strong><br/>Any ASCII character</dd><dd id="escape-character-default"><strong>Default:</strong><br/>\"</dd></dlentry>
<dlentry id="dataflow-teradata-sync-fetch-size"><dt>Fetch size</dt><dd id="fetch-size-description">Specify the number of rows at a time to fetch and process in memory. If you specify zero, the system extracts all rows at once.</dd><dd id="fetch-size-required">Mandatory field.</dd><dd id="fetch-size-example"><strong>Example:</strong><br/>1000</dd><dd id="fetch-size-valid-values"><strong>Valid Values:</strong><br/>Any numeric value</dd><dd id="fetch-size-default"><strong>Default:</strong><br/>1000</dd></dlentry>
<dlentry id="dataflow-teradata-sync-ts-load-options"><dt>TS load options</dt><dd id="ts-load-options-description">Specifies the parameters passed with the <code>tsload</code> command, in addition to the commands already included by the application. The format for these parameters is:<br/><code> --&lt;param_1_name&gt; &lt;optional_param_1_value&gt;</code><br/><code> --&lt;param_2_name&gt; &lt;optional_param_2_value&gt;</code></dd><dd id="ts-load-options-required">Optional field.</dd><dd id="ts-load-options-example"><strong>Example:</strong><br/>--max_ignored_rows 0</dd><dd id="ts-load-options-valid-values"><strong>Valid Values:</strong><br/>--user "dbuser" --password "$DIWD" --target_database "ditest" --target_schema "falcon_schema"</dd><dd id="ts-load-options-default"><strong>Default:</strong><br/>--max_ignored_rows 0</dd><dd id="reference"><strong>Reference:</strong><br/><a href="{{ site.baseurl }}/reference/data-importer-ref.html">tsload flag reference</a></dd></dlentry></dl>

## Related Information

[Dataflow tips]({{ site.baseurl }}/data-integrate/data-flow-tips.html)
