---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/data-management/manage-jobs
---

# Manage Jobs



Ascribe is able to perform certain jobs for you while you are working on other things. This report shows you these jobs, their status (such as running), and the result.

<figure><img src="../../.gitbook/assets/image (363).png" alt=""><figcaption></figcaption></figure>



Jobs are processed in the order they are submitted. With the exception of scripted output jobs, only one job will run at a time in a given Ascribe account. This is because a job may depend on the completion of a previous job for it to execute properly. For example, you may restore a study as a template for a new study (as job 1), then load data to the new study (as job 2). Clearly job 2 cannot run at the same time as job 1. By ensuring that jobs run in the same order they are submitted, Ascribe allows you to start multiple jobs in a logical sequence without waiting for the completion of the jobs started first.

Scripted output jobs will not start while another type of job is running. However, once a scripted output job is running, it will not prevent other jobs from starting (including other scripted output jobs).

**Location**: Menu > JOBS > Jobs

<details>

<summary>Navigation menu</summary>

<figure><img src="../../.gitbook/assets/image (364).png" alt=""><figcaption></figcaption></figure>

</details>

## Page Layout <a href="#minitocbookmark2" id="minitocbookmark2"></a>

The page has this format: black title bar with a toolbar underneath, followed by the Refresh button and date range display, and the grid of jobs.

## Title Bar <a href="#minitocbookmark3" id="minitocbookmark3"></a>

<table><thead><tr><th width="222.6666259765625" align="center" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/Studies_page_navigation_icon.png" alt=""></p><p>Navigation Icon</p></td><td valign="top">Click the icon to navigate to other pages in Ascribe. The page behind the menu is blurred if the browser supports this action. Click anywhere in the black or off the menu to close it. If the current page is displayed in the menu, it has an arrow in front of it. Links appear in the menu only if the user has privilege to navigate to the page.</td></tr><tr><td align="center" valign="top">Page Name</td><td valign="top">Self-explanatory</td></tr><tr><td align="center" valign="top">Ascribe Coder Logo</td><td valign="top">Acts as the one-click navigation option to the page you selected in <a href="../get-started/customization-features/user-options.md#user-options-and-single-sign-on">User Options</a></td></tr><tr><td align="center" valign="top">Account</td><td valign="top">The account you're logged into</td></tr><tr><td align="center" valign="top">User</td><td valign="top">User name has a drop-down list of options: navigate to User Options, open and submit a support request, and logout</td></tr><tr><td align="center" valign="top">Browser Language</td><td valign="top">This field indicates what language your browser is using.</td></tr><tr><td align="center" valign="top">Session Time</td><td valign="top">The duration of the user's session is displayed in HH:MM format</td></tr><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/help_icon_jan2022.jpg" alt=""></p><p>Online Help and Guides</p></td><td valign="top">The drop-down list contains options for Ascribe Help (the online help system) and interactive guides for the page.</td></tr></tbody></table>

## Date Range <a href="#minitocbookmark4" id="minitocbookmark4"></a>

Use the drop-down arrow to display a calendar where you can select beginning and ending dates. Or you can click the subheadings of Today, Yesterday, etc., to set the calendar.&#x20;

<figure><img src="../../.gitbook/assets/image (368).png" alt="" width="563"><figcaption></figcaption></figure>

When Use Local Time is toggled on, the Create Date field displays time according to your browser. When it is off, UTC time is displayed.

## Grid <a href="#minitocbookmark5" id="minitocbookmark5"></a>

The columns in the grid of responses are controlled through the [Table Manager](../study/table-manager.md). Choose what fields display, such as job type, study ID, and user.&#x20;

<figure><img src="../../.gitbook/assets/image (366).png" alt="" width="563"><figcaption></figcaption></figure>

To see only jobs that you started, sort the User column or use the filter to select only your user name.&#x20;

**Columns**:

<table><thead><tr><th width="203.3333740234375" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Job Type</td><td valign="top"><p><strong>Save study -</strong> Indicates a study was saved from the Ascribe software. Right-click "save study" to download the saved study.</p><p><strong>Restore study -</strong> Indicates a study was restored from a zipped .XML file (usually a file that originally was saved from Ascribe.) Check the file name to see the original study ID and name (studyid_name).</p><p><strong>Load from Ascribe -</strong> Indicates a file has been manually loaded into Ascribe from the "Load data/process file" option on the Supervisor/Studies page.</p><p><strong>Load from FTP -</strong> A data file (or setup file) has been loaded via an FTP site. The user should be "_loader" in these instances.</p><p><strong>Merge Study -</strong> A study was merged with a previous study. The previous study is indicated by the file name.</p><p><strong>Scripted Output -</strong> A scripted output has been run on a study. To see which study, right-click and select parameters. The type of scripted output ran is indicated in the "file" field (user defined is considered a scripted output here.)<br><strong>AI Coder</strong> - Indicates that an AI Coder analysis was run on the study.</p></td></tr><tr><td valign="top">Job Status</td><td valign="top"><p><strong>Queued -</strong> The job has been created, but execution of the job has not yet begun. Only one job can be active at a given time.</p><p><strong>Running -</strong> The job is running.</p><p><strong>Paused -</strong> The job is paused awaiting action from you.</p><p><strong>Completed -</strong> The job has completed. If the job completed with an error, the row will be red.</p></td></tr><tr><td valign="top">File Name</td><td valign="top">The name of the file submitted to the job. For scripted output jobs, this is the name of the script.</td></tr><tr><td valign="top">User Name</td><td valign="top">The user who started the job.</td></tr><tr><td valign="top">Create Date</td><td valign="top">The time the job was created. This is not necessarily the time that the job began execution since a job may need to wait for other jobs to complete.</td></tr><tr><td valign="top">Seconds</td><td valign="top">The number of seconds that the job has run (or took to run if the job is complete.)</td></tr></tbody></table>

