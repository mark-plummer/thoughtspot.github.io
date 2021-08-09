---
title: [Google BigQuery connection reference]
summary: Learn about the fields used to create an Google BigQuery connection with ThoughtSpot DataFlow.
last_updated: 07/03/2020
redirect_from:
- /7.0.0.mar.sw/data-integrate/dataflow/dataflow-google-bigquery-reference.html
- /7.0.1.jun.sw/data-integrate/dataflow/dataflow-google-bigquery-reference.html
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---

Here is a list of the fields for a Cassandra connection in ThoughtSpot DataFlow. You need specific information to establish a seamless and secure connection.

## Connection properties

<dl id="dataflow-google-bigquery-connection-properties">
<dlentry id="dataflow-google-bigquery-conn-project-id"><dt>Project id</dt><dd id="project-id-description">The identification number given to particular project and its always unique.</dd><dd id="project-id-required">Mandatory field.</dd><dd id="project-id-example"><strong>Example:</strong><br/>myproject-1234</dd></dlentry>
<dlentry id="dataflow-google-bigquery-conn-authentication-type"><dt>Authentication type</dt><dd id="authentication-type-description">It can be either Service Account or Access Tokens</dd><dd id="authentication-type-required">Mandatory field.</dd><dd id="authentication-type-example"><strong>Example:</strong><br/>Service Account</dd><dd id="authentication-type-valid-values"><strong>Valid Values:</strong><br/>Service Account, Access Token</dd><dd id="authentication-type-default"><strong>Default:</strong><br/>Service Account</dd></dlentry>
<dlentry id="dataflow-google-bigquery-conn-service-account-key/access-token"><dt>Service account key/access Token</dt><dd id="service-account-key/access-token-description">Provide the Service Account key when authentication type is selected as Service account and token when access token is selected as authentication type.</dd><dd id="service-account-key/access-token-required">Mandatory field.</dd><dd id="service-account-key/access-token-example"><strong>Example:</strong><br/>ABCDEFGH245HIJK</dd></dlentry>
<dlentry id="dataflow-google-bigquery-conn-query-priority"><dt>Query priority</dt><dd id="query-priority-description">Specify the time duration to run the query and it can be either Interactive or Batch.</dd><dd id="query-priority-required">Optional field.</dd><dd id="query-priority-example"><strong>Example:</strong><br/>BATCH</dd><dd id="query-priority-valid-values"><strong>Valid Values:</strong><br/>INTERACTIVE, BATCH</dd><dd id="query-priority-default"><strong>Default:</strong><br/>BATCH</dd><dd id="query-priority-other"><strong>Other notes:</strong><br/>In <strong>Advanced configuration</strong></dd></dlentry>
<dlentry id="dataflow-google-bigquery-conn-use-proxy"><dt>Use proxy</dt><dd id="use-proxy-description">If required, to use a proxy, select the check box Use Proxy and provide the details</dd><dd id="use-proxy-required">Optional field.</dd><dd id="use-proxy-other"><strong>Other notes:</strong><br/>In <strong>Advanced configuration</strong></dd></dlentry>
<dlentry id="dataflow-google-bigquery-conn-host"><dt>Host</dt><dd id="host-description">Specify the hostname or the IP address of the BigQuery system</dd><dd id="host-required">Optional field.<br/>For proxy authentication only.</dd><dd id="host-example"><strong>Example:</strong><br/>www.example.com</dd></dlentry>
<dlentry id="dataflow-google-bigquery-conn-port"><dt>Port</dt><dd id="port-description">Specify the port associated to the BigQuery system</dd><dd id="port-required">Optional field.<br/>For proxy authentication only.</dd><dd id="port-example"><strong>Example:</strong><br/>1234</dd></dlentry>
<dlentry id="dataflow-google-bigquery-conn-protocol"><dt>Protocol</dt><dd id="protocol-description">It can be either http or https</dd><dd id="protocol-required">Optional field.<br/>For proxy authentication only.</dd><dd id="protocol-example"><strong>Example:</strong><br/>http</dd><dd id="protocol-valid-values"><strong>Valid Values:</strong><br/>http, https</dd><dd id="protocol-default"><strong>Default:</strong><br/>http</dd></dlentry>
<dlentry id="dataflow-google-bigquery-conn-jdbc-options"><dt>JDBC options</dt><dd id="jdbc-options-description">Specify the options associated with the JDBC URL.</dd><dd id="jdbc-options-required">Optional field.</dd><dd id="jdbc-options-example"><strong>Example:</strong><br/><code>jdbc:sqlserver://[serverName[\instanceName][:portNumber]]</code></dd><dd id="jdbc-options-other"><strong>Other notes:</strong><br/>Advanced configuration</dd></dlentry>
</dl>


