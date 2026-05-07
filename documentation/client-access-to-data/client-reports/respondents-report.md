---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/client-access-to-data/client-reports/respondents-report
---

# Respondents Report

The Respondents page allows you to view respondents, delete them, or export them to Excel. When you navigate to this page, you must make choices about which respondents you want to view or export.

**Location**: Supervisor/Studies/Right-click study/Select Reports/Select Respondents

**To display respondents:** Select the Page Size and Question Types in the gray filter bar and click Update. Your choices will stick from study to study so you may only need to click Update if you are satisfied with the filters.

**To export the respondents to Excel without displaying them first: Just click Save as Excel.**

Here is an example of the Respondents page when you first navigate to it. The study ID and name are at the top of the page, above the gray toolbar. To display respondents, choose question types and page size and click Update.

![](https://static.goascribe.com/Help/Respondents_Report_091214.gif)

**Toolbar**:

<table><thead><tr><th width="217.33331298828125" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Update</td><td valign="top">Click the Update button after you make a selection of the various options.</td></tr><tr><td valign="top">Search</td><td valign="top">Search will find and display a respondent ID or a group of respondent IDs starting with a string of characters. For example, you can search for 10015, and respondent 10015 will be listed. If you are using 5 digit numeric respondent ids and you enter "1001", the list will display 10010 through 10019.</td></tr><tr><td valign="top">Question Type</td><td valign="top">Use the check boxes to select or unselect which questions should display. <strong>The page will display a maximum of 100 columns. To see the entire report, use the Save As Excel option.</strong></td></tr><tr><td valign="top">Load List</td><td valign="top"><p>Load List displays a box where you can enter individual respondent IDs or copy and paste a list of respondent IDs from another source such as Word or Excel. To prepare a list for copying to the Load List, enter the individual respondent IDs on separate lines as follows:</p><p>10001<br>10005<br>10010<br>10034<br>After you enter the respondent IDs, click OK. The respondents and the verbatims display. The text of the Load List button displays in red when items are in the list box.</p><p> </p><p>To clear the Load List filter, click Load List, click Clear, and click Update.</p></td></tr><tr><td valign="top">Save As Excel</td><td valign="top"><p>Use this option to export respondents to Excel. The file will contain three sheets: Full Data, Load File, and Coded Status.</p><p> </p><p>This option uses the Question Type filters and the Load List filter when creating the Excel file. For example, if you have selected Open and then click Save As Excel, only the open-ended questions for the respondents will be saved in the Excel file. If you have respondents in the Load List filter, only the responses for those respondents will be saved in the Excel file.</p><p> </p><p>It may take time for the Excel file to generate, depending on the number of respondents. During this time, you will receive a message which says "Generating Excel Spreadsheet". Once the file is ready, you can save it to your computer.</p></td></tr></tbody></table>

The Page Size option, which indicates how many respondents will display, is below the gray filter bar. It defaults to 50; other options are 100, 250, and 500. **The maximum number of respondents that can display at one time is 500; use the Save as Excel option to view all respondents.**

Once you click Update, these additional options display:

<table><thead><tr><th width="195.3333740234375" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Records</td><td valign="top">Select a range of records to display. The range is based on the Page Size that is selected and the total number of respondents in the study.</td></tr><tr><td valign="top">Data View</td><td valign="top"><p>Data View allows you to select what is displayed in the individual cells. The choices are:</p><ul><li>Abbreviated Data - displays the first 20 characters of the response</li><li>Full Data - displays the entire text of the response</li><li>Load File – displays the name of the file from which the data was loaded</li><li>Coded Status – displays the coding status of the response</li></ul></td></tr></tbody></table>

Below the toolbar are these columns: a selector check box, respondent ID, and question ID columns (one column for each question in the study, based on question type filters with a maximum of 100 columns.)

To select respondents, you can click the box next to the respondent ID. Or you can use the right-click menu to select and delete respondents. Here is the right-click menu for the page:

<table><thead><tr><th width="302.6666259765625" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Studies</td><td valign="top">Navigates to the Studies page.</td></tr><tr><td valign="top">Questions</td><td valign="top">Navigates to the Questions page.</td></tr><tr><td valign="top">Select All</td><td valign="top">This option selects all of the respondents in the current list.</td></tr><tr><td valign="top">Clear All</td><td valign="top">This option de-selects all of the respondents in the current list.</td></tr><tr><td valign="top">Delete Selected Respondents</td><td valign="top">This option removes all of the selected respondents from all questions in the study.</td></tr><tr><td valign="top">Keyboard Shortcuts</td><td valign="top">Opens the keyboard shortcuts in case you need to change the shortcuts for listening to audio responses.</td></tr></tbody></table>

{% hint style="info" %}
#### Note

**Deleting respondents from this page will remove the respondent from all questions in the study.** To remove respondents from individual questions, see [Edit Verbatims](../../verbatims/edit-verbatims/).

There are only two ways to get a respondent back after you delete it. One way is to reload the data file. The Load File option gives you the name of that file. The other way is to save the study before you delete respondents and then restore the study. But, remember, you have to save the study before you delete any respondents.
{% endhint %}
