---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/data-management/how-to-load-data/load-details
---

# Load Details

_Navigate: Supervisor/Loads/Right-click a load/Select Load Details_\
_Jobs/Right-click a job/Right-click a load/Select Load Details_

The Load Details screen displays the result of a load on a question by question basis.

To delete responses from a question, right-click the question and select Delete. This action deletes all responses for the selected question which were loaded from the file on the date and time indicated.

The Load Details screen has these fields:

<table><thead><tr><th width="236.6666259765625" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Question ID</td><td valign="top">When you load data to an existing study, the question ID of the new load must match exactly the question ID of the existing study. The match is case insensitive.</td></tr><tr><td valign="top">Question Label</td><td valign="top">The question label.</td></tr><tr><td valign="top">Responses Processed</td><td valign="top">The number of responses that have been processed from the load file.</td></tr><tr><td valign="top">Responses Loaded</td><td valign="top">The number of responses added to the study from this load.</td></tr><tr><td valign="top">Blank Responses (Ignored)</td><td valign="top">Responses are ignored if they contain no data.</td></tr><tr><td valign="top">Loaded Previously</td><td valign="top">Responses are skipped if they are already loaded. Responses are skipped if you try to load a question ID/respondent ID that has been loaded previously.</td></tr><tr><td valign="top">Responses Combined</td><td valign="top">If there are responses from the same respondent to the same question, these responses are combined into a single response. The responses are separated by the ‘|’ character. </td></tr><tr><td valign="top">Auto-Coded in Load</td><td valign="top">The number of responses that were auto-coded during this load.</td></tr></tbody></table>
