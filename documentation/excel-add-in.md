---
metaLinks:
  alternates:
    - https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/excel-add-in
---

# Excel Add-In

The Excel Add-In is used for cleaning data or study set-up. (It was formerly used to handle problems related to loading Excel files, but those issues have been resolved. Try loading the Excel file directly to Ascribe without using the add-in.)

To use the add-in, install the latest version:

{% stepper %}
{% step %}
Navigate to General/Downloads.
{% endstep %}

{% step %}
Click the link for Excel Add-In for Ascribe, which should download a .xlam file to your computer.
{% endstep %}

{% step %}
Move the file from the download location to this location: C:\Users\YOURUSERNAME\AppData\Roaming\Microsoft\Addins. (Substitute your user name for YOURUSERNAME.)
{% endstep %}

{% step %}
Once the file has been moved, right-click it and select Properties.
{% endstep %}

{% step %}
In the Properties dialog, look for an Unblock button or checkbox at the bottom of the General tab. If it is present, click it and then click OK. If it is not present, close the dialog and go to the next step.
{% endstep %}

{% step %}
Open a new blank Excel workbook.
{% endstep %}

{% step %}
From the Excel menu, select File/Options.
{% endstep %}

{% step %}
In the Excel Options dialog, select Add-ins in the left margin.
{% endstep %}

{% step %}
The display to the right of the margin should change. At the bottom of the dialog, there should be a Manage drop-down; ensure that Excel Add-ins is selected in the drop-down list and then click the Go... button next to it.
{% endstep %}

{% step %}
In the Add-ins dialog, select the Browse button and browse to the file you moved in Step 3. Once you browse to the correct folder, select the file and click OK. It should now be listed in your available add-ins.
{% endstep %}

{% step %}
Make sure Excel Utilities for Ascribe is checked and then click OK.
{% endstep %}
{% endstepper %}

You should now see an Add-ins tab at the top of your Excel. If you do not, try the additional steps below or [contact Support](https://app.gitbook.com/s/z7SRTUu0F0liQ4Zr5Bdl/contact-support-ascribe).

{% stepper %}
{% step %}
From the Excel menu, select File/Options.
{% endstep %}

{% step %}
Select Trust Center in the left margin.
{% endstep %}

{% step %}
The display to the right should change. Click the Trust Center Settings button.
{% endstep %}

{% step %}
A new Trust Center dialog will display. Select Trusted Locations in the left margin.
{% endstep %}

{% step %}
The display to the right should change. Click the Add New Location button.
{% endstep %}

{% step %}
In the Microsoft Office Trusted Location dialog, select the Browse button and browse to the location from Step 3 (see first set of directions) and click OK.
{% endstep %}

{% step %}
Click OK in the Microsoft Office Trusted Location dialog.
{% endstep %}

{% step %}
Click OK in the Trust Center dialog.
{% endstep %}

{% step %}
Click OK in the Excel Options dialog.
{% endstep %}
{% endstepper %}

Close Excel and open a new blank Excel workbook. You should now see the Add-ins tab at the top of your Excel.

### Use the Excel Add-In for Question Setup in Ascribe <a href="#minitocbookmark2" id="minitocbookmark2"></a>

The study setup functions allow the user to create, modify, or update question setting information for all questions in a study with a one-page document. Information that can be updated: qtype, qlabel, qtext, qcard, qcolumn, qcolumns, qmaxcode.

Here are the steps to set up a study with the add-in:

{% stepper %}
{% step %}
Open Excel.
{% endstep %}

{% step %}
For Excel 2003, click the Ascribe Tools menu. For Excel 2007 or higher, click the Add-Ins tab.
{% endstep %}

{% step %}
For Excel 2003, click **Study Set-Up**. For Excel 2007, click Ascribe Tools and then click Study Setup.
{% endstep %}

{% step %}
Choose the appropriate set-up option from the list:

* Make new Blank Question Template -Used to add questions manually to an existing study in Ascribe or if you only need to add one or two questions to an existing study.
* Load Questions from saved Ascribe Study (XML) - Allows the user to pull the question set-up information from any saved Ascribe study.
* Load Questions from Ascribe - Allows the user to populate the template with question set-up information from an existing study in Ascribe.
{% endstep %}

{% step %}
Fill out the form for any questions you wish to add or modify in your study. You can copy and paste from the questionnaire, data map, or any other document that contains the information you need. All Excel functionality works on the template. You can use formulas to create card and column locations. You can use the drag/fill function to populate the cells, etc. One thing that you should not do is insert new columns within the Question Information headings. If you need to do "math" or insert formulas, be sure to use columns outside of the template (i.e., after the Max Codes column).
{% endstep %}
{% endstepper %}

After filling out the template with the desired question set-up information, you have two choices for loading the template to Ascribe:

* Save the file using the .setup.xls extension. (Examples: statichair.setup.xls or 10238.setup.xls). Then, load the template into the study.
* Use the **Send Questions to Ascribe** function, which automatically sends the template to Ascribe and updates the current set-up with any modifications.
