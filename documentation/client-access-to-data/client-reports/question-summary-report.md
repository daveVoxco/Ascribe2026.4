---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/client-access-to-data/client-reports/question-summary-report
---

# Question Summary Report

The Question Summary Report lists summary information about each question. You can filter the list of questions by question type. In the grey bar at the top of the window, check the boxes for the question types you want to view, and then click the Update button. The report also has additional options for showing codebooks and verbatims.

**Location**: Client/Right-click study/Select Reports/Click Question Summary

Here is the information on the Question Summary Report:

<table><thead><tr><th width="248" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Question ID</td><td valign="top">The question identification number</td></tr><tr><td valign="top">Question Label</td><td valign="top">The question label</td></tr><tr><td valign="top">Question Type</td><td valign="top">The question type</td></tr><tr><td valign="top">Layout</td><td valign="top">The data layout</td></tr><tr><td valign="top">Respondents</td><td valign="top">The number of respondents for this question; the total of all respondents is displayed at the bottom of the table.</td></tr><tr><td valign="top">Responses Coded</td><td valign="top">The number of responses coded for this question, followed by the number of responses coded as a percentage of the number of responses; the total number of responses coded and its percentage display at the bottom of the table.</td></tr><tr><td valign="top">Hours</td><td valign="top">The number of hours recorded in time accounting for this question; only administrators can view this field. The total number of hours displays at the bottom of the table.</td></tr><tr><td valign="top">Responses Per Hour</td><td valign="top">The average number of responses per hour is determined by the number of responses coded divided by the number of hours worked on this question; only administrators can view this field. The average responses coded per hour displays at the bottom of the table.</td></tr></tbody></table>

### Question Detail Report within the Question Summary Report <a href="#minitocbookmark2" id="minitocbookmark2"></a>

The Question Detail Report is used to quality check a study, approve codebooks or just check on the status of a study. You can select any number of questions to see more information.

**Location**: Client/Right-click study/Select Reports/Click Question Summary

From the Question Summary Report, click the box next to the question ID of one or more questions. Right-click the question to display these options:

<table><thead><tr><th width="298.6666259765625" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Detail This Question</td><td valign="top">Displays a detail report of the selected question. From this option, you also can display a detail report for questions that share this question. </td></tr><tr><td valign="top">Detail Selected Questions</td><td valign="top">Displays detail reports for multiple selected questions</td></tr><tr><td valign="top">Edit Question</td><td valign="top">Displays the Edit Question dialog</td></tr><tr><td valign="top">Select All</td><td valign="top">Selects all of the questions and puts a checkmark in each box</td></tr><tr><td valign="top">Clear All</td><td valign="top">Removes the checkmark from each box</td></tr><tr><td valign="top">Show Responses For This Question</td><td valign="top">Displays all of the responses for one question</td></tr><tr><td valign="top">Download Data</td><td valign="top">Navigates to Codebooks and Results or Scripted Output</td></tr><tr><td valign="top">Reports</td><td valign="top">Navigates to other reports</td></tr><tr><td valign="top">Export Table To Excel</td><td valign="top">Copies the report to Excel</td></tr></tbody></table>

The Question Detail Report has general information about the question at the top of the page. This information includes question type, number of responses loaded, number of current responses, number of responses coded, number of responses currently referred, number of codes applied, card number, column number, number of columns and data layout.

The codebook displays below the question information. The codebook information has these fields:

<table><thead><tr><th width="256" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Row</td><td valign="top">The row number for this code or net</td></tr><tr><td valign="top">Input</td><td valign="top">The input ID for the code. This value is not displayed for nets.</td></tr><tr><td valign="top">Output</td><td valign="top">The output ID for the code. This value is not displayed for nets.</td></tr><tr><td valign="top">Description</td><td valign="top">The description of the codes. Nets display in bold.</td></tr><tr><td valign="top">Number of Respondents</td><td valign="top">The top of the column shows the total number of respondents in the question. For nets, this value is the unduplicated count of respondents who had any code of this net applied. For codes, this value is the number of responses to which this code was applied.</td></tr><tr><td valign="top">Percentage Of Respondents</td><td valign="top">This column displays the percentage of respondents who had this code applied.  </td></tr></tbody></table>

If the codebook is shared and if you select _Detail this questions/with questions sharing codebook_, a column is added for each question that shares the codebook within the study. Codebooks that are shared with questions in different studies are not displayed.

You can also display responses for this question from the Question Detail Report. To view responses for a code, right-click the code and select Show responses for this code. To view all of the responses for a question, right-click anywhere in the table and select Show responses for this question.
