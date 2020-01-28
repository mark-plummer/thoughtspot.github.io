By default, the language that ThoughtSpot UI displays depends on the system locale. It is simple to change it using the **Profile** interface.

The **Language** selection specifies more than just the language: it sets the locale, which controls both the language choice and standard data formats for date and number. So, if you set French as the default locale in your profile settings, the interface updates to reflect this. Be sure to refresh your browser page.

For example, in the United States the number format for large numbers uses the comma thousands separator and a period decimals separator, and looks like this: `xxx,xxx.xx`. In most  European countries, they use the reverse notation, with comma decimals separator and period thousands separator, like this: `xxx.xxx,xx`.

In addition to American English (*en-US*), ThoughtSpot supports the following locales:

| Locale |  Language  
|---|---|
| *da-DK* | Dansk  |
| *de-DE* | Deutsche  |
| *en-AU* | English (Australia)  |
| *en-CA* | English (Canada)  |
| *en-GB* | English (United Kingdom)  |
| *en-US* | English (United States)  |
| *es-US* | Español (latín)  |
| *es-ES* | Español (España)  |
| *fr-CA* | Français (Canada)  |
| *fr-FR* | Français (France)  |
| *it-IT* | Italiano  |
| *nl-NL* | Nederland (beta)  |
| *nb-NO* | Norsk  |
| *pt-BR* | Português (Brazil)  |
| *pt-PT* | Português (Portugal)  |
| *fi-FI* | Suomi  |
| *sv-SE* | Svenska  |
| *zh-CN* | 中文(简体)  |
| *ja-JP* | 日本語  |

ThoughtSpot translates keywords, operators, and error messages. See the keyword reference for all supported languages at (https://docs.thoughtspot.com/6.0/reference/keywords.html).

ThoughtSpot _DOES NOT_ translate formulas, or metadata entered by the user. For example, if you name a visualization 'Quarterly Sales' in any variant of English and subsequently change the locale to a variant of French, the visualization remains 'Quarterly Sales' and does not become 'Ventes trimestrielles'.
