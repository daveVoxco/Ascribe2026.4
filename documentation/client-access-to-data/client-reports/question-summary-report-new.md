---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/client-access-to-data/client-reports/question-summary-report-new
---

# Question Summary Report (New)

The Question Summary Report lists summary information about each question. You can filter the list of questions by question type. In the grey bar at the top of the window, check the boxes for the question types you want to view, and then click the Update button. The report also has additional options for showing codebooks and verbatims.

<figure><img src="../../../.gitbook/assets/image (329).png" alt=""><figcaption></figcaption></figure>

**Location**: Right-click a Study > Reports > Question Summary (New)

## **Question Summary Report fields**:

<table><thead><tr><th width="248" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Question ID</td><td valign="top">The question identification number</td></tr><tr><td valign="top">Question Label</td><td valign="top">The question label</td></tr><tr><td valign="top">Question Type</td><td valign="top">The question type</td></tr><tr><td valign="top">Layout</td><td valign="top">The data layout</td></tr><tr><td valign="top">Respondents</td><td valign="top">The number of respondents for this question; the total of all respondents is displayed at the bottom of the table.</td></tr><tr><td valign="top">Responses Coded</td><td valign="top">The number of responses coded for this question, followed by the number of responses coded as a percentage of the number of responses; the total number of responses coded and its percentage display at the bottom of the table.</td></tr><tr><td valign="top">Hours</td><td valign="top">The number of hours recorded in time accounting for this question; only administrators can view this field. The total number of hours displays at the bottom of the table.</td></tr><tr><td valign="top">Responses Per Hour</td><td valign="top">The average number of responses per hour is determined by the number of responses coded divided by the number of hours worked on this question; only administrators can view this field. The average responses coded per hour displays at the bottom of the table.</td></tr></tbody></table>

## **Sub reports and tools**

<table><thead><tr><th width="298.6666259765625" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top"><strong>Detail This Question</strong></td><td valign="top">Displays a detail report of the selected question. From this option, you also can display a detail report for questions that share this question. <br><strong>See</strong>: <a data-mention href="question-summary-report-new.md#question-detail-reports">#question-detail-reports</a></td></tr><tr><td valign="top"><strong>Detail Selected Questions</strong></td><td valign="top">Displays detail reports for multiple selected questions.<br><strong>See</strong>: <a data-mention href="question-summary-report-new.md#question-detail-reports">#question-detail-reports</a></td></tr><tr><td valign="top"><strong>Edit Question</strong></td><td valign="top">Displays the Edit Question dialog.</td></tr><tr><td valign="top"><strong>Select All</strong></td><td valign="top">Selects all of the questions and puts a checkmark in each box.</td></tr><tr><td valign="top"><strong>Clear All</strong></td><td valign="top">Removes the checkmark from each box.</td></tr><tr><td valign="top"><strong>Show Responses For This Question</strong></td><td valign="top">Displays all of the responses for one question.</td></tr><tr><td valign="top"><strong>Download Data</strong></td><td valign="top">Navigates to Codebooks and Results or Scripted Output.</td></tr><tr><td valign="top"><strong>Reports</strong></td><td valign="top">Navigates to other reports.</td></tr><tr><td valign="top"><strong>Export Table To Excel</strong></td><td valign="top">Copies the report to Excel.</td></tr></tbody></table>

### **Question detail reports**

Right click on a question in the report to access sub-reports that display general information about one or more question(s).

<figure><img src="../../../.gitbook/assets/image (333).png" alt=""><figcaption></figcaption></figure>

**Location(s)**:&#x20;

* Right-click question > Detail this question > (sub menu options)
* Check multiple questions > Right-click question > Detail selected questions

<figure><img src="../../../.gitbook/assets/image (335).png" alt=""><figcaption></figcaption></figure>

**Detail reports header information**

This view displays the following metrics:

* **Question Type**: Type of question
* **Response Counts**:
  * Total loaded
  * Current count
  * Number coded
  * Number currently referred
* **Coding Activity**: Total codes applied
* **Data Specifications**:
  * Card and column numbers
  * Total column count
  * General data layout

**Table fields**:

<table><thead><tr><th width="256" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Row</td><td valign="top">The row number for this code or net</td></tr><tr><td valign="top">Input</td><td valign="top">The input ID for the code. This value is not displayed for nets.</td></tr><tr><td valign="top">Output</td><td valign="top">The output ID for the code. This value is not displayed for nets.</td></tr><tr><td valign="top">Description</td><td valign="top">The description of the codes. Nets display in bold.</td></tr><tr><td valign="top">Number of Respondents</td><td valign="top">The top of the column shows the total number of respondents in the question. For nets, this value is the unduplicated count of respondents who had any code of this net applied. For codes, this value is the number of responses to which this code was applied.</td></tr><tr><td valign="top">Percentage Of Respondents</td><td valign="top">This column displays the percentage of respondents who had this code applied.  </td></tr></tbody></table>

### With questions sharing codebook

If a codebook is shared within the current study, select **Detail this question** > **with questions sharing codebook**.

<figure><img src="../../../.gitbook/assets/image (334).png" alt=""><figcaption></figcaption></figure>

* **Result**: A new column is added for every question using this codebook.

{% hint style="info" %}
#### Note

Questions from _other_ studies are not shown.
{% endhint %}

### Viewing Responses

<figure><img src="../../../.gitbook/assets/image (332).png" alt=""><figcaption></figcaption></figure>

You can view response data directly from the Question Detail Report:

* **For a specific code**: Right-click the code > Select Show responses for this code
* **For the entire question**: Right-click anywhere in the table > Select Show responses for this question
