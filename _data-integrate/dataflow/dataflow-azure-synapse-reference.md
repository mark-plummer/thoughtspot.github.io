---
title: [Azure Synapse connection reference]
summary: Learn about the fields used to create an Azure Synapse connection with ThoughtSpot DataFlow.
last_updated: 06/19/2020
redirect_from:
- /7.0.0.mar.sw/data-integrate/dataflow/dataflow-azure-synapse-reference.html
- /7.0.1.jun.sw/data-integrate/dataflow/dataflow-azure-synapse-reference.html
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---

Here is a list of the fields for an Azure Synapse connection in ThoughtSpot DataFlow. You need specific information to establish a seamless and secure connection.

## Connection properties

<dl id="dataflow-azure-synapse-connection-properties">
<dlentry id="dataflow-azure-synapse-conn-connection-name"><dt>Connection name</dt><dd id="connection-name-description">Name your connection.</dd><dd id="connection-name-required">Mandatory field.</dd><dd id="connection-name-example"><strong>Example:</strong><br/>AzureSynapseConnection</dd></dlentry>
<dlentry id="dataflow-azure-synapse-conn-connection-type"><dt>Connection type</dt><dd id="connection-type-description">Choose the Azure Synapse connection type.</dd><dd id="connection-type-required">Mandatory field.</dd><dd id="connection-type-example"><strong>Example:</strong><br/>Azure Synapse</dd></dlentry>
<dlentry id="dataflow-azure-synapse-conn-host"><dt>Host</dt><dd id="host-description">Specify the name of the server.</dd><dd id="host-required">Mandatory field.</dd><dd id="host-example"><strong>Example:</strong><br/>http://www.example.net/</dd></dlentry>
<dlentry id="dataflow-azure-synapse-conn-port"><dt>Port</dt><dd id="port-description">Specify the connection port for Azure Synapse.</dd><dd id="port-required">Mandatory field.</dd><dd id="port-example"><strong>Example:</strong><br/>1234</dd></dlentry>
<dlentry id="dataflow-azure-synapse-conn-user"><dt>User</dt><dd id="user-description">Specify the user who connects to Azure Synapse. This user must have data access privileges.</dd><dd id="user-required">Mandatory field.</dd><dd id="user-example"><strong>Example:</strong><br/>user1</dd></dlentry>
<dlentry id="dataflow-azure-synapse-conn-password"><dt>Password</dt><dd id="password-description">Specify the password.</dd><dd id="password-required">Mandatory field.</dd><dd id="password-example"><strong>Example:</strong><br/>pswrd234%!</dd></dlentry>
<dlentry id="dataflow-azure-synapse-conn-jdbc-options"><dt>JDBC options</dt><dd id="jdbc-options-description">Specify JDBC URL for connecting to Azure Synapse, and the neccessary options.</dd><dd id="jdbc-options-required">Optional field.</dd><dd id="jdbc-options-example"><strong>Example:</strong><br/>jdbc:sqlserver://yourserver.database.windows.net:1234;database=mydatabase;</dd><dd id="jdbc-options-other"><strong>Other notes:</strong><br/>Under <strong>Advanced configuration</strong>.</dd></dlentry>
<dlentry id="dataflow-azure-synapse-conn-jdbc-options"><dt>JDBC options</dt><dd id="jdbc-options-description">Specify the options associated with the JDBC URL.</dd><dd id="jdbc-options-required">Optional field.</dd><dd id="jdbc-options-example"><strong>Example:</strong><br/><code>jdbc:sqlserver://[serverName[\instanceName][:portNumber]]</code></dd><dd id="jdbc-options-other"><strong>Other notes:</strong><br/>Advanced configuration</dd></dlentry>
</dl>


## Sync properties

