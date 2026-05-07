---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/data-management/job-properties-and-parameters
---

# Job Properties and Parameters

The Properties dialog has these fields:

<table><thead><tr><th width="195.3333740234375" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Job Type</td><td valign="top"><p><strong>Save study -</strong> Indicates a study was saved from the Ascribe™ software. Right-click "save study" to download the saved study.</p><p><strong>Restore study -</strong> Indicates a study was restored from a zipped .XML file (usually a file that originally was saved from Ascribe™.) Check the file name to see the original study ID and name ( studyid_name).</p><p><strong>Load from Ascribe -</strong> Indicates a file has been manually loaded into Ascribe from the "Load data/process file" option on the Supervisor/Studies page.</p><p><strong>Load from FTP -</strong> A data file (or setup file) has been loaded via an FTP site. The user should be "_loader" in these instances.</p><p><strong>Merge Study -</strong> A study was merged with a previous study. The previous study is indicated by the file name.</p><p><strong>Scripted Output -</strong> A scripted output has been run on a study. To see which study, right-click and select parameters. The type of scripted output ran is indicated in the "file" field (user defined is considered a scripted output here.)</p></td></tr><tr><td valign="top">Job Status</td><td valign="top"><p><strong>Queued -</strong> The job has been created, but execution of the job has not yet begun. Only one job can be active at a given time.</p><p><strong>Running -</strong> The job is running.</p><p><strong>Paused -</strong> The job is paused awaiting action from you.</p><p><strong>Completed -</strong> The job has completed. If the job completed with an error, the row will be red.</p></td></tr><tr><td valign="top">Job Schedule</td><td valign="top">Displays the name of the job if it has been added to the <a href="schedule-jobs.md">job schedule</a>.</td></tr><tr><td valign="top">User Name</td><td valign="top">The user who started the job.</td></tr><tr><td valign="top">Time Created</td><td valign="top">Actual time a job was submitted.</td></tr><tr><td valign="top">Time Started</td><td valign="top">Time a job began running.</td></tr><tr><td valign="top">Time Completed</td><td valign="top">Time a job finished running.</td></tr><tr><td valign="top">Total Time (Seconds)</td><td valign="top">Time from submission of job to completion (includes queued time.)</td></tr><tr><td valign="top">Run Time (Seconds)</td><td valign="top">Time the job took to run.</td></tr><tr><td valign="top">File Name</td><td valign="top">Name of the file loaded or the script that was run.</td></tr><tr><td valign="top">Message</td><td valign="top">Log field for reporting information.</td></tr><tr><td valign="top">Error</td><td valign="top">Displays the error that caused the job to fail (see <a href="../error-messages.md">Error Messages</a> or email support@goascribe.com for help in troubleshooting failed jobs.)</td></tr></tbody></table>

## Parameters

The Parameters screen has these fields:

<table><thead><tr><th width="203.333251953125" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Script</td><td valign="top">Script name</td></tr><tr><td valign="top">Study</td><td valign="top">Study ID and study name</td></tr><tr><td valign="top">Questions</td><td valign="top">Question IDs and labels for those questions selected for output</td></tr><tr><td valign="top">Parameters</td><td valign="top">Some custom scripts are based on information entered by the user. (See Auto-Coder Script for an example of a script that requires parameters.)</td></tr></tbody></table>

## Schedule Job

See[ Schedule Jobs](schedule-jobs.md) for more information.
