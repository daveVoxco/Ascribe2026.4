---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/client-access-to-data/client-reports/card-layout-report
---

# Card Layout Report

The Card Layout Report finds errors in your study set-up before you deliver data. It displays any problems detected in card/column/columns set-up and in numbering.

**Location**: Client/Right-click study/Select Reports/Click Card Layout

The report is divided into two panes. The upper pane displays the questions in the study and is updated automatically if you change the properties of the study or the questions. The lower pane displays a picture of the data output in cards and columns. The lower pane is updated only if you select Update Card View in the upper pane and click the Update button.

**Question list fields**:

<table><thead><tr><th width="206.66668701171875" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Question ID</td><td valign="top">The question ID</td></tr><tr><td valign="top">Question Label</td><td valign="top">The question label</td></tr><tr><td valign="top">Type</td><td valign="top">The question type</td></tr><tr><td valign="top">Card</td><td valign="top">The card number where the data will be placed in column binary output.</td></tr><tr><td valign="top">Layout</td><td valign="top">Numeric, column punch, and punch using column offset are the three data layout types.</td></tr><tr><td valign="top">Maximum Codes</td><td valign="top">The maximum number of codes allowed for this question as defined on the Data tab of the Edit Question dialog. (0 = unlimited number of codes.)</td></tr><tr><td valign="top">Max Codes Applied</td><td valign="top">The maximum number of codes that actually have been applied to any one response.</td></tr><tr><td valign="top">Column</td><td valign="top">In numeric layout, codes for this question will start in this column. Punch using column offset layout uses the column field in a calculation. See <a href="../../data-management/download-data/download-data-with-scripted-output/column-binary-output-script.md#minitocbookmark5">Punch Using Column Offset</a> for more information. Punch layout does not use this field.</td></tr><tr><td valign="top">Columns Per Code</td><td valign="top">The number of columns used to write the code which is also the number of digits in the output code value. This field only applies to the numeric layout type.</td></tr><tr><td valign="top">Columns Used</td><td valign="top">The maximum number of columns used for the output of codes for this question, based on the codes currently applied to this question. Applies only to the numeric layout type.</td></tr></tbody></table>

The lower pane displays a diagram of the cards and columns to be output. The columns that are used display across the top of the card. The report has these fields:

<table><thead><tr><th width="194.66668701171875" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">C</td><td valign="top">Card number</td></tr><tr><td valign="top">R</td><td valign="top">Respondent ID</td></tr><tr><td valign="top">Question ID</td><td valign="top">The report displays the columns used by the questions.</td></tr><tr><td valign="top">Problems</td><td valign="top">A list of any problems detected by analysis of the study and question settings, the codebooks, and the codes currently applied in the study. This message displays if there are no errors - <em>Card field : Specified column 0 starts before the first column of the card (1).</em></td></tr></tbody></table>

Use the Edit icon (<img src="https://static.goascribe.com/Help/Edit_Question_Properties_icon.gif" alt="" data-size="line">) in the toolbar to open the Questions Properties dialog to make any necessary changes.