## View Detailed Information about a Job <a href="#minitocbookmark6" id="minitocbookmark6"></a>

Right-click the job and select **Show Details** from the menu, or double-click the job. The dialog box displayed contains information about the execution of the job.

<figure><img src="../../.gitbook/assets/image (365).png" alt="" width="563"><figcaption></figcaption></figure>

**Window**:

<figure><img src="../../.gitbook/assets/image (369).png" alt=""><figcaption></figcaption></figure>

**Tabs**:

{% tabs %}
{% tab title="Properties" %}
The Properties screen has these fields:

<table><thead><tr><th width="197.99993896484375" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Job Type</td><td valign="top"><p><strong>Save study -</strong> Indicates a study was saved from the Ascribe™ software. Right-click "save study" to download the saved study.</p><p><strong>Restore study -</strong> Indicates a study was restored from a zipped .XML file (usually a file that originally was saved from Ascribe™.) Check the file name to see the original study ID and name ( studyid_name).</p><p><strong>Load from Ascribe -</strong> Indicates a file has been manually loaded into Ascribe from the "Load data/process file" option on the Supervisor/Studies page.</p><p><strong>Load from FTP -</strong> A data file (or setup file) has been loaded via an FTP site. The user should be "_loader" in these instances.</p><p><strong>Merge Study -</strong> A study was merged with a previous study. The previous study is indicated by the file name.</p><p><strong>Scripted Output -</strong> A scripted output has been run on a study. To see which study, right-click and select parameters. The type of scripted output ran is indicated in the "file" field (user defined is considered a scripted output here.)</p></td></tr><tr><td valign="top">Job Status</td><td valign="top"><p><strong>Queued -</strong> The job has been created, but execution of the job has not yet begun. Only one job can be active at a given time.</p><p><strong>Running -</strong> The job is running.</p><p><strong>Paused -</strong> The job is paused awaiting action from you.</p><p><strong>Completed -</strong> The job has completed. If the job completed with an error, the row will be red.</p></td></tr><tr><td valign="top">Job Schedule</td><td valign="top">Displays the name of the job if it has been added to the <a href="schedule-jobs.md">job schedule</a>.</td></tr><tr><td valign="top">User Name</td><td valign="top">The user who started the job.</td></tr><tr><td valign="top">Time Created</td><td valign="top">Actual time a job was submitted.</td></tr><tr><td valign="top">Time Started</td><td valign="top">Time a job began running.</td></tr><tr><td valign="top">Time Completed</td><td valign="top">Time a job finished running.</td></tr><tr><td valign="top">Total Time (Seconds)</td><td valign="top">Time from submission of job to completion (includes queued time.)</td></tr><tr><td valign="top">Run Time (Seconds)</td><td valign="top">Time the job took to run.</td></tr><tr><td valign="top">File Name</td><td valign="top">Name of the file loaded or the script that was run.</td></tr><tr><td valign="top">Message</td><td valign="top">Log field for reporting information.</td></tr><tr><td valign="top">Error</td><td valign="top">Displays the error that caused the job to fail (see <a href="../error-messages.md">Error Messages</a> or email support@goascribe.com for help in troubleshooting failed jobs.)</td></tr></tbody></table>


{% endtab %}

{% tab title="Parameters" %}
## View Parameters for Scripted Output Jobs <a href="#minitocbookmark7" id="minitocbookmark7"></a>

Right-click the job, and then select **Show Details** from the menu and then click the **Parameters** tab. This menu item is available for scripted output jobs only. The dialog box displays the information passed to the job when it was started.

The Parameters screen has these fields:

<table><thead><tr><th width="198.6666259765625" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Script</td><td valign="top">Script name</td></tr><tr><td valign="top">Study</td><td valign="top">Study ID and study name</td></tr><tr><td valign="top">Questions</td><td valign="top">Question IDs and labels for those questions selected for output</td></tr><tr><td valign="top">Parameters</td><td valign="top">Some custom scripts are based on information entered by the user. (See Auto-Coder Script for an example of a script that requires parameters.)</td></tr></tbody></table>
{% endtab %}
{% endtabs %}

## Download the Results of a Job <a href="#minitocbookmark8" id="minitocbookmark8"></a>

If a job created an output file (such as a scripted output job, or a save study job), you can retrieve the file. Right-click the job, and select Download File.

<figure><img src="../../.gitbook/assets/image (370).png" alt="" width="563"><figcaption></figcaption></figure>

The files created by jobs are not saved indefinitely. The files are available for about a week from the time the job was run.

If the Download menu item is grayed out, the file is no longer available for download.

## Resume a Paused Job <a href="#minitocbookmark9" id="minitocbookmark9"></a>

Certain jobs can pause while awaiting user input. If a job has paused, you can cause it to resume execution. Right-click the paused job. Then select Resume from the menu. This menu item is available only to users with supervisor privilege.

<figure><img src="../../.gitbook/assets/image (371).png" alt="" width="563"><figcaption></figcaption></figure>

Paused jobs will not remain paused indefinitely. If you have not resumed execution of a paused job after about a day, the job will abort.
