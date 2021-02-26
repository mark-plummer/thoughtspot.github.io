The latest release of ThoughtSpot Cloud contains several new and enhanced features.

<ul>
<li><a href="{{ site.baseurl }}#feb-cloud-analyst">For the Analyst</a></li>
<li><a href="{{ site.baseurl }}#feb-cloud-business-user">For the Business User</a></li>
<li><a href="{{ site.baseurl }}#feb-cloud-data-engineer">For the Data Engineer</a></li>
<li><a href="{{ site.baseurl }}#feb-cloud-it-ops-engineer">For the IT Ops Engineer</a></li>
</ul>

<h3><a id="feb-cloud-analyst"></a>For the Analyst</h3>

<dl>
  <dlentry id="scriptability">
    <dt>Scriptability</dt>
    <dd><ul><li><p>You can now create and edit joins at the table level using TML, including range and generic joins. You must edit these joins from the source table, not the destination table. Refer to <a href="{{ site.baseurl }}/admin/ts-cloud/tml.html#syntax-tables">ThoughtSpot Modeling Language</a>.</p>
    <p>This feature is in Beta. To enable it, <a href="{{ site.baseurl }}/admin/misc/contact.html">contact ThoughtSpot Support</a>.</p></li>
    <li><strong>Export custom SpotApps</strong>: Support for custom SpotApp export is now GA and on by default. You can now export your own custom SpotApps, or collections of Scriptable ThoughtSpot Answers, Pinboards, Views, tables, and Worksheets, packaged together as a zip file. Simply navigate to <strong>Data > SpotApps</strong> and choose the objects you would like to include in a custom SpotApp. Refer to <a href="{{ site.baseurl }}/admin/ts-cloud/app-templates.html">SpotApps</a>.</li></ul>
</dd></dlentry>

 <dlentry id="simplified-join-creation">
  <dt>Simplified join creation</dt>
  <dd>This release makes creating and editing joins from a table more flexible and intuitive. Our new joins interface allows you to define and edit the join type and cardinality at the table level, where previously this was only possible at the Worksheet level. Refer to <a href="{{ site.baseurl }}/admin/worksheets/add-joins.html#table-join">Table joins</a>.
</dd></dlentry>

<dlentry id="pinboard-download-api">
  <dt>Pinboard Download API</dt>
  <dd>Use the new Pinboard Download API to programmatically download Pinboards, or specific visualizations from the Pinboards, as PDFs. Refer to <a href="{{ site.baseurl }}/reference/api/pinboard-download-api.html">Pinboard Download API</a>.
</dd></dlentry>

<dlentry id="spotiq-analyze">
  <dt>Support for SpotIQ Analyze</dt>
  <dd><p>In this release, ThoughtSpot Cloud adds support for SpotIQ analyze. Now you can analyze any answer, pinboard visualization, or data source to generate instant insights, by clicking the SpotIQ analyze button <img src="{{ site.baseurl }}/images/icon-lightbulb.png" alt="SpotIQ analyze icon" class="inline"/>. For more information, see <a href="{{ site.baseurl }}/spotiq/customization.html">Custom SpotIQ analysis</a>.</p></dd></dlentry>

</dl>

<h3><a id="feb-cloud-business-user"></a>For the Business User</h3>

<dl>
<dlentry id="home-page-shortcuts">
<dt>Home page shortcuts</dt>
<dd><p>You can now create and access quick links to your most-used Answers and Pinboards from the ThoughtSpot One home page. Refer to <a href="{{ site.baseurl }}/end-user/thoughtspot-one/thoughtspot-one-homepage.html#quick-links">Home page shortcuts</a>.</p>
<p>ThoughtSpot One may be off in your environment. To enable ThoughtSpot One, <a href="{{ site.baseurl }}/admin/misc/contact.html">contact ThoughtSpot Support.</a></p></dd>
</dlentry>

<dlentry id="internet-explorer">
  <dt>Deprecation of Internet Explorer</dt>
