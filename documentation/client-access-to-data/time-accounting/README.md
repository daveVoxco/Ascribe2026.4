---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/client-access-to-data/time-accounting
---

# Time Accounting

Time accounting provides time and cost information about your studies. There are two types of time accounting reports available in Ascribe: [Time by Study](time-accounting-reports/time-by-study-reports/) and [Time by Period](time-accounting-reports/time-by-period-reports/).

## How Ascribe Tracks Time <a href="#minitocbookmark2" id="minitocbookmark2"></a>

Time accounting in Ascribe is based on entering and leaving certain web pages (tracked pages) on the site. Ascribe maintains a clock for each tracked activity. The clock starts when the user enters a tracked page. The clock stops (and restarts for a new activity) when the user enters a different tracked page. The clock also stops when the user navigates to the Home page, or when the user logs out.

When the clock stops for an activity, the time record for that activity is finished, and the start and end times for the activity are stored.

Each time record contains:

* The **person** who performed the activity (based on the login information)
* The **activity** performed (the name of the page)
* The **study** worked on (If the activity does not relate to a study, this entry is blank.)
* The **question** worked on (If the activity does not relate to a question, this entry is blank.)
* The **start time** of the activity
* The **end time** of the activity
* The **number of responses** for which codes were applied during the tracked activity (i.e., the difference between the number of responses coded at the end time and the start time; this will be zero if the activity does not relate to a question.)

The time tracking reports display the time tracking information in various ways, allowing you to look at times by study, question, activity, and associate.

There are several important issues to remember when you are looking at time accounting reports:

* The **times recorded in these reports always will be less than the total session (login) time** of the people working. When the time accounting clock is stopped (because it was never started, or because the user navigated to the Home page), the time is not recorded in any time tracking record.
* **Time records are assigned to users by login ID.** This means that if you want to distinguish activities by individuals, each person using Ascribe must log in with a unique user name.
* **Time records are maintained for each browser session.** If a person uses two browser sessions and both are logged into Ascribe), time records will be maintained separately for each session. If you want to track activities only and are not interested in time for costing purposes, it is fine for users to log in with multiple sessions. However, if you want Ascribe time accounting to accurately reflect your project costs for labor hours, you should instruct your staff to use only a single browser session at a time.
* **Idle time when the clock is running is recorded the same way as non-idle time.** For example, a worker takes a break while coding a study and does not stop the clock. The worker then resumes coding later. The break time will be recorded along with active time. To prevent recording idle time, instruct your users to navigate to the Home page or log out during idle periods.
* **The only exception to the above is when a session times out from inactivity. When a session times out, the time record is finalized with the end time as the last time the user performed any activity.**

## **S**ession, Login and Tracked Hours <a href="#minitocbookmark3" id="minitocbookmark3"></a>

In the time accounting reports, you will find three ways time is tracked:

* **Session hours** - A session corresponds to an internet browser session in Ascribe. A session starts when the user logs in, and ends when the user logs out, or the session times out. If the user logs out, the session end time is the time of the logout. If the session times out, the session end time is the time of the last activity by the user, not the time that the timeout occurred. A session is tied to the user ID of the person who logged in.
* **Login hours** - It is possible for a given user to have more than one simultaneous session. The user might open two browsers and log in to each of them. Or, two people might log in to Ascribe at the same time using the same user ID. Login hours report the time a given user is logged in, eliminating any overlapping session hours for the user. For an example, a user opened two browsers and logged in with the same user ID in both, then worked for an hour and logged out in both browsers. The session hours recorded for this user would be 2 (one hour in each browser). The login hours reported would be 1 (the overlapping time is discarded). Login hours are a better indication of the total time a user worked in Ascribe, assuming no two users log in with the same user ID. If your users never work in two browsers at the same time, login hours will be the same as session hours. One final note: Login hours are computed when the session ends. Login hours will therefore not contain times for any open sessions.
* **Tracked hours** - As described above, Ascribe keeps track of time spent in certain activities. These are tracked hours. Tracked hours, like session hours, are recorded for each open session. If more than one session is active for the same user, tracked hours will be recorded for each session.

Generally, session hours will be greater than both login hours and tracked hours.

### Count of Responses Coded in Time Tracking Records <a href="#minitocbookmark4" id="minitocbookmark4"></a>

The count of responses coded in time tracking records gives information about production during a user's session. To interpret this information properly, you need to understand how this value is calculated.

Each code applied is marked with two pieces of information used in time accounting:

* The user session in which the code was applied (this also identifies the user)
* The date and time the code was applied.

This information is used by time accounting to determine the count of responses coded. When the user logs out, each code applied during the session is inspected. For each time slot in the time accounting records for that session, the number of responses with codes applied is totaled. This becomes the count of responses coded for that time accounting record.

There are a few implications of this method of counting responses coded:

* The sum of responses coded in time accounting for a given question will normally not equal the number of coded responses for that question. There are many reasons for this. For example, a response may have one code applied in one session, and a second code applied in a different session. In this case, the response will be counted twice in the time accounting records. Equally, a response may be coded in one session. In a later session, the response may be uncoded and coded a second time. Again, this response will be counted twice in time accounting.
* Counts of responses coded are calculated when the user logs out. Hence time accounting reports will not show response count information for currently open sessions.
* If responses are coded and the codes are deleted in the same session, they will not appear in the time accounting reports.
* The count of responses coded is intended to give a feel for overall production by a worker during a session. Do not use time accounting records to try to determine the number of currently coded responses.

## Use Time Accounting for Job Cost Calculations <a href="#minitocbookmark5" id="minitocbookmark5"></a>

You can configure Ascribe to give you job cost based on time accounting records. To do this, enter the hourly rate for each associate under Administrator/Associates. This allows Ascribe to calculate cost figures in the various time accounting reports. Some clients prefer to enter a flat rate for all associates to include the entire cost of the project to obtain this estimate.
