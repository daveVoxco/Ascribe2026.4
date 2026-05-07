---
description: >-
  The Study Details dialog lets users manage study properties, track coding
  progress with estimates, view questions, assign coders to questions, and
  monitor data loads for survey coding projects.
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/study/study-details-dialog
---

# Study Details Dialog

<figure><img src="../../.gitbook/assets/image (95).png" alt=""><figcaption></figcaption></figure>

**Study Details dialog tabs**:

* [Properties](study-details-dialog.md#minitocbookmark2) - study properties
* [Progress](study-details-dialog.md#minitocbookmark3) - statics about progress
* [Questions](study-details-dialog.md#minitocbookmark7) - study questions
* [Coders](study-details-dialog.md#minitocbookmark8) - assign or edit coders
* [Loads](study-details-dialog.md#minitocbookmark9) - information about data loads for the study

## Study Properties <a href="#minitocbookmark2" id="minitocbookmark2"></a>

The Properties tab contains all property information about the study. Every field can be edited.

<figure><img src="../../.gitbook/assets/image (97).png" alt=""><figcaption><p>Study Details Dialog - Properties tab</p></figcaption></figure>

<table><thead><tr><th width="213.66668701171875" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Study ID</td><td valign="top">The unique identifier for the study</td></tr><tr><td valign="top">Study Name</td><td valign="top">Name of the study</td></tr><tr><td valign="top">Description</td><td valign="top">Text to explain or identify the study</td></tr><tr><td valign="top">Help on This Study</td><td valign="top">Enter information about the study</td></tr><tr><td valign="top">Study Status</td><td valign="top"><p>Has the following options:</p><ul><li><strong>Under Construction</strong> - The study is not ready to code. Use this status while you prepare a study. For example, use this status if the data or the codebooks are not ready. The study will not appear on the Studies in Progress page or Studies to Transcribe page. Studies restored as New have a default status of Under Construction.</li><li><strong>In Progress</strong> - The study is ready to code or the coding has started. The study can be accessed from the Studies in Progress page or the Studies to Transcribe page (or any page).</li><li><strong>On Hold</strong> - The study cannot be accessed from the Studies in Progress page, the Studies to Transcribe page or the Studies to Translate page. There may be a problem or a change to the study, and all work should be stopped until the problems are resolved.</li><li><strong>Review in Progress</strong> - Use this status while the user does a quality check of the study. For example, use when the codes are checked for accuracy or low mentions. The study cannot be accessed from the Studies in Progress page, the Studies to Transcribe page, or the Studies to Translate page. Also, you can use this status when you create or deliver study output.</li><li><strong>Complete</strong> - The study is complete; data is ready to be downloaded for analysis.</li><li><strong>Archived</strong> - The study is removed from all lists of active studies. If study shipping is enabled, all archived studies are sent to your FTP site on the Saturday after the status is changed to archived. At that time, the study is deleted from Ascribe. You can see a list of studies that have been shipped to your FTP site under Supervisor/Shipped Studies.</li></ul></td></tr><tr><td valign="top">Supervisor</td><td valign="top">Select the supervisor assigned to the study</td></tr><tr><td valign="top">Client</td><td valign="top">Select the company who requested the study</td></tr><tr><td valign="top">End Customer</td><td valign="top">Select the company who requested the study</td></tr><tr><td valign="top">Start Date</td><td valign="top"><p><strong>There are two ways to set dates. You can enter a date in MM/DD/YYYY format or use the calendar. (You can also set the Start Date on the Studies page.)</strong></p><p><strong>To set or edit the start date,</strong> enter the date in MM/DD/YYYY format in the text box. Or, you can click the drop-down arrow to display the calendar, and click the appropriate day on the calendar. After you select a day, the text box displays the date.</p><p><strong>To change the start date,</strong> click the text box and enter a new date in MM/DD/YYYY format. Or, you can click the text box, and click a date on the calendar.</p><p><strong>To display another the month on the calendar,</strong> click the backward or forward arrows next to the calendar header. Or click the calendar header to display a list of months. Click the header a second time to display a list of years.</p></td></tr><tr><td valign="top">Due Date</td><td valign="top"><p><strong>There are two ways to set dates. You can enter a date in MM/DD/YYYY format or use the calendar. (You can also set the Due Date from the Studies Page.)</strong></p><p><strong>To set or edit a due date,</strong> click the text box and enter the date in MM/DD/YYYY format.  Or, you can click the drop-down arrow to display the calendar, and click the appropriate day on the calendar. After you select a day, the text box displays the date.</p><p><strong>To display another the month on the calendar,</strong> click the backward or forward arrows next to the calendar header. Or click the calendar header to display a list of months. Click the header a second time to display a list of years.</p></td></tr><tr><td valign="top">Quota</td><td valign="top">The quota for the study</td></tr><tr><td valign="top">File Format</td><td valign="top"><p>Options are:</p><ul><li>Binary: Write a binary file in 1130 binary format </li><li>ASCII: Write an ASCII (text) file. If you use column binary output, you will almost always want ASCII format.</li></ul></td></tr><tr><td valign="top">Layout</td><td valign="top"><p>See Layout Types for more information. Options are:</p><ul><li>Punch: Write column binary data using punch format</li><li>Numeric: Write column binary data using numeric format</li><li>Punch Using Column Offset: Compute the column for the punch by adding the code column to the question column</li><li>Use Question Settings: Use the layout setting specified in each question. This setting allows you to mix data formats among different questions.</li></ul></td></tr><tr><td valign="top">Columns Per Card/Respondent</td><td valign="top">The value specifies the number of columns (in characters) in each data record written to the output file. In column binary format, these records are called cards.</td></tr><tr><td valign="top">Card Number Column</td><td valign="top">The value specifies the location of the card number on the card. The value 1 means the first column on the card.</td></tr><tr><td valign="top">Card Number Columns</td><td valign="top">The value specifies the number of columns used to write the card number on the card. The card number is left filled with 0's when written.</td></tr><tr><td valign="top">Respondent ID Column</td><td valign="top">The value specifies the location of the respondent ID on the card. The value 1 means the first column on the card.</td></tr><tr><td valign="top">Respondent ID Columns</td><td valign="top">The value specifies the number of columns used to write the respondent ID on the card. The respondent ID is left filled with 0's when written.</td></tr><tr><td valign="top">Help on This Study</td><td valign="top">Enter information about the study. You can view this information from the Coder Window when you right-click in the codebook pane and select Question info.</td></tr></tbody></table>

## Progress <a href="#minitocbookmark3" id="minitocbookmark3"></a>

This tab displays several graphs for the progress of the study; this tab only displays for users with administrator or supervisor privilege.

<figure><img src="../../.gitbook/assets/image (98).png" alt=""><figcaption><p>Study Details Dialog - Progress tab</p></figcaption></figure>

<table><thead><tr><th width="213" valign="top">Graph</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Summary</td><td valign="top"><ul><li>Tasks - The percentage completion of questions marked with Code, Transcribe, and Translate tasks.</li><li>Question Type - The percentage completion of coding by question type, for questions marked with the Code task</li><li>Responses Coded - The total number of responses and the number of coded responses by question type, for questions marked with the Code task</li></ul></td></tr><tr><td valign="top">Estimates</td><td valign="top"><p>Overall estimates of codes per hour and hours remaining for Open and Other Specify questions, by those types, for questions marked with the Code task.</p><p>See <a href="study-details-dialog.md#minitocbookmark4">Coding Estimates</a> for a detailed explanation of the calculations.</p></td></tr><tr><td valign="top">Questions</td><td valign="top">Displays the percent coded, counts of coded responses, and estimates by question for questions marked with the Code task.</td></tr></tbody></table>

## Coding Estimates <a href="#minitocbookmark4" id="minitocbookmark4"></a>

The first thing to understand about the coding estimates is that they are just that: estimates. We are trying to estimate the past productivity on coding and the future time that the work will be completed. There are many factors that make these estimates imprecise.

**Examples**:

* Do we include responses coded by the machine in the calculation? This includes coding duplicate responses. If we code one response and that causes 10 duplicates to be coded, is that one response or 10 in our calculation?
* Coders might get interrupted as they work. We cannot know that the coder was not staring at the screen but was chatting with a friend. Does the chat time count in our calculation of responses per hour?
* And so on...

Given these factors, the best approach is to err on the side of simplicity. This allows us to explain what the numbers mean so the user can best decide whether to rely on the numbers for a given job or not.

### Responses per Hour <a href="#minitocbookmark5" id="minitocbookmark5"></a>

We work here with information associated with each code applied to a response:

* The response that was coded, and from that the question
* The user’s session
* The timestamp: the exact date and time the code was applied.

Also important to understand is that all codes applied to in a single operation in Coder are given the same timestamp. This is also what supports the “undo last codes applied” operation in Coder. The set of codes removed by the undo is the same set of codes we are talking about as “applied in a single operation”.

Note that we are not using any of the time accounting information.

The basic operation we are going to do is try to figure out how much time it took for the user to code a response. We assume that the amount of time is the difference between the timestamp of that code and the timestamp of the last code the user applied. We cannot tell anything from a single timestamp. To get an interval of time, we need to take the difference between two timestamps.

Now, to calculate the responses per hour for a question we do this:

First, we get all the applied codes that were not applied by the \_loader user and have a session and timestamp. This omits codes applied at load time, and codes applied by restoring a study.

Next, we divide these applied codes by session. We need to look at the sessions individually, so that we can figure out the time intervals for this user, not for all users who may be coding the question.

Next, we sort the session codes by timestamp. As we scan down the list, we can now see the interval of time between successive codes. We simply sum up those intervals and divide by the number of intervals to get the average time required to apply a single code.

If you are following closely, you will note that if our list has ten codes, we only have nine intervals. We cannot give an estimate for the time it took for the user to apply the first code in the list. Another way to look at this is that if the user applied only one code in the session, there is no way to determine how long that took.

Now we have the number of codes applied per unit time for this session. If our time units are hours, we can write this as C/hr, codes per hour. Clearly, we can now look across all the sessions, and get an average C/hr for all sessions.

That took a lot of words. To state this succinctly we can simply say that C/hr is the average time interval between successively applied codes.

C/hr includes all codes applied, like automatically coded duplicates. This is an interesting number and gives an estimate of true worker productivity. Still, it does not give us insight into how long the coder took to figure out how to code the next response. For that, we want to remove codes applied automatically. That is easy. Instead of counting all the time intervals between codes, we count only those intervals that are not zero. This gives the time interval between coding operations in Coder. We can call this alternative value Manual C/hr.

Armed with our two codes per hour numbers, we can calculate responses per hour by simply multiplying by the average number of codes applied to a response. Now we have estimates R/hr and Manual R/hr. These are the numbers displayed in those columns on the questions page, and in tooltips.

So, to give the quick statement of R/hr, we say that it is the average time interval between successively applied codes multiplied by the average number of codes per response.

The Manual R/hr is the same, except that we count codes applied at the same time as a single code. &#x20;

Note: when double arrows display in the R/hr column, this means over 100,000 responses per hour are estimated. Coding was probably done in an automated way.

### Hours to completion <a href="#minitocbookmark6" id="minitocbookmark6"></a>

Going from responses per hour to hours to complete coding is easy. We just divide the number of uncoded responses by Manual R/hr. Note that we use the manual number here, not the one that includes duplicate coding. This is a conservative number that is probably too high when starting coding, but more accurate when finishing coding. This is because we can assume that as the project nears completion there will be few duplicates remaining to code.

## Questions <a href="#minitocbookmark7" id="minitocbookmark7"></a>

This tab displays a table of all questions in the study. It provides all information contained on the Questions page, without the need to navigate to that page.

<figure><img src="../../.gitbook/assets/image (99).png" alt=""><figcaption><p>Study Details Dialog - Questions tab</p></figcaption></figure>

The table is read-only, but does provide a link to the Questions Details popup. This allows the operations in that popup, without the need to navigate away from the Studies page.

## Coders <a href="#minitocbookmark8" id="minitocbookmark8"></a>

This tab, which only displays for users with administrator or supervisor privilege, allows viewing and changing the assignment of coders to questions. Coders appear on the left, and questions on the right.<br>

<figure><img src="../../.gitbook/assets/image (100).png" alt=""><figcaption><p>Study Details Dialog - Coders tab</p></figcaption></figure>

**Assign coders:** select the coder or coders and then select the question or questions. Click the Set Coders for Selected Questions button to assign the coders. The assigned coders display in the Coders column on the Studies page and the Assigned To column on the Questions page.

**View the assigned coders:** click the down arrow next to the question.

**Change coders assignment:** select the appropriate coders and select the question. Click the Set Coders for Selected Questions button. Only the selected coders are assigned.&#x20;

**Remove all coders from question(s)**: select the question(s) and click the Clear Coders from Selected Questions button.&#x20;

## Loads <a href="#minitocbookmark9" id="minitocbookmark9"></a>

This tab only displays for users with administrator or supervisor privilege. The top table lists the loads for the study. In the case of automated loads by FTP, many study loads will result in no responses loaded. The table can be filtered by the Questions or Responses Loaded column if desired to show only those loads that added responses. The table allows selection of one or more loads by checking the row selector checkbox.

<figure><img src="../../.gitbook/assets/image (101).png" alt=""><figcaption><p>Study Details Dialog - Loads tab</p></figcaption></figure>

The lower table lists the questions that had responses loaded in the loads selected in the upper table. If more than one load is selected in the upper table, there may be more than one load displayed in the lower table for a given question, up to one for each study load selected. One or more question loads can be deleted by selecting them and clicking Delete Selected Question Loads. If you select all questions, then the entire load is deleted (meaning all responses for the load are deleted, the load will still appear in the upper table, but with no responses loaded).
