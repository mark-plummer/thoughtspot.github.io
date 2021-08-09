---
title: [REST API connection reference]
summary: Learn about the fields used to create a REST API connection with ThoughtSpot DataFlow.
last_updated: 11/25/2020
redirect_from:
- /7.0.0.mar.sw/data-integrate/dataflow/dataflow-rest-api-reference.html
- /7.0.1.jun.sw/data-integrate/dataflow/dataflow-rest-api-reference.html
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---

Here is a list of the fields for a REST API connection in ThoughtSpot DataFlow. You need specific information to establish a seamless and secure connection.

## Connection properties

<dl id="dataflow-rest-api-connection-properties">
<dlentry id="dataflow-rest-api-conn-connection-name"><dt>Connection name</dt><dd id="connection-name-description">Name your connection.</dd><dd id="connection-name-required">Mandatory field.</dd><dd id="connection-name-example"><strong>Example:</strong><br/>RESTAPIConnection</dd></dlentry>
<dlentry id="dataflow-rest-api-conn-connection-type"><dt>Connection type</dt><dd id="connection-type-description">Choose the REST API connection type.</dd><dd id="connection-type-required">Mandatory field.</dd><dd id="connection-type-example"><strong>Example:</strong><br/>REST API</dd></dlentry>
<dlentry id="dataflow-rest-api-conn-authentication-type"><dt>Authentication type</dt><dd id="authentication-type-description">Specify the type of authentication that is required to connect to the REST API service.</dd><dd id="authentication-type-required">Mandatory field.</dd><dd id="authentication-type-example"><strong>Example:</strong><br/>NONE</dd><dd id="authentication-type-valid-values"><strong>Valid Values:</strong><br/>NONE, BASIC, or OAuth 2.0</dd><dd id="authentication-type-default"><strong>Default:</strong><br/>NONE</dd><dd id="authentication-type-other"><strong>Other notes:</strong><br/><ul><li><code>NONE</code>: Credentials not required to connect to web service.</li><li><code>BASIC</code>: Must have Username and Password for authentication.</li><li><code>OAuth 2.0</code>: Must supply the access key/token to connect to the web service.</li></ul></dd></dlentry>
<dlentry id="dataflow-rest-api-conn-rest-api-base-url"><dt>REST API base URL</dt><dd id="rest-api-base-url-description">Specify the end point URL to access REST API web-service.</dd><dd id="rest-api-base-url-required">Mandatory field.</dd></dlentry>
<dlentry id="dataflow-rest-api-conn-user"><dt>User</dt><dd id="user-description">Specify the user who connects to the Rest web service. This user must have data access privileges.</dd><dd id="user-required">Mandatory field.<br/>For BASIC authentication type only.</dd><dd id="user-example"><strong>Example:</strong><br/>userid</dd></dlentry>
<dlentry id="dataflow-rest-api-conn-password"><dt>Password</dt><dd id="password-description">Specify the password for the User.</dd><dd id="password-required">Mandatory field.<br/>For BASIC authentication type only.</dd><dd id="password-example"><strong>Example:</strong><br/>pswrd234%!</dd></dlentry>
<dlentry id="dataflow-rest-api-conn-obtain-access-token"><dt>Obtain access token</dt><dd id="obtain-access-token-description">Select this option to use access key/token to connect to the REST API web-service</dd><dd id="obtain-access-token-required">Optional field.<br/>For OAuth 2.0 authentication type only.</dd></dlentry>
<dlentry id="dataflow-rest-api-conn-access-token"><dt>Access token</dt><dd id="access-token-description">Specify the access token to authenticate REST API.</dd><dd id="access-token-required">Optional field.<br/>For OAuth 2.0 authentication type only.</dd></dlentry>
<dlentry id="dataflow-rest-api-conn-refresh-token"><dt>Refresh token</dt><dd id="refresh-token-description">Specify the refresh token to authenticate REST API.</dd><dd id="refresh-token-required">Optional field.<br/>For OAuth 2.0 authentication type only.</dd></dlentry>
<dlentry id="dataflow-rest-api-conn-oauth-client-id"><dt>OAuth client ID</dt><dd id="oauth-client-id-description">Specify the OAuth client ID</dd><dd id="oauth-client-id-required">Mandatory field.<br/>Displayed only when "obtain access token" check-box is selected</dd></dlentry>
<dlentry id="dataflow-rest-api-conn-mask-client-secret"><dt>Mask client secret</dt><dd id="mask-client-secret-description">Specify the OAuth client secret</dd><dd id="mask-client-secret-required">Mandatory field.<br/>Displayed only when "obtain access token" check-box is selected</dd></dlentry>
<dlentry id="dataflow-rest-api-conn-oauth-authorization-url"><dt>OAuth authorization URL</dt><dd id="oauth-authorization-url-description">Specify the OAuth authorization URL </dd><dd id="oauth-authorization-url-required">Mandatory field.<br/>Displayed only when "obtain access token" check-box is selected</dd></dlentry>
<dlentry id="dataflow-rest-api-conn-oauth-accesstoken-url"><dt>OAuth accesstoken URL</dt><dd id="oauth-accesstoken-url-description">Specify the OAuth accesstoken URL </dd><dd id="oauth-accesstoken-url-required">Mandatory field.<br/>Displayed only when "obtain access token" check-box is selected</dd></dlentry>
<dlentry id="dataflow-rest-api-conn-scope"><dt>Scope</dt><dd id="scope-description">Specify the number of users to access the account</dd><dd id="scope-required">Mandatory field.<br/>Displayed only when "obtain access token" check-box is selected</dd></dlentry>
<dlentry id="dataflow-rest-api-conn-callback-url"><dt>Callback URL</dt><dd id="callback-url-description">Secured domain URL of the repo which is used to register in REST API</dd><dd id="callback-url-required">Mandatory field.<br/>Displayed only when "obtain access token" check-box is selected</dd></dlentry>
<dlentry id="dataflow-rest-api-conn-rest-api-parameters"><dt>REST API parameters</dt><dd id="rest-api-parameters-description">When adding REST API parameters, click <strong>Add</strong>, and then specify the <code>Parameter name</code>, <code>Value</code>, and if the parameter is a <code>Header</code>.</dd><dd id="rest-api-parameters-required">Optional field.</dd></dlentry>
</dl>