<dl id="dataflow-azure-synapse-sync-properties">
<dlentry id="dataflow-azure-synapse-sync-data-extraction-mode"><dt>Data extraction mode</dt><dd id="data-extraction-mode-description">Specify the extraction type.</dd><dd id="data-extraction-mode-required">Mandatory field.</dd><dd id="data-extraction-mode-example"><strong>Example:</strong><br/>BCP</dd><dd id="data-extraction-mode-valid-values"><strong>Valid Values:</strong><br/>JDBC, BCP</dd><dd id="data-extraction-mode-default"><strong>Default:</strong><br/>JDBC</dd></dlentry>
<dlentry id="dataflow-azure-synapse-sync-column-delimiter"><dt>Column delimiter</dt><dd id="column-delimiter-description">Specify the column delimiter character.</dd><dd id="column-delimiter-required">Mandatory field.</dd><dd id="column-delimiter-example"><strong>Example:</strong><br/>, (comma)</dd><dd id="column-delimiter-valid-values"><strong>Valid Values:</strong><br/>Any character, (comma, semicolon) or a number. If using a number, system uses its ASCII value as delimiter.</dd><dd id="column-delimiter-default"><strong>Default:</strong><br/>, (comma)</dd></dlentry>
<dlentry id="dataflow-azure-synapse-sync-null-value"><dt>Null value</dt><dd id="null-value-description">Specify the string literal that represents NULL on the source. When loading data, the system replaces this with NULL.</dd><dd id="null-value-required">Optional field.<br/>Available only when <strong>Data extraction mode</strong> is <em>BCP</em>.</dd><dd id="null-value-example"><strong>Example:</strong><br/>NULL</dd><dd id="null-value-valid-values"><strong>Valid Values:</strong><br/>Any string literal</dd><dd id="null-value-default"><strong>Default:</strong><br/>NULL</dd></dlentry>
<dlentry id="dataflow-azure-synapse-sync-enclosing-character"><dt>Enclosing character</dt><dd id="enclosing-character-description">Specify if text columns in the source data are enclosed in quotes; if yes, single quotes or double quoates.</dd><dd id="enclosing-character-required">Optional field.</dd><dd id="enclosing-character-example"><strong>Example:</strong><br/>Double</dd><dd id="enclosing-character-valid-values"><strong>Valid Values:</strong><br/>Single, Double</dd><dd id="enclosing-character-default"><strong>Default:</strong><br/>Double</dd><dd id="enclosing-character-other"><strong>Other notes:</strong><br/>Required if text data uses newline character or delimiter character.</dd></dlentry>
<dlentry id="dataflow-azure-synapse-sync-escape-character"><dt>Escape character</dt><dd id="escape-character-description">Specify the escape character if using a text qualifier in the source data.</dd><dd id="escape-character-required">Optional field.</dd><dd id="escape-character-example"><strong>Example:</strong><br/>\"</dd><dd id="escape-character-valid-values"><strong>Valid Values:</strong><br/>Any ASCII character</dd><dd id="escape-character-default"><strong>Default:</strong><br/>\"</dd></dlentry>
<dlentry id="dataflow-azure-synapse-sync-fetch-size"><dt>Fetch size</dt><dd id="fetch-size-description">Specify the number of rows fetched into memory at the same time. If the value is 0, system fetches all rows at the same time.</dd><dd id="fetch-size-required">Mandatory field.<br/>Available only when <strong>Data extraction mode</strong> is <em>JDBC</em>.</dd><dd id="fetch-size-example"><strong>Example:</strong><br/>1000</dd><dd id="fetch-size-valid-values"><strong>Valid Values:</strong><br/>Any numeric value</dd><dd id="fetch-size-default"><strong>Default:</strong><br/>1000</dd></dlentry>
<dlentry id="dataflow-azure-synapse-sync-ts-load-options"><dt>TS load options</dt><dd id="ts-load-options-description">Specify additional parameters passed with the <code>tsload</code> command. The format for these parameters is:<br/><code>--&lt;param_1_name&gt; &lt;optional_param_1_value&gt;</code></dd><dd id="ts-load-options-required">Optional field.</dd><dd id="ts-load-options-example"><strong>Example:</strong><br/><code>--max_ignored_rows 0</code></dd><dd id="ts-load-options-valid-values"><strong>Valid Values:</strong><br/><br/><code> --null_value ""</code><br/><code> --escape_character ""</code><br/><code> --max_ignored_rows 0</code></dd><dd id="ts-load-options-default"><strong>Default:</strong><br/><code> --max_ignored_rows 0</code></dd><dd id="reference"><strong>Reference:</strong><br/><a href="{{ site.baseurl }}/reference/data-importer-ref.html">tsload flag reference</a></dd></dlentry>
</dl>

## Related Information

[Dataflow tips]({{ site.baseurl }}/data-integrate/data-flow-tips.html)
