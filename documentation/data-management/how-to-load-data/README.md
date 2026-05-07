---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/data-management/how-to-load-data
---

# How to Load Data

There are number of ways to load data:

* From an Excel file
* From a tab delimited file
* From a CfMC SURVENT generated . lst file
* From an XML file in the Ascribe format
* From a "mapped ASCII" file that you define
* From custom developed interfaces that typically deliver data in "real time."

Each has different formatting requirements, and each is recognized by Ascribe by the file name extension. When you load the data, the system will load only "new" data. This means that you may load cumulative data sets and be assured that only those records that are new will be loaded. The respondent number/question ID combination must be unique to be loaded.

## Load Tab Delimited Data <a href="#minitocbookmark2" id="minitocbookmark2"></a>

Three-column tab delimited data is the "native format" for Ascribe. When Ascribe encounters a file with a . txt extension, it assumes that the file is in this format: question ID, respondent ID, and verbatim/closed ended data. If a fourth column is present, Ascribe assumes it is transcription data. Each field is delimited by a tab character. (If this format is inconvenient, or you have a file with a different delimiter, you can define your own file format. See [Define Your Own Load File Types](define-your-own-load-file-types.md) for more information.)

To load a tab delimited file, prepare a file of data that contains question ID, respondent ID, and verbatim or closed ended data in a tab delimited text file. (Transcription data can follow the verbatim.) At Ascribe, we use Excel to prepare the file.

Here are the steps to prepare the file:

* Copy the file into Excel (you may have to use the text to columns feature).
* Delete any header rows and irrelevant columns.
* Check that you have the question ID in the first column, the respondent ID in the second, and the verbatim text or closed-ended data in the third column.
* Save the file as a tab delimited text file; use Save As from the Excel File menu.
* Name the file studyname\_date.txt. If you use this naming format, the person who loads the data into the study will have an easier time finding it. We recommend that you include the date in the filename for identification purposes and to make support more efficient. Tab delimited files will look like this:

![](https://static.goascribe.com/Help/Tab_Delimited_Data.gif)

The next step is to load the data to the study. Data loads in the order it is in the file. So if you sort the data before you load, it will load in that sorted order. For more information, see [Load Data to a Study](load-data-to-a-study.md).

## Load Excel Files <a href="#minitocbookmark3" id="minitocbookmark3"></a>

Ascribe loads Excel files in their native, Excel format. To load an Excel file, you will need to have it in this format.

The column containing the respondent number must have the word " RespondentID", " ResponseID", "RID", " CaseID" or " SessionID" as the first cell in the column.

{% hint style="info" %}
#### Note

You can also specify the column header using a "Load File Type". It is advised to do this only if the files you will be loading consistently use the column header you wish to specify. See "[Define Your Own Load File Types](define-your-own-load-file-types.md)" for further information.
{% endhint %}

Each of the questions that you are loading must have their question ID in the top row (the first cell), with the data for that question in the rows beneath those questions.

A few comments:

* You may "customize" your Excel format by defining a "Load File Type".
* If you have multiple spreadsheets in an Excel workbook, only the first one alphabetically will load. The rest will be ignored.
