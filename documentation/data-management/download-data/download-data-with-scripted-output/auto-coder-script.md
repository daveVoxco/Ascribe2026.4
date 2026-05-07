---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/data-management/download-data/download-data-with-scripted-output/auto-coder-script
---

# Auto-Coder Script

_Navigate: Client/Studies/Right-click study/Select Download Data/Select Scripted Output/Select Auto Coder_\
_Supervisor/Studies/Right-click study/Select Download Data/Select Scripted Output/Select Auto Coder_

This script is used to auto-code exact textual matches or to check for consistency in coding. Before you auto-code a study, you can check to see if the coding is consistent. For example, the coding consistency report can be useful for a study with multiple data loads. In the first load, these responses were coded like this:

Respondent 100 "chocolate taste" was coded with code 8: Chocolate taste

Respondent 110 "chocolate taste" was coded with code 21: Chocolate

Respondent 150 "chocolate taste" was coded with code 8: Chocolate taste

When you process a second load, any respondents who said “chocolate taste” will not be coded automatically because of the inconsistency in the first load.

If you run the coding consistency report after coding of the first load, you would find the inconsistency. In this example, you would fix the inconsistency by changing Respondent 110 from code 21 to code 8. Then, when you load any new respondents who said "chocolate taste," they will be coded automatically with code 8.

To run the report, select Auto Coder from the Scripted Output screen and click the Ok button. The next screen has these fields:

<table><thead><tr><th width="267.3333740234375" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Study List</td><td valign="top">List of study IDs you wish to compare for auto-coding; leave it blank to only check the current study.</td></tr><tr><td valign="top">Delimiter</td><td valign="top">Character that separates the study IDs in the Study List. It defaults to a comma.</td></tr><tr><td valign="top">Report or Code</td><td valign="top">Enter "report" to generate a consistency report or "code" to auto-code responses.</td></tr><tr><td valign="top">Case Insensitive Comparison</td><td valign="top">To compare responses and ignore case, enter "true" otherwise enter "false."</td></tr><tr><td valign="top">Order of Mention</td><td valign="top">If the order of codes applied is required criteria, enter "true" otherwise enter "false.”</td></tr><tr><td valign="top">Match Question ID or Shared Codebook</td><td valign="top">To only code or report on matching questions, enter " QuestionID" otherwise enter "codebooks." If you enter “ QuestionID,” you have more control over what is to be auto-coded. If you enter “codebooks,” the question ID does not matter. This option allows you to auto-code after loading data without having to reload the data.</td></tr></tbody></table>

After you enter the fields, click the OK button to run the report. After the report runs, right-click the link and select the appropriate option.
