---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/ascribe-coder/word-list
---

# Word List

![](https://static.goascribe.com/Help/word_list_icon_02_071514.gif)

Click the Word List icon to display the Word List dialog, which provides an interactive word list. Note that the Word List icon may be hidden through the [Tools setting](responses-settings.md#minitocbookmark5) on the Appearance tab of Responses Settings. You can also access the Word List dialog through the navigation menu option of Tools.

In the Word List dialog, click on a word to search the coding source for that word. The responses will be displayed with the word highlighted - unless the word matches a regular expression in the codebook, in which case it will be underlined.

Here is an example of the Word List dialog:

![](https://static.goascribe.com/Help/Word_List_dialog.gif)

When you click on a word, the [Responses Containing This Text field](search-responses.md#minitocbookmark2) in the Search Responses dialog is populated with an expression based on that word. For example, if the word 'dixie' is clicked, the Responses Containing This Text field would contain \<dixie> as shown below. (The Search Responses dialog does not open - this action is done automatically without the dialog displaying.)

![](https://static.goascribe.com/Help/search_responses_with_expression.png)

Also note that the [Show Only field](search-responses.md#minitocbookmark3) in the Search Responses dialog takes priority over the Word List Options dialog. For example, if the Show Only field has Uncoded Responses selected, the Word List will use that rather than what is selected in the [Word List Options](word-list.md#minitocbookmark2) dialog.

Here are the fields:

<table><thead><tr><th width="221.33331298828125" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Count</td><td valign="top">Number of times a word appears in the source selected in the Word List Options dialog.</td></tr><tr><td valign="top">Percentage</td><td valign="top">Percentage based on total number of words displayed in the Word List. The Word List options have an effect on which words are displayed; for example, if a word does not meet Minimum Count, it will not be displayed, and therefore, the percentage calculation will not include those words.  </td></tr><tr><td valign="top">Word</td><td valign="top">List of words that appear in the source selected in the Word List Options dialog.</td></tr><tr><td valign="top">Options</td><td valign="top">Options that control how the Word List is created and displayed.</td></tr><tr><td valign="top">Update</td><td valign="top">Update or refresh the list after changing options.</td></tr><tr><td valign="top">Close</td><td valign="top">Close the dialog.</td></tr></tbody></table>

## Word List Options <a href="#minitocbookmark2" id="minitocbookmark2"></a>

Here is an example of the Word List Options dialog:

![](https://static.goascribe.com/Help/Word_List_Options_dialog.gif)

&#x20;Here are the fields:

<table><thead><tr><th width="224.6666259765625" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Word Characters</td><td valign="top">A list of characters to ignore when the responses are displayed in the word list.</td></tr><tr><td valign="top">Words To Ignore</td><td valign="top">A list of words to ignore when the responses are displayed in the word list.</td></tr><tr><td valign="top">Minimum Count</td><td valign="top">Allows you to change the display according to the number of mentions of a word.</td></tr><tr><td valign="top"><strong>Select From</strong></td><td valign="top"> </td></tr><tr><td valign="top">Verbatim</td><td valign="top">Uses verbatims as the source for the Word List.</td></tr><tr><td valign="top">Translation</td><td valign="top">Uses translations as the source for the Word List.</td></tr><tr><td valign="top">Transcription</td><td valign="top">Uses transcriptions as the source for the Word List.</td></tr><tr><td valign="top">Notes</td><td valign="top">Uses notes as the source for the Word List.</td></tr><tr><td valign="top">All Responses</td><td valign="top">Uses both coded and uncoded responses as the source for the Word List. Note: The <a href="search-responses.md#minitocbookmark3">Show Only field</a> in the Search Responses dialog takes priority over the Word List Options dialog.</td></tr><tr><td valign="top">Coded Responses</td><td valign="top">Uses coded responses as the source for the Word List. Note: The <a href="search-responses.md#minitocbookmark3">Show Only field</a> in the Search Responses dialog takes priority over the Word List Options dialog.</td></tr><tr><td valign="top">Uncoded Responses</td><td valign="top">Uses uncoded responses as the source for the Word List. Note: The <a href="search-responses.md#minitocbookmark3">Show Only field</a> in the Search Responses dialog takes priority over the Word List Options dialog.  </td></tr><tr><td valign="top"><strong>Sort By</strong></td><td valign="top"> </td></tr><tr><td valign="top">Count</td><td valign="top">Words are sorted in descending numerical order.</td></tr><tr><td valign="top">Word</td><td valign="top">Words are sorted in alphabetical order.</td></tr></tbody></table>