<dd>ThoughtSpot browser support for Internet Explorer is now deprecated. Refer to <a href="{{ site.baseurl }}/end-user/accessing.html">ThoughtSpot browser access</a> for a list of supported browsers.</dd>
</dlentry>

</dl>

<h3><a id="feb-cloud-data-engineer"></a>For the Data Engineer</h3>

<dl>
<dlentry id="embrace">
<dt>Embrace</dt>
<dd>Embrace now supports security passthrough for Snowflake and Google BigQuery using OAuth for authentication and authorization. For more information, see <a href="{{ site.baseurl }}/admin/ts-cloud/ts-cloud-embrace-snowflake-add-connection.html">Snowflake</a>, and <a href="{{ site.baseurl }}/admin/ts-cloud/ts-cloud-embrace-gbq-add-connection.html">Google BigQuery</a>.</dd>
<dd>Embrace passthrough functions are available for Snowflake. Passthrough functions allow you to send custom SQL expressions directly to your Snowflake database without being interpreted by ThoughtSpot. For more information, see <a href="{{ site.baseurl }}/admin/ts-cloud/ts-cloud-embrace-snowflake-passthrough.html">Passthrough functions for Snowflake</a>.</dd>
<dd>Embrace now supports Oracle Autonomous Database <span class="label label-beta">Beta</span>. This feature is in beta and disabled by default. To enable this feature, contact <a href="{{ site.baseurl }}/admin/misc/contact.html">ThoughtSpot Support</a>.</dd>
</dlentry>
</dl>

<h3><a id="feb-cloud-it-ops-engineer"></a>For the IT Ops Engineer</h3>

<dl>
<dlentry id="new-region-support">
<dt>New region support</dt>
<dd>ThoughtSpot Cloud is now available in the following 2 regions, in addition to US East and West, Sydney, and Ireland:
<ul><li>Frankfurt</li>
<li>Singapore</li></ul></dd></dlentry>

<dlentry id="search-answers-pinboard">
<dt>Search on Answers Pinboard</dt>
<dd>There are several changes to the behavior of the <a href="{{ site.baseurl }}/admin/thoughtspot-one/query-intelligence-pinboard.html">Stats and Trends for Search on Answers Pinboard</a>:
<ul>
<li>The Pinboard and its underlying Worksheet, <strong>Discover Monitoring Data</strong>, are now accessible only to admins by default. Admins can share the Pinboard and Worksheet with anyone else who might need this information.</li>
<li>The Pinboard is populated with your users' Search on Answers data by default. You do not need to contact ThoughtSpot Support to see your users' Search on Answers data in the Pinboard.</li></ul></dd>
</dlentry>

<dlentry id="pinboard-download-control">
<dt>Pinboard download control</dt>
<dd><p>You can now limit or remove the options ThoughtSpot provides for downloading Pinboards and their visualizations. You can allow users to only download Pinboard visualizations in a specific format (such as .csv), or you can restrict access to downloading Pinboards and their visualizations altogether.</p>
<p>This is a cluster-level feature. You cannot configure permissions for specific users.</p>
<p>This is an embed-only feature. To enable this functionality, <a href="{{ site.baseurl }}/admin/misc/contact.html">contact ThoughtSpot Support</a>.</p></dd>
</dlentry>

<dlentry id="consumption-based-pricing">
<dt>Consumption-based pricing</dt>
<dd>ThoughtSpot now offers consumption, or usage, based pricing. Refer to <a href="{{ site.baseurl }}/admin/ts-cloud/consumption-pricing.html">Consumption-based pricing</a> and the <a href="{{ site.baseurl }}/admin/ts-cloud/consumption-pricing-faq.html">Consumption pricing FAQ</a>. To compare consumption- and capacity-based pricing, refer to <a href="https://www.thoughtspot.com/pricing" target="_blank">ThoughtSpot pricing</a>.</dd>
</dlentry>
</dl>