## Sync properties

<dl id="dataflow-rest-api-sync-properties">
<dlentry id="dataflow-rest-api-sync-column-delimiter"><dt>Column delimiter</dt><dd id="column-delimiter-description">Specify the column delimiter character.</dd><dd id="column-delimiter-required">Mandatory field.</dd><dd id="column-delimiter-example"><strong>Example:</strong><br/>1</dd><dd id="column-delimiter-valid-values"><strong>Valid Values:</strong><br/>Any printable ASCII character or decimal value for ASCII character</dd><dd id="column-delimiter-default"><strong>Default:</strong><br/>1</dd></dlentry>
<dlentry id="dataflow-rest-api-sync-enclosing-character"><dt>Enclosing character</dt><dd id="enclosing-character-description">Specify if the text columns in the source data needs to be enclosed in quotes.</dd><dd id="enclosing-character-required">Optional field.</dd><dd id="enclosing-character-example"><strong>Example:</strong><br/>DOUBLE</dd><dd id="enclosing-character-valid-values"><strong>Valid Values:</strong><br/>SINGLE, DOUBLE</dd><dd id="enclosing-character-default"><strong>Default:</strong><br/>DOUBLE</dd><dd id="enclosing-character-other"><strong>Other notes:</strong><br/>This is required if the text data has newline character or delimiter character.</dd></dlentry>
<dlentry id="dataflow-rest-api-sync-escape-character"><dt>Escape character</dt><dd id="escape-character-description">Specify this if the text qualifier is mentioned. This should be the character which escapes the text qualifier character in the source data.</dd><dd id="escape-character-required">Optional field.</dd><dd id="escape-character-example"><strong>Example:</strong><br/>\"</dd><dd id="escape-character-valid-values"><strong>Valid Values:</strong><br/>Any ASCII character</dd><dd id="escape-character-default"><strong>Default:</strong><br/>\"</dd></dlentry>
<dlentry id="dataflow-rest-api-sync-null-value"><dt>Null value</dt><dd id="null-value-description">Specifies the string literal that indicates the null value in the extracted data. During the data load, the column value matching this string loads as null in the target.</dd><dd id="null-value-required">Optional field.</dd><dd id="null-value-example"><strong>Example:</strong><br/>NULL</dd><dd id="null-value-valid-values"><strong>Valid Values:</strong><br/>Any string literal</dd><dd id="null-value-default"><strong>Default:</strong><br/>NULL</dd></dlentry>
<dlentry id="dataflow-rest-api-sync-ts-load-options"><dt>TS load options</dt><dd id="ts-load-options-description">Specifies the parameters passed with the <code>tsload</code> command, in addition to the commands already included by the application. The format for these parameters is:<br/><code> --&lt;param_1_name&gt; &lt;optional_param_1_value&gt;</code><br/><code> --&lt;param_2_name&gt; &lt;optional_param_2_value&gt;</code></dd><dd id="ts-load-options-required">Optional field.</dd><dd id="ts-load-options-example"><strong>Example:</strong><br/><code>--max_ignored_rows 0</code></dd><dd id="ts-load-options-valid-values"><strong>Valid Values:</strong><br/><br/><code> --null_value ""</code><br/><code> --escape_character ""</code><br/><code> --max_ignored_rows 0</code></dd><dd id="ts-load-options-default"><strong>Default:</strong><br/><code> --max_ignored_rows 0</code></dd><dd id="reference"><strong>Reference:</strong><br/><a href="{{ site.baseurl }}/reference/data-importer-ref.html">tsload flag reference</a></dd></dlentry>
</dl>

## Related Information

[Dataflow tips]({{ site.baseurl }}/data-integrate/data-flow-tips.html)
