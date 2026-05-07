---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/data-management/how-to-load-data/load-data-to-a-study
---

# Load Data to a Study

_Navigate: Supervisor/Studies/Right-click study/Select Load Responses /Process File_

Once you navigate to the Load Responses/Process File page, enter the name of the file which contains the data into the field labeled 'Enter the name of the data file.' Either enter the path and file name of the file to be loaded or use the Browse button to browse your file system (just like Excel or Word).

Load file types are determined by their extension (the characters after the last '.' in the file name.) For more information, see [Load File Types](load-file-types.md).

When you load data, you have some options. These options always override the load file type properties. The options are:

<table><thead><tr><th width="249.99993896484375" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Load Data for Existing Questions</td><td valign="top">This option loads data to questions that already exist in the study. It is useful to load cumulative data files that contain questions which will not be used in Ascribe. Data for questions that have not been defined will be ignored. This option is grayed out if no questions exist in the study.</td></tr><tr><td valign="top">Pause Load to Prompt for Missing Questions</td><td valign="top">The loader will ask the user which questions should be created and/or loaded if the questions do not already exist in Ascribe.</td></tr><tr><td valign="top">Create Missing Questions Automatically</td><td valign="top">Ascribe will create questions whenever data is encountered for questions that have not been previously defined in the study. When you use this option, Ascribe ‘guesses’ the question type since you have not defined it yet. You can change the question type on the General Tab of the Edit Question screen.</td></tr><tr><td valign="top">Auto-Code Closed and O/S Questions</td><td valign="top">While it loads data, Ascribe will automatically code responses to closed-ended and other specify questions which have numeric values.</td></tr><tr><td valign="top">Auto-Code Text Responses</td><td valign="top">Ascribe will automatically code text responses as they are loaded. See the next sections for more information.</td></tr></tbody></table>

After you select the options, press the OK button to load the data. The Load Details screen displays. It describes the results of your load. For more information, see [Load Details](load-details.md).

## Auto-Code Text Responses on Load <a href="#minitocbookmark2" id="minitocbookmark2"></a>

This feature allows the user to elect for Ascribe to attempt to auto-code textual responses after loading. It looks for exact textual matches across shared codebooks. It compares the data across studies with shared codebooks. In essence, it allows the user to code a unique response one time, and after that, the loader compares and automatically codes the responses after they are loaded.

It is helpful for a few scenarios:

* Code across shared codebooks within a study
* Code across shared codebooks between two or more studies
* Code incremental loads of data

Some considerations:

* "See previous response" comments – if you refer to the previous response to code this type of answer, then you might want to leave them for coding after your last load.
* Positive/Negative/Neutral Nets -- Auto-coding textual responses does not work well for codebooks that have positive, negative and neutral nets. If the code applied depends on a previous question, then auto-coding textual responses should not be used. For example, you have a believability question that refers back to rating question. The response "price" could be positive, negative or neutral depending on the closed-end rating question.

The data coded by the load coder will not be attributed to a user; instead, it will be attributed to "loader." This allows the user to distinguish between responses coded by a person and responses coded by Ascribe.

## Use the Load Coder <a href="#minitocbookmark3" id="minitocbookmark3"></a>

Set your study up and share codebooks where necessary. For tracker studies, it is usually best to create your new study by using the Copy Study option.

After loading a file, a post-load process will compare the coding source of all previously coded responses using the same shared codebook with the responses from newest load. While comparing the responses, if there are any inconsistencies in coding of a duplicate response, load coder will skip the response rather than apply a code.

You can check for inconsistencies in coding before you load more data. See the [Auto-Coder Script](../download-data/download-data-with-scripted-output/auto-coder-script.md) or the [Inconsistencies tab](../../ascribe-coder/search-responses.md#minitocbookmark5) of Search Responses in Ascribe Coder.

## Ways to Run Load Coder <a href="#minitocbookmark4" id="minitocbookmark4"></a>

There are several ways you can run the load coder:

* Manual Load – Check the "auto-code text responses" box before you load your data file.
* Automated Load – Use Account Options to set the "auto-code text responses" box.
* Set up a special load file type for auto-coding textual responses (works on manual and automatic loads.)

{% hint style="info" %}
#### Hint

If you need to auto-code textual responses sometimes but not always, you could set up a load file type called auto.txt (for text files) and auto.xls (for Excel files.) Then, just rename the files you wanted to auto-code with the extension .auto.txt or .auto.xls.
{% endhint %}

Remember, load coder compares the newly loaded data with the coding source of all previously coded data across shared codebooks (across studies, across questions). You do not have the choice to compare the coding with a certain study. The load coder identifies which codebook the question uses and compares across all shared codebook responses.
