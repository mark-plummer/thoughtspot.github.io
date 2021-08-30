The latest release of ThoughtSpot Cloud contains several new and enhanced features.

<ul>
<li><a href="{{ site.baseurl }}#august-cloud-first">For the First user</a></li>
<li><a href="{{ site.baseurl }}#august-cloud-analyst">For the Analyst</a></li>
<li><a href="{{ site.baseurl }}#august-cloud-business-user">For the Business User</a></li>
<li><a href="{{ site.baseurl }}#august-cloud-data-engineer">For the Data Engineer</a></li>
<li><a href="{{ site.baseurl }}#august-cloud-it-ops-engineer">For the IT Ops Engineer</a></li>
<li><a href="{{ site.baseurl }}#august-cloud-developer">For the Developer</a></li>
</ul>

<h3><a id="august-cloud-first"></a>For the First user</h3>

<dl>

<dlentry id="getting-started">
<dt>Getting started with ThoughtSpot Cloud</dt>
<dd>The first user on the account has to complete a series of steps before other people can start using ThoughtSpot with your organization’s data. For these instructions, see <a href="{{ site.baseurl }}/admin/ts-cloud/ts-cloud-getting-started.html">Getting Started with ThoughtSpot Cloud</a>.
</dd>
</dlentry>
</dl>

<h3><a id="august-cloud-analyst"></a>For the Analyst</h3>

<dl>

<dlentry id="scriptability">
<dt>Scriptability</dt>
<dd><ul><li><strong>Improved import workflow:</strong> The new import workflow for <a href="{{ site.baseurl }}/admin/ts-cloud/scriptability.html">Scriptability</a> identifies errors, suggests solutions, and allows you to resolve these errors as part of the import workflow. It also has a cleaner, more intuitive UI, with separate sections for different object types.</li>
<li><strong>TML for tables with row-level security:</strong> ThoughtSpot now supports the migration and editing of tables with <a href="{{ site.baseurl }}/admin/data-security/row-level-security.html">row level security (RLS)</a> using <a href="{{ site.baseurl }}/admin/ts-cloud/tml.html#syntax-tables">TML</a>.</li>
</ul></dd>
</dlentry>

</dl>

<h3><a id="august-cloud-business-user"></a>For the Business User</h3>

<dl>
<dlentry id="watchlist-metrics">
<dt>Watchlist metrics</dt>
<dd>There are several new features for the metrics watchlist on your ThoughtSpot home page:
<ul><li>You can now open metrics in your watchlist in a new tab by right-clicking on the metric on the home page.</li>
<li>There is now no limit to the number of metrics you can add to your watchlist.</li></ul>
Refer to <a href="{{ site.baseurl }}/end-user/thoughtspot-one/thoughtspot-one-homepage.html#quick-links">ThoughtSpot One home page</a> for more information about watchlist metrics.</dd>
</dlentry>

<dlentry id="scatter-bubble-charts">
<dt>Minimum and maximum on x-axis for scatter and bubble charts</dt>
<dd>You can now specify a minimum and maximum value for measures on the x-axis of <a href="{{ site.baseurl }}/end-user/search/about-scatter-charts.html">scatter</a> and <a href="{{ site.baseurl }}/end-user/search/about-bubble-charts.html">bubble</a> charts. For more information on how to add a minimum and maximum value to a chart axis, refer to <a href="{{ site.baseurl }}/end-user/search/chart-axes-options.html#edit">Change axis options</a>.</dd>
</dlentry>

<dlentry id="deprecations">
<dt>Deprecations</dt>
<dd>ThoughtSpot is dropping support for one feature in the August Cloud release. This feature is <strong><em>not</em></strong> available in the August release. Refer to <a href="{{ site.baseurl }}/release/deprecation.html#de-support-august-cloud">Deprecation Announcements</a> for more information.</dd></dlentry>

</dl>

<h3><a id="august-cloud-data-engineer"></a>For the Data Engineer</h3>

<dl>
<dlentry id="custom-calendar">
<dt>Custom calendar enhancements</dt>
<dd>There are several enhancements for custom calendar in this release:
<ul><li>Custom calendar offers <span class="badge badge-update">Beta</span> support for Redshift, Teradata, Starburst, Synapse, and SAP Hana connections. These are off by default. To enable them, <a href="{{ site.baseurl }}/admin/misc/contact.html">contact ThoughtSpot support</a>.</li><li>Streamlined custom calendar window with the ability to preview calendar data.</li>
<li>Simplified workflow.</li>
<li>Preview calendar data from custom calendar list</li></ul>
For more information, refer to <a href="{{ site.baseurl }}/admin/ts-cloud/ts-cloud-embrace-cust-cal.html">Custom calendar overview</a>.</dd>
</dlentry>
</dl>

<h3><a id="august-cloud-it-ops-engineer"></a>For the IT Ops Engineer</h3>

<dl>
<dlentry id="credit-usage-pinboard">
<dt>Credit Usage pinboard</dt>
<dd>The Credit Usage pinboard, a pinboard for monitoring your credit consumption under the consumption-based pricing model, is now accessible from the Admin Console, under <strong>Billing > Credit consumption</strong>.</dd>
</dlentry>

<dlentry id="saml-mail-field">
<dt>SAML configuration</dt>
<dd>When configuring SAML authentication for ThoughtSpot, it is now mandatory to map the <code>mail</code> attribute in the IDP metadata file to the email address of the user. If your company cannot meet this requirement, <a href="{{ site.baseurl }}/admin/misc/contact.html">contact ThoughtSpot support</a>. For more information, refer to <a href="{{ site.baseurl }}/admin/ts-cloud/authentication-integration.html">configure SAML</a>.</dd>
</dlentry>

<dlentry id="admin-console">
<dt>UI improvement for help customization</dt>
<dd>This release improves the UI and user experience of the <a href="{{ site.baseurl }}/admin/ts-cloud/customize-help.html">Help customization</a> section of the admin console.</dd>
</dlentry>

</dl>

<h3><a id="august-cloud-developer"></a>For the Developer</h3>
<dl>
<dd>ThoughtSpot introduces several new features and enhancements to the Developer Portal and Visual Embed SDK. This release also introduces new REST APIs to manage users, user sessions, group privileges, cluster configuration, and metadata objects. </dd>

<dd>For more information, refer to <a href="https://developers.thoughtspot.com/docs/?pageid=whats-new" target="_blank">ThoughtSpot Developer Documentation</a>.</dd>
</dl>