## Sync properties

<dl id="dataflow-google-bigquery-sync-properties">
<dlentry id="dataflow-google-bigquery-sync-column-delimiter"><dt>Column delimiter</dt><dd id="column-delimiter-description">Specify the column delimiter character.</dd><dd id="column-delimiter-required">Mandatory field.</dd><dd id="column-delimiter-example"><strong>Example:</strong><br/>1</dd><dd id="column-delimiter-valid-values"><strong>Valid Values:</strong><br/>Any printable ASCII character, or the  decimal value for an ASCII character.</dd><dd id="column-delimiter-default"><strong>Default:</strong><br/>The delimiter specified in sync</dd></dlentry>
<dlentry id="dataflow-google-bigquery-sync-enclosing-character"><dt>Enclosing character</dt><dd id="enclosing-character-description">Specify if the text columns in the source data needs to be enclosed in quotes.</dd><dd id="enclosing-character-required">Optional field.</dd><dd id="enclosing-character-example"><strong>Example:</strong><br/>DOUBLE</dd><dd id="enclosing-character-valid-values"><strong>Valid Values:</strong><br/>DOUBLE, SINGLE, NULL</dd><dd id="enclosing-character-default"><strong>Default:</strong><br/>SINGLE</dd></dlentry>
<dlentry id="dataflow-google-bigquery-sync-escape-character"><dt>Escape character</dt><dd id="escape-character-description">Specify the escape character if using a text qualifier in the source data.</dd><dd id="escape-character-required">Optional field.</dd><dd id="escape-character-example"><strong>Example:</strong><br/>\"</dd><dd id="escape-character-valid-values"><strong>Valid Values:</strong><br/>\\, any ASCII character</dd><dd id="escape-character-default"><strong>Default:</strong><br/>\"</dd></dlentry>
<dlentry id="dataflow-google-bigquery-sync-fetch-size"><dt>Fetch size</dt><dd id="fetch-size-description">Specify the number of rows to fetch at one time, and proces in memory. Tofeth all rows, specify 0 rows.</dd><dd id="fetch-size-required">Mandatory field.</dd><dd id="fetch-size-example"><strong>Example:</strong><br/>1000</dd><dd id="fetch-size-valid-values"><strong>Valid Values:</strong><br/>1000, 10, 100. 100000, any numeric value</dd><dd id="fetch-size-default"><strong>Default:</strong><br/>10</dd></dlentry>
<dlentry id="dataflow-google-bigquery-sync-allow-large-resultset"><dt>Allow large resultset</dt><dd id="allow-large-resultset-description">If enabled, allows query results that are larger in size.</dd><dd id="allow-large-resultset-required">Optional field.</dd><dd id="allow-large-resultset-example"><strong>Example:</strong><br/>FALSE</dd><dd id="allow-large-resultset-valid-values"><strong>Valid Values:</strong><br/>TRUE</dd><dd id="allow-large-resultset-default"><strong>Default:</strong><br/>FALSE</dd></dlentry>
<dlentry id="dataflow-google-bigquery-sync-ts-load-options"><dt>TS load options</dt><dd id="ts-load-options-description">Specifies the parameters passed with the <code>tsload</code> command, in addition to the commands already included by the application. The format for these parameters is:<br/><code> --&lt;param_1_name&gt; &lt;optional_param_1_value&gt;</code><br/><code> --&lt;param_2_name&gt; &lt;optional_param_2_value&gt;</code></dd><dd id="ts-load-options-required">Optional field.</dd><dd id="ts-load-options-example"><strong>Example:</strong><br/>--max_ignored_rows 0</dd><dd id="ts-load-options-valid-values"><strong>Valid Values:</strong><br/><br/><code> --null_value ""</code><br/><code> --escape_character ""</code><br/><code> --max_ignored_rows 0</code></dd><dd id="ts-load-options-default"><strong>Default:</strong><br/><code>. --max_ignored_rows 0</code></dd><dd id="reference"><strong>Reference:</strong><br/><a href="{{ site.baseurl }}/reference/data-importer-ref.html">tsload flag reference</a></dd></dlentry>
</dl>

## Related Information

[Dataflow tips]({{ site.baseurl }}/data-integrate/data-flow-tips.html)
