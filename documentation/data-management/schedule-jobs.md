---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/data-management/schedule-jobs
---

# Schedule Jobs

_Navigate: General/Jobs/Right-click job/Select Schedule Job_

Users with supervisor privilege can schedule certain types of jobs to run again automatically on a job schedule. To create a schedule for a job, navigate to the Jobs page, right-click the job and select Schedule Job from the menu. Click the OK button, and the Job Schedules dialog displays.

The fields on the Job Schedules dialog control when the job will run. The dialog has these fields:

<table><thead><tr><th width="202.66668701171875" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">ID</td><td valign="top">The ID defaults to the name of the script, but you can change it.</td></tr><tr><td valign="top">Enable</td><td valign="top">Check the Enabled box if you want this Job to run on schedule. If the Enabled box is not checked the schedule is not active, and jobs will not run automatically based on this schedule. You can, however, run jobs that are not enabled by using the <em>Run now</em> command from the Job schedules window.</td></tr><tr><td valign="top">Description</td><td valign="top">Describe the job for future reference; this field is optional. The description will appear as hover help for the job schedule.</td></tr><tr><td valign="top">UTC</td><td valign="top">By default, the date and times shown in the dialog box are in Universal Coordinated Time (UTC), also known as Greenwich Mean Time. You can clear the UTC check box to change the start and end date/time values to your local time zone. If you are working in a team environment across time zones, we recommend that you use the UTC view of the schedule. This view will be the same for any team member who looks at the schedule, regardless of the time zone that person is in.</td></tr><tr><td valign="top">Start Time</td><td valign="top">Enter the start time for the job to run.</td></tr><tr><td valign="top">End Time</td><td valign="top">Enter the end time of the job.</td></tr><tr><td valign="top">Occurrence</td><td valign="top"><p>Use the drop-down arrow to set the occurrence of your job:</p><p><a href="schedule-jobs.md#set-up-a-daily-schedule">Daily</a> - The job runs every N days beginning at the start date and time, where N is the value specified in the Every ... day(s) box.</p><p><a href="schedule-jobs.md#set-up-a-weekly-schedule">Weekly</a> - The job runs every N weeks beginning at the start date and time, where N is the value specified in the Every ... week(s) box. The job runs only on the days of the week selected by the check boxes at the right of the dialog.</p><p><a href="schedule-jobs.md#set-up-a-monthly-schedule">Monthly</a> - The job runs monthly, in the months specified in the check boxes at the right of the dialog. The job runs on the day of the month specified by the start date, and at the time specified by the start time.</p></td></tr><tr><td valign="top">Calendars</td><td valign="top">Use the calendars to choose the start and end date.</td></tr><tr><td valign="top">Every …Day(s)</td><td valign="top">Set the number of days between jobs. For example, to run the job every other day, enter the value 2. The minimum allowed value is 1, and the maximum is 365.</td></tr><tr><td valign="top">Repeat &#x26; Every…Minutes For…Minutes</td><td valign="top">If you want the job to repeat on a given day, check the Repeat box and set the number of minutes between jobs, and the length of time you want to continue the repetitions. The minimum value allowed in each of these boxes is 10, and the maximum 1440. The value in the For ... minutes box must not be less than that in the Every ... minutes box.</td></tr></tbody></table>

A scheduled job will run only if all of the following conditions are true:

* The schedule is enabled
* The current date and time is not earlier than the specified start date and time
* No end date and time is specified, or the current date and time is not later than the specified end date and time.

{% hint style="info" %}
#### Note

The server that runs scheduled jobs operates with a UTC clock. This is important for Weekly and Monthly schedules when specifying the day of the week and the month of the year to run a job. For example, 11PM Saturday in the Eastern time zone is Sunday on the UTC clock. When working with Weekly or Monthly schedules we recommend that you set up your schedule using UTC.
{% endhint %}

## Set Up a Daily Schedule

To set up a daily schedule for the job, select Daily in the drop-down list at the left of the dialog. If you want the job to end at a particular time, click the End box.

Specify the starting time in the format HH:MM, using a 24 hour clock (for example, 4:12PM is entered as 16:12). Set the desired start date in the calendar. If the End box is checked, set the ending time and date in a similar fashion.

In the Every ... Day(s) box, set the number of days between jobs. For example, to run the job every other day, enter the value 2. The minimum allowed value is 1, and the maximum is 365.

## Set Up a Weekly Schedule

To set up a weekly schedule for the job, select Weekly in the drop-down list at the left of the dialog. If you want the job to end at a particular time, click the End box.

Specify the starting time in the format HH:MM, using a 24 hour clock (for example, 4:12PM is entered as 16:12). Set the desired start date in the calendar. If the End box is checked, set the ending time and date in a similar fashion.

In the Every ... Weeks(s) box, set the number of weeks between scheduled weeks. For example, to run the job every other week, enter the value 2. The minimum allowed value is 1, and the maximum is 52.

In the check boxes at the right of the dialog, specify the days of the week you want the job to run. If you do not specify a day of the week, the schedule will run on the same day of the week as the start date.

## Set up a Monthly Schedule

To set up a monthly schedule for the job, select Monthly in the drop-down list at the left of the dialog. If you want the job to end at a particular time, click the End box.

Specify the starting time in the format HH:MM, using a 24 hour clock (for example, 4:12PM is entered as 16:12). Set the desired start date in the calendar. If the End box is checked, set the ending time and date in a similar fashion.

In the check boxes at the right of the dialog, specify the months of the year you want the job to run. If you do not specify a month, the job will run on the same month as the start date. The job will run on the day of the month specified in the Start date.

## Repeat a Job

If you want the job to repeat on a given day, check the Repeat box and set the number of minutes between jobs, and the length of time you want to continue the repetitions. The minimum value allowed in each of these boxes is 10, and the maximum 1440. The value in the For ... minutes box must not be less than that in the Every ... minutes box.

For example, if you want a job to run on the hour every day from 8AM to 4PM, create a Daily schedule with a start time of 8AM. Check the Repeat box, and enter 60 in the Every ... minutes box, and 480 in the For ... minutes box. It is 8 hours from 8AM to 4PM, and 480 minutes is 8 hours.

## Change a Schedule

_Navigate: General/Jobs/Right-click job/Select Job Schedules_

To change a schedule, right-click the schedule and select Edit from the menu. If you have administrator privilege, you can edit any schedule. Otherwise, you can edit only those schedules that list you in the User Name column (the schedules you created.)

## Delete a Schedule

_Navigate: General/Jobs/Right-click job/Select Job Schedules_

To delete a schedule, right-click the schedule and select Delete from the menu. If you have administrator privilege, you can delete any schedule. Otherwise, you can delete only those schedules that list you in the User Name column (the schedules you created.)

## View the Parameters for a Scheduled Job

_Navigate: General/Jobs/Right-click job/Select Job Schedules_

To view the parameters for a scheduled job, right-click the schedule and select Parameters from the menu. The dialog box displays the information passed to the job when it runs.

## Run a Job Now <a href="#minitocbookmark9" id="minitocbookmark9"></a>

_Navigate: General/Jobs/Right-click job/Select Job Schedules_

If a schedule is not enabled, you can schedule the job to run at the current time. Right-click the schedule, and select Run Now from the menu. This menu item is grayed out if the schedule is enabled. Enabled schedules can run automatically only, based on the specified schedule.

When you use the Run Now command, the job will start soon, but not immediately.
