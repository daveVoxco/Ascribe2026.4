---
description: >-
  Automatically code closed-end and other-specify responses using matching
  rules.
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/verbatims/auto-code-closed-ends-and-other-specify-responses
---

# Auto-Code Closed Ends and Other Specify Responses

_Navigate: Supervisor/Studies/Right-click study/Select Questions/Right-click question/Select Auto Code_

The auto-code function is used to automatically code closed-ended questions and the closed-ended portions of other specify questions. This is also helpful in coding brand lists and the open ended portions of "other specify" type questions.

The following sections explain the [Auto Code page toolbar](auto-code-closed-ends-and-other-specify-responses.md#minitocbookmark2), the [Responses Grid](auto-code-closed-ends-and-other-specify-responses.md#minitocbookmark3), and the [auto code process](auto-code-closed-ends-and-other-specify-responses.md#minitocbookmark4).

## Auto Code Page Toolbar <a href="#minitocbookmark2" id="minitocbookmark2"></a>

_Navigate: Supervisor/Studies/Right-click study/Select Questions/Right-click question/Select Auto Code_

![](https://static.goascribe.com/Help/Auto_Code_Page_toolbar_june_12.gif)

The toolbar has several options, but they are not all active at the same time; it depends on the state of the data. For example, if there are empty codes, the Copy Responses to Empty Codes is active, but Add Codes is not. Here are the options:

<table><thead><tr><th width="208.66668701171875" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top"><p><img src="https://static.goascribe.com/Help/copy_responses_to_empty_codes.gif" alt="" data-size="original"></p><p>Copy Responses To Empty Codes</p></td><td valign="top">If there is a not a matched code, the option copies the response text to the match code column. You can edit the matched code text. Responses longer than 50 characters cannot be copied; you'll have to manually add those codes.</td></tr><tr><td valign="top"><p><img src="https://static.goascribe.com/Help/add_codes.gif" alt="" data-size="original"></p><p>Add Codes</p></td><td valign="top">Adds and applies the matched codes.</td></tr><tr><td valign="top"><p><img src="https://static.goascribe.com/Help/Apply_codes.gif" alt="" data-size="original"></p><p>Apply Codes</p></td><td valign="top">Applies the matched codes.</td></tr><tr><td valign="top"><p><img src="https://static.goascribe.com/Help/Auto_Code_options.gif" alt="" data-size="original"></p><p>Auto Code Options</p></td><td valign="top">Has additional options for handling responses which contain text as well as adding uncoded segments to the Notes field. See <a href="auto-code-options.md">Auto Code Options</a> for more information.</td></tr><tr><td valign="top"><p><img src="https://static.goascribe.com/Help/auto_code_settings.gif" alt="" data-size="original"></p><p>Settings</p></td><td valign="top"><p>The settings dialog has the option to hide items with a minimum number of mentions.</p><p>When the entered number is equal to 1, this means all items are displayed.</p><p>When the entered number is greater than 1, this means only items that are greater than or equal to the entered number display. You can view the hidden items by clicking Hidden Comments at the bottom of the page.</p></td></tr><tr><td valign="top"><p>List Single Mention Comments</p><p>or</p><p>List Less Than X</p><p>Mention Comments</p></td><td valign="top"><p>If the setting dialog contains a number greater than 1, List Less than X Mentions Comments displays. If you select the checkbox, then all comments display. If the checkbox is not selected, then items less than X are in the Hidden Comments section at the bottom of the page.</p><p>If the setting dialog contains 1, List Single Mention Comments displays, and all comments display. Selecting the checkbox does not change the display.</p><p>Note that even though comments are not displayed, they will be coded if they match a code input ID.</p></td></tr><tr><td valign="top"><p><img src="https://static.goascribe.com/Help/Search_icon_for_auto_code_page.gif" alt="" data-size="original"></p><p>Search</p></td><td valign="top">Displays the search dialog, which allows you to filter the grid by search criteria.</td></tr><tr><td valign="top"><p><img src="https://static.goascribe.com/Help/excel_icon_for_auto_code_page.gif" alt="" data-size="original"></p><p>Save As Excel</p></td><td valign="top">Creates an Excel file of the grid.</td></tr><tr><td valign="top"><p><img src="https://static.goascribe.com/Help/refresh_grid.gif" alt="" data-size="original"></p><p>Reset Grid Settings</p></td><td valign="top">Refreshes the grid to its original display, but is only applicable before you apply codes. For example, if you copy responses to empty codes or edit the matched code field, you can click the Reset icon to remove those changes. Once you click Add Codes or Apply Codes, the codes are applied, and that action cannot be reversed here.</td></tr></tbody></table>

## Responses Grid <a href="#minitocbookmark3" id="minitocbookmark3"></a>

The Auto Code page has these fields:

<table><thead><tr><th width="224" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Response</td><td valign="top">The data values found in the responses.</td></tr><tr><td valign="top">Matched Code</td><td valign="top"><p>The matched code description.</p><p>If no match is found, field contains the phrase "Enter new code"; type the text for the new code or click Copy Responses To Empty Codes to copy the response as the code description.</p><p>If a match is found, click Apply Codes to code the responses.</p></td></tr><tr><td valign="top">Input ID</td><td valign="top">Input ID of code.</td></tr><tr><td valign="top">Output ID</td><td valign="top">Output ID of code.</td></tr><tr><td valign="top">Regular Expression</td><td valign="top">This column displays the existing regular expression or the regular expression that is created when you add a code; it is only for text responses.</td></tr><tr><td valign="top">Respondents</td><td valign="top">The count of respondents whose response match the input value of the question’s codebook.</td></tr><tr><td valign="top">Codes Currently Applied</td><td valign="top">The number of codes currently applied. Zeroes mean that no codes are applied.</td></tr></tbody></table>

## Auto Code Process <a href="#minitocbookmark4" id="minitocbookmark4"></a>

Closed-ended questions may have a pre-defined response list. For example, you may have a likes rating scale from 1 to 5. Ascribe views the response list just like any other codebook. To auto-code a closed-ended question, set up the codebook/response list first in Ascribe Coder. Make sure that the input code values match the responses’ values that were generated in the survey.

Once the codebook is ready, navigate to the Auto Code page (from the Questions page, right-click the question, and select Auto Code.)

Responses can be numeric or text or a combination of both. If the responses are separated by pipe symbols ( | ), Ascribe parses the data into segments. The segments are listed in the Responses Grid. The segments are matched to existing codes by input code ID. If there is no match, you can copy the segment to the Matched Code column or enter it manually. You also have the choice whether to add the codes or only code the matched segments.

The Auto Code page has several options for auto-coding, and how each one is used depends on your data.

<table><thead><tr><th width="224" valign="top">Data</th><th valign="top">Action</th></tr></thead><tbody><tr><td valign="top">All Responses Have Matched Codes</td><td valign="top">Click the Apply Codes button to apply the matched codes.</td></tr><tr><td valign="top">Some Responses Have Matched Codes And Some Responses Do Not</td><td valign="top"><p><strong>If you want to add codes for all missing codes:</strong> Click Copy Responses to Empty Codes button to copy the response to the Matched Code column. You can edit the Matched Code field if necessary. Then click Add Codes to add and apply the codes.</p><p>Keep in mind that single mention responses are listed in the Single Mention Comments dialog; use the toolbar option of List Single Mention Comments to display them in the Responses Grid if you want to add codes for any of them that do not have matched codes.</p><p><strong>If you don't want to add codes:</strong> Click Apply Codes to apply the matched codes; not adding codes can lead to partially coded data. To help with this situation, you can use <a href="auto-code-options.md">Auto Code Options</a> to apply matched codes and add uncoded segments to the Notes field; then use Ascribe Coder to <a href="../ascribe-coder/response-filters-and-sorting.md">filter responses that have data in the Notes field</a> and handle any uncoded segments.</p></td></tr></tbody></table>
