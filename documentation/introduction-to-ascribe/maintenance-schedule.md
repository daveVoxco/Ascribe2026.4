---
description: Know when planned maintenance happens so you can plan work around downtime.
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/introduction-to-ascribe/maintenance-schedule
---

# Maintenance Schedule

The maintenance schedule is determined by the support team and is different for most accounts. Users can see their own Maintenance Schedule under the General heading on the Home page.

The standard schedule for maintenance operations on the Ascribe database server is displayed below. During maintenance operations, Ascribe can run slowly. You can use the information in this report to help you plan your work schedule so that you avoid the maintenance periods to the extent possible.

The report has this form:

<table><thead><tr><th width="121"></th><th>Last Run</th><th width="145">Run Time (Seconds)</th><th>Next Run</th></tr></thead><tbody><tr><td>Daily</td><td>Sun 10/5/2008 1:00:05 AM</td><td>1,085<br>0:18</td><td>Mon 10/6/2008 1:00:00 AM</td></tr><tr><td>Weekly</td><td>Sun 10/5/2008 4:09:54 PM</td><td>3,720<br>1:02</td><td>Sun 10/12/2008 1:00:00 AM</td></tr><tr><td>Monthly</td><td>Sun 10/5/2008 2:20:35 PM</td><td>1<br>0:00</td><td>Sat 11/1/2008 2:00:00 AM</td></tr></tbody></table>

The maintenance operations run daily, weekly, and monthly. For each operation, this information is displayed:

* **Last run –** This column shows the date and time the maintenance operation last started. It is adjusted to your local time zone. You can hover over the date to see the information in UTC (Greenwich Mean Time.)
* **Run time (seconds) –** This column shows the number of seconds the maintenance operation took last time it ran, followed by the same information in hours:minutes. The amount of time the operation took last time is a good estimate of the time required next time.
* **Next run –** This column shows date and time the next maintenance operation will start. It is adjusted to your local time zone. You can hover over the date to see the information in UTC (Greenwich Mean Time.)

## Daily Maintenance Operations <a href="#minitocbookmark2" id="minitocbookmark2"></a>

During daily maintenance, you can still use Ascribe, and you should see only minimal performance reduction.

The primary function of daily maintenance is to defragment or reorganize the database indexes. The Ascribe database uses indexes to improve speed. As the contents of the database change, these indexes can become "fragmented," meaning that they are not organized as efficiently as possible.

First, the maintenance program checks for fragmentation on each index. This check can take several minutes, but typically less than 15 minutes. The program next fixes any fragmented indexes. Defragmentation can take from no time (if there are no fragmented indexes,) to more than an hour (if a large index is fragmented.)

Ascribe is usable still during this operation. The check for the amount of fragmentation actually causes slower performance than the defragmentation procedure does.

## Weekly Maintenance Operations <a href="#minitocbookmark3" id="minitocbookmark3"></a>

Weekly maintenance can affect Ascribe’s performance severely. You should try to avoid using Ascribe during this maintenance.

During weekly maintenance, Ascribe performs these tasks: deferred data deletion, shrink database, rebuild indexes, and consistency checks.

### Deferred Data Deletion <a href="#minitocbookmark4" id="minitocbookmark4"></a>

To improve performance, Ascribe defers the deletion of certain database records. An example is the deletion of questions from a study. If you were to delete a question with a large number of responses, it could take a long time for the database to process this request. This would slow you down, as well as any others using Ascribe. Instead of deleting the questions at the time you make the request, Ascribe marks the question for later deletion.

Deleting the data can take many minutes, and of course depends on just how much data was marked for deletion. The performance of Ascribe is very poor during this operation.

### Shrink Database <a href="#minitocbookmark5" id="minitocbookmark5"></a>

As data are deleted from the database, the size of the data files can become very large, which can adversely affect performance. During this maintenance task, the database files are reorganized to make them smaller. Ascribe is usable during this maintenance operation.

### Rebuild Indexes <a href="#minitocbookmark6" id="minitocbookmark6"></a>

The daily defragmentation of indexes helps keep performance at optimum levels, but a full index rebuild is required periodically. This operation does a better job than defragmentation, at the cost of rendering Ascribe unusable while it runs. Ascribe is not usable during this maintenance operation. You do not risk data by trying to use Ascribe while the operation is in progress, but many operations will fail, and most will be intolerably slow.

### Consistency Checks <a href="#minitocbookmark7" id="minitocbookmark7"></a>

A complete check of the database is performed to ensure the health of the database. Ascribe is usable during this operation, with degraded performance.

## Monthly Maintenance Operations <a href="#minitocbookmark8" id="minitocbookmark8"></a>

The monthly maintenance does not affect performance of Ascribe. Monthly maintenance performs the operation of usage calculation. Ascribe collects the transactions used for each account, and inserts this information in the statement for the account.\\
