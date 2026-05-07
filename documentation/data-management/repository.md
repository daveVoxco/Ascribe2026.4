---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/data-management/repository
---

# Repository

_Navigate: Supervisor/Repository_

The repository stores the copies of all of your studies and saves them for later retrieval.

The repository is updated daily. At the time of the update, every study in your Ascribe account is saved to disk, just as if you had saved it manually. The saved study file contains the complete study, including all responses and codes applied. The saved study does not contain media files. If the study does not yet exist in the repository, it is added. If the study is already in the repository, the saved study file is then compared to the most recently saved version of the study in the repository. If the two versions are identical, the new copy is discarded. Otherwise, the new copy is stored in the repository.

The repository retains all versions of a study that were inserted in the repository within the last 30 days. Only the most recently saved copy of a study older than 30 days is retained. Hence the repository contains daily copies of all studies that have changed within the past 30 days, but only the most recent copy of studies that have not changed within 30 days. For studies that are not changed, over time the repository will contain a single copy of each study (the one most recently saved).

Ascribe does not delete the study from the repository.

You can retrieve a study from the repository at any time. The file can be restored to Ascribe using the [Restore Study](../study/restore-a-study.md) page.

{% hint style="info" %}
#### Note

The studies saved in the repository do not contain media files. Do not rely on the repository to retain media files for multi-media studies. If you need to retain copies of the media files in a study, you should [save the study](../study/save-a-study.md) manually.
{% endhint %}

## Display Studies

_Navigate: Supervisor/Repository_

The Repository page displays the studies in the repository. The list of the studies is sorted with the most recently saved studies at the top of the list. Black lines group copies of the same study, with the most recently saved copy at the top of the group.

## Find Box

_Navigate: Supervisor/Repository_

Use the Find box to select the studies to display. Type the text you want to search for in the Find box, and then click the Update button. (If the Find box is blank, no studies will be displayed.) Ascribe will display studies that contain this text in the study ID or study name.

The Find box also accepts a regular expression, so you can use standard regular expressions to search for your studies. To display all studies, enter a period (.) in the Find box. The period matches any character, so all studies will be displayed that have at least one character in either the ID or name.

## Show Details

_Navigate: Supervisor/Repository_

There are two views available for the repository. If the Show Details box is checked, the list contains detailed information about the studies in the repository. If this box is not checked, the list shows only the status and identification information for the studies. To change the view, click the Show Details box and click the Update button.

The study details screen has these fields:

<table><thead><tr><th width="206.66668701171875" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Row Number</td><td valign="top">Click this column header to restore the sort order to the original view.</td></tr><tr><td valign="top">Saved</td><td valign="top">The date this copy of the study was saved in the repository.</td></tr><tr><td valign="top">Status</td><td valign="top">The status shows the study’s current state of progress.</td></tr><tr><td valign="top">Study ID</td><td valign="top">The study ID, which is important for automatically sending data to Ascribe with the FTP site.</td></tr><tr><td valign="top">Study Name</td><td valign="top">The name of the study.</td></tr><tr><td valign="top">Description</td><td valign="top">Description of the study.</td></tr><tr><td valign="top">Created</td><td valign="top">The date the study originally was added to Ascribe.</td></tr><tr><td valign="top">Due Date</td><td valign="top">The due date of the study.</td></tr><tr><td valign="top">Client</td><td valign="top">The name of the client company.</td></tr><tr><td valign="top">End Customer</td><td valign="top">The name of the end customer.</td></tr><tr><td valign="top">Supervisor</td><td valign="top">The username of the supervisor for this study.</td></tr><tr><td valign="top">Questions</td><td valign="top">The number of questions in the study.</td></tr><tr><td valign="top">Respondents</td><td valign="top">The number of unique respondents.</td></tr><tr><td valign="top">Responses</td><td valign="top">The number of responses to all questions.</td></tr><tr><td valign="top">Responses Coded</td><td valign="top">The number of coded responses.</td></tr><tr><td valign="top">Loads</td><td valign="top">The number of loads.</td></tr><tr><td valign="top">Hours</td><td valign="top">The number of work hours spent on this study, taken from the time accounting records.</td></tr></tbody></table>

All of your studies currently in Ascribe are saved and placed in the repository each weekend. If the study is already in the repository and has changed, the new copy of the study is also stored. This gives you a weekly "snapshot" of all of your studies.

## Download a Study from the Repository

_Navigate: Supervisor/Repository_

Right-click a study and select "Download file..." from the menu, or click the link in the "Saved" column.

## View the Questions in the Repository

_Navigate: Supervisor/Repository_

Right-click a study and select Questions from the menu.
