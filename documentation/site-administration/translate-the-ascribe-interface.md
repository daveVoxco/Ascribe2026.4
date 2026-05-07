---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/site-administration/translate-the-ascribe-interface
---

# Translate the Ascribe Interface

Ascribe is fully language capable and supports a number of languages.

{% hint style="info" %}
#### Note

Ascribe is fully Unicode compliant.
{% endhint %}

You can translate the Ascribe website to other languages. When you translate the site, you change the text displayed by Ascribe in menus, buttons, headers, explanatory text, and so on. Translating the site does **not** translate verbatims.

To translate the site, you must have localize access (this privilege is set on the Associates page.) The language you use to translate the site must be your language in your internet browser. Also, you may use this capability to change the text in any of the strings in English or any other language. This is useful if you would like to use different wording.

Be careful to preserve the symbols in the text as they govern the way other text strings are inserted into the text string that you are translating.

## Page Layout <a href="#minitocbookmark2" id="minitocbookmark2"></a>

This page has this format: black title bar with a toolbar underneath, followed by the grid of Ascribe fields and translations.

## Title Bar <a href="#minitocbookmark3" id="minitocbookmark3"></a>

The title bar has these fields:

<table><thead><tr><th width="228" align="center" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/Studies_page_navigation_icon.png" alt=""></p><p>Navigation Icon</p></td><td valign="top">Click the icon to navigate to other pages in Ascribe. The page behind the menu is blurred if the browser supports this action. Click anywhere in the black or off the menu to close it. If the current page is displayed in the menu, it has an arrow in front of it. Links appear in the menu only if the user has privilege to navigate to the page.</td></tr><tr><td align="center" valign="top">Page Name</td><td valign="top">Self-explanatory</td></tr><tr><td align="center" valign="top">Ascribe Coder Logo</td><td valign="top">Acts as the one-click navigation option to the page you selected in <a href="../get-started/customization-features/user-options.md">User Options</a></td></tr><tr><td align="center" valign="top">Account</td><td valign="top">The account you're logged into</td></tr><tr><td align="center" valign="top">User</td><td valign="top">User name has a drop-down list of options: navigate to User Options, open and submit a support request, and logout</td></tr><tr><td align="center" valign="top">Language</td><td valign="top">The language that initially displays is the browser language. The language drop-down allows you to change the language for any translations that exist for the account.</td></tr><tr><td align="center" valign="top">Session Time</td><td valign="top">The duration of the user's session is displayed in HH:MM format</td></tr><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/help_icon_jan2022.jpg" alt=""></p><p>Online Help and Guides</p></td><td valign="top">The drop-down list contains options for Ascribe Help (the online help system) and interactive guides for the page.</td></tr></tbody></table>

## Toolbar <a href="#minitocbookmark4" id="minitocbookmark4"></a>

The toolbar has these fields:

<table><thead><tr><th width="243.33331298828125" align="center" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td align="center" valign="top">Add Language</td><td valign="top">Click this option to add another language to the language drop-down; translations must exist on the account in order to use the language.</td></tr><tr><td align="center" valign="top">Reload Strings</td><td valign="top"><p>When you click the Reload Strings button and click Show String Keys, Ascribe displays a number following each string. This number corresponds to the Key value in the translations table. You can use this to determine exactly which string to change to update the translation.</p><p>These numbers display in your browser session only. Other users will not see the numbers. This setting remains in effect until you change it back.</p><p>Also, when you click Reload Strings, this action causes any modifications made in the Localize page to be immediately reflected in the web site.</p></td></tr><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/localize_excel_export.jpg" alt=""></p><p>Excel Export</p></td><td valign="top">Click to export the current page view to Excel; only the fields displayed are included in the export.</td></tr><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/Upload_translations.jpg" alt=""></p><p>Upload Translations</p></td><td valign="top">Upload an Excel file of translations. The file must have the format of columns titled Key, English, and Translation. Before you upload, you can download the current backup file in case there is a problem.</td></tr></tbody></table>

## Set the Browser Language to Add New Translations <a href="#minitocbookmark5" id="minitocbookmark5"></a>

The first step is to set your browser to the desired target language and then follow these steps:

1. Click the Languages... button. If the language you want is not displayed in the list, click the Add... button and add the language.
2. Click the desired language, then click the Move Up button until it is at the top of the list and then click OK.
3. To make the change effective, you must log out of Ascribe and log in again.

Language selections come in two types: those with two-character identifiers like ' fr' and those with identifiers like ' fr-ca'. The two character identifiers are base languages, and the longer ones are regional identifiers. For example, ' fr' means French, and ' fr-ca' means Canadian French.

When you translate the site, start with the two-character language. When the user selects a language, Ascribe displays the string keys for the selected language (like fr-ca). For a given string, if there is no fr-ca translation, Ascribe will look for an fr translation (the base language). If it does not find one, it displays the English string. This means you should always provide translations for the base language first. If you want to do regional customizations within that language, you can select the more specific language (such as fr-ca) and enter only the strings that differ between fr and fr-ca.

When you log into Ascribe, the language drop-down field in the toolbar displays the browser language.&#x20;

## Change Ascribe Text <a href="#minitocbookmark6" id="minitocbookmark6"></a>

_Navigate: Localize_

Once you have set your browser to the language you want to translate to, open the Localize page.&#x20;

Here are the available columns on the Localize page:

<table><thead><tr><th width="275.33331298828125" valign="top">Column</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Column 1 (Key in English)</td><td valign="top">This is a number that identifies the string. You cannot change this number.</td></tr><tr><td valign="top">Column 2</td><td valign="top"><ul><li>This is the English version of the string. You cannot change this string. It is the string that you need to translate.</li><li>The <em>%%1</em> means 'substitute a value in this location'. When Ascribe displays the string, it replaces the <em>%%1</em> with the information to display. You must keep the <em>%%1</em> in the translated string.</li><li><em>%%1</em> means 'parameter one', <em>%%2</em> means 'parameter 2' and so on. You can rearrange the position of these parameters in the translated string.</li></ul><p>These strings are HTML. When you see &#x3C; > characters, it means that an HTML tag is in the string. You must not translate the text inside of the &#x3C; > characters.</p></td></tr><tr><td valign="top">Column 3 (Translation)</td><td valign="top">This is the translation of the English string. You can change this string if you right-click the phrase and select Edit.</td></tr></tbody></table>

To change the translation of a phrase, left-click the translation column and enter the translation. When you change translations, you will not see the results in Ascribe until you log out and log in again; you may also need to click the Reload Strings button to clear cache.&#x20;

To help with matching the text displayed in Ascribe with the specific entry in the table of translations, you can set Ascribe to show the key value of each string. See Reload Strings (below) for details.

## Reload Strings <a href="#minitocbookmark7" id="minitocbookmark7"></a>

_Navigate: Localize_

When you click the Reload Strings button and click Show String Keys, Ascribe displays a number following each string. This number corresponds to the Key value in the translations table. You can use this to determine exactly which string to change to update the translation.

These numbers display in your browser session only. Other users will not see the numbers. This setting remains in effect until you change it back.

Also, when you click Reload Strings, this action causes any modifications made in the Localize page to be immediately reflected in the web site.
