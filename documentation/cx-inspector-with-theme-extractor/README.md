---
hidden: true
noIndex: true
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/cx-inspector-with-theme-extractor
---

# CX Inspector with Theme Extractor

CX Inspector with Theme Extractor analyzes textual (open-end) data and organizes similar ideas into themed categories (which we call codes or a codebook). It also visualizes the categories, facilitates exploration/filtering via demographics, ratings, or other relevant data (closed-end data).

Any textual data can be analyzed, such as NPS, CSAT, employee satisfaction, and product reviews.

## How It Works

* Load data
* Analyze the data
* Visualize the results
* Edit the results

## Load the Data

![](https://static.goascribe.com/Help/CXI_3_home_page.jpg)

Click the Upload and Analyze icon to select a file and load it.

Some notes about loading data:

* Acceptable file formats are Excel (horizontal for multiple questions), CSV (table format), and TSV.
* The file should be formatted with the first row containing column headers such as question IDS and other variable identifiers. The following column headers are recognized as respondent identifiers: id, uuid, guid, rid, respondentid, and respondent.
* The maximum file size that can be loaded is 30 megabytes.
* If the Excel file has multiple sheets, only the data contained in the first non-hidden sheet will be loaded.
* Incremental data can be loaded.

## Options

Here are the CX Inspector options:

<table><thead><tr><th width="245.66668701171875" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top"><strong>View</strong></td><td valign="top"></td></tr><tr><td valign="top">Sentiment and/or Topics</td><td valign="top">Choose Sentiment, Topics or both.</td></tr><tr><td valign="top"><strong>Tables and Charts</strong></td><td valign="top"></td></tr><tr><td valign="top">Display</td><td valign="top">Choose count, percentage, or both.</td></tr><tr><td valign="top">Source</td><td valign="top">Choose overall (count of mentions; it is a duplicated count which means if a topic was mentioned multiple times in a response, each mention is counted), comments (count of responses; it is an unduplicated count which means no matter how many times a topic is mentioned in a response, it only counts once), or respondents (this is the same as comments unless you have analyzed multiple questions; a respondent is only counted once.)</td></tr><tr><td valign="top">Sentiment</td><td valign="top">Choose average sentiment, X-Score, or X-Sum. (X-Sum is topic frequency multiplied by average sentiment rating.)</td></tr><tr><td valign="top">Top N Items in Tables</td><td valign="top">Enter the number of items to display in tables.</td></tr><tr><td valign="top">Top N X-Scores in Chart</td><td valign="top">Enter the number of items to display in the X-Score chart.</td></tr><tr><td valign="top"><strong>Inspection</strong></td><td valign="top"></td></tr><tr><td valign="top">ID</td><td valign="top">Indicates the name of the file loaded but can be renamed in this field or in the top blue banner.</td></tr><tr><td valign="top">Contact Name</td><td valign="top">Optional contact information</td></tr><tr><td valign="top">Phone or Email</td><td valign="top">Optional contact information</td></tr><tr><td valign="top"><strong>Advanced</strong></td><td valign="top"></td></tr><tr><td valign="top">Loads</td><td valign="top">This section has load properties, including a summary of what was loaded and when, what variables were loaded, and what variables were analyzed. This section also has an option to delete loads. The loaded file is available for download from the Summary tab.</td></tr><tr><td valign="top">Ignore Items</td><td valign="top">Displays the Ignore dialog. You can ignore expressions. Add the items and separate them with commas or semicolons.  </td></tr><tr><td valign="top">Rule Sets</td><td valign="top">This section lists available rule sets with the option to undo the application of a rule set. The last rule set applied is listed at the top of the dialog, along with the user name and date. For more information, see Rule Sets.</td></tr><tr><td valign="top">View</td><td valign="top">This option allows you to toggle on/off a dark chart background.</td></tr><tr><td valign="top">Load Study</td><td valign="top">Load additional data from a study.</td></tr><tr><td valign="top"> </td><td valign="top"></td></tr><tr><td valign="top">Save As Defaults</td><td valign="top">This option saves the settings as a default for new inspections. It also saves whatever is displayed in the Extracts pane as the default view.</td></tr><tr><td valign="top">Restore To Defaults</td><td valign="top">This option restores to settings whatever the user has selected when using the Save as Defaults option.</td></tr></tbody></table>

<br>
