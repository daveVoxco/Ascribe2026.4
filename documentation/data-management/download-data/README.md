---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/data-management/download-data
---

# Download Data

_Navigate: Supervisor/Studies/Right-click study/Select Download Data/Select Codebooks and Results_\
_Client/Studies/Right-click study/Select Download Data/Select Codebooks and Results_

Ascribe has several standard formats for downloading data. To download codebooks or study results, set the desired options on the Downloads and click the OK button.

You can select which questions are included in the download. The table at the bottom of the page displays the questions. To change the questions selected, check the desired question types in the grey bar, and click the Update button. Or you can select individual questions in the Select column. There is also a Filter box where you can enter text to filter the questions displayed. The data included in the download is drawn from only the questions selected in this table.

## Download Study Results <a href="#minitocbookmark2" id="minitocbookmark2"></a>

_Navigate: Supervisor/Studies/Right-click study/Select Download Data/Select Codebooks and Results/Select Download Results_\
_Client/Studies/Right-click study/Select Download Data/Select Codebooks and Results/Select Download Results_

Results may be downloaded in any of a number of formats. If you choose column binary, the codes will be interpreted as column/punch (e.g., 141 = column 14, punch 1). You may also choose to include the actual verbatim in any of the ASCII data formats. For larger files it is recommended that you write the results to a file and download the file, rather than cutting and pasting which are more convenient with smaller files.

To download study results, select one of the formats from the list:

<table><thead><tr><th width="230" valign="top">Format</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Table format, one row for each response</td><td valign="top">This format gives a file with one text row per response. Each row contains the question ID, the respondent ID, and the output code value of the codes applied to the response. Because a variable number of codes can be applied to each response, the number of fields in each row is variable. Fields are separated by tab characters. Table formats may be pasted directly into Word.</td></tr><tr><td valign="top">Comma separated variable format, one row for each response</td><td valign="top">This format is identical to the above option, except that fields are separated by commas, and all fields except the respondent ID are enclosed in quotation marks. Comma separated variables provide fast and easy integration into Microsoft products and other applications.</td></tr><tr><td valign="top">Table format, one row for each code</td><td valign="top">This format gives a file with one text row per code. Each row contains the question ID, the respondent ID, and the output code value of the code applied. If a given response has more than one code applied, it will be written to successive rows. The number of fields is fixed at three. Fields are separated by tab characters. Table formats may be pasted directly into Word.</td></tr><tr><td valign="top">Comma separated variable format, one row for each code</td><td valign="top">This format is identical to the above option, except that fields are separated by commas, and all fields except the respondent ID are enclosed in quotation marks. Comma separated variables provide fast and easy integration into Microsoft products and other applications.</td></tr><tr><td valign="top">Column binary format</td><td valign="top">This format produces a file suitable for use by tab packages such as Quantum. The properties set in the Study Edit page and the Edit Questions page determine the layout of data in the file.</td></tr><tr><td valign="top">CfMC format</td><td valign="top">This format produces output in a format compatible with the CfMC products.</td></tr><tr><td valign="top">User defined</td><td valign="top">You can define your own format. It is commonly used to generate statements that instruct other software to insert data into specific locations. For example, you can use an emit statement in Quantum. For more information, see <a href="./#minitocbookmark3">User Defined Study Results</a>.</td></tr></tbody></table>

The first four formats listed allow you to also include the verbatim response in the output when you click the check box for this option.

## User Defined Study Results <a href="#minitocbookmark3" id="minitocbookmark3"></a>

_Navigate: Supervisor/Studies/Right-click study/Select Download Data/Select Codebooks and Results/Select Download Results/Select User Defined/Click New or Edit_\
_Client/Studies/Right-click study/Select Download Data/Select Codebooks and Results/Select Download Results/Select User Defined/Click Edit_

The user defined option under download data and results allows the user to customize the data output from Ascribe by specifying the text to output, and include substitution values that are replaced with information from the study.

{% hint style="info" %}
#### Note

Ascribe has a more powerful way to create custom output files using scripted output. If you cannot create the output format you need in this window, check with Ascribe support about a custom-written scripted output.
{% endhint %}

As Ascribe processes the results, it writes your output values at the start of each question, the start and end of each respondent, and the start of each code. To create your file, fill in the form with a mixture of text and substitution values. Any text that is not a substitution value is output 'as is'.

<table><thead><tr><th width="217.333251953125" valign="top">Entry</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Name</td><td valign="top">The name of this user defined results specification. This name will appear in the drop-down list of user defined results available to all users.</td></tr><tr><td valign="top">Start of a Question</td><td valign="top">This value is output at the beginning of each question.</td></tr><tr><td valign="top">Start of a Respondent</td><td valign="top">This value is output at the start of each respondent to the question.</td></tr><tr><td valign="top">Code</td><td valign="top">This value is output for each code applied to the response for a respondent.</td></tr><tr><td valign="top">End of a Respondent</td><td valign="top">This value is output after all codes for the response.</td></tr><tr><td valign="top">End of a Question</td><td valign="top">This value is output after all responses to a question.</td></tr></tbody></table>

By default, only responses that have codes applied are included in the output. If you want all responses regardless of whether or not they have been coded, click the Include uncoded responses check box. To include output that has double-byte characters (i.e., Chinese and Korean), click the Unicode check box.

```
/* Dislikes

if (c(101,105).eq.10001) emit

+ c0420'8'

+ c0420'2'

if (c(101,105).eq.10015) emit

+ c0420'8'

+ c0421'8'

if (c(101,105).eq.10023) emit

+ c0420'8'

+ c0421'8'

if (c(101,105).eq.10035) emit

+ c0420'8'

if (c(101,105).eq.10093) emit

+ c0420'8'

if (c(101,105).eq.10095) emit

+ c0420'8'

if (c(101,105).eq.10096) emit

+ c0420'8'
```

This code instructs a TAB package to look in columns 1 through 5, and if it matches the respondent number, to insert the relevant punches in the relevant columns.

## Substitution Values for User Defined Study Results <a href="#minitocbookmark4" id="minitocbookmark4"></a>

Here are the substitution values for the user defined study results:

<table><thead><tr><th width="219.99993896484375" valign="top">Value</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">[ CColumn]</td><td valign="top">Code column (all characters of code value except punch) -<br>This gives all characters of the code Output value except for the rightmost character. For example, if the code output value is 1234, CColumn is 123.</td></tr><tr><td valign="top">[CColumn+]</td><td valign="top">QColumn incremented by QColumns for each code applied -<br>This gives the QColumn value for the first code applied to a response, then QColumn + QColumns for the next code, and so on. The QColumns value is added after each code. This is useful for Numeric output for column binary format, to determine the column value for the code.</td></tr><tr><td valign="top">[CEndColumn+]</td><td valign="top">(QColumn + QColumns - 1) incremented by QColumns for each code applied - This is similar to [CColumn+], but gives the end column for the code instead of the start column.</td></tr><tr><td valign="top">[CHelp]</td><td valign="top">Code help - The Long help text for the code.</td></tr><tr><td valign="top">[CHover]</td><td valign="top">Code hover help - The Hover help text for the code.</td></tr><tr><td valign="top">[CInputID]</td><td valign="top">Input code value - The Input code value.</td></tr><tr><td valign="top">[CLevel]</td><td valign="top">Level of code in code book (1 = top level) - The indentation level of the code in the codebook, where the value 1 means 'top level'.</td></tr><tr><td valign="top">[ColPunch]</td><td valign="top">Same as [CColumn]'[CPunch]' - This is simply a shorthand for a common way of showing column/punch style codes. A code with Output code value 1234 will produce 123'4'</td></tr><tr><td valign="top">[COutputID]</td><td valign="top">Output code value - The Output code value of the code</td></tr><tr><td valign="top">[CNumber]</td><td valign="top">Code row number - The position of the code in the codebook, where the first code is number 1, the second 2, and so on. The indentation level of the code is ignored. It is simply the vertical position of the code in the codebook.</td></tr><tr><td valign="top">[CPunch]</td><td valign="top">Code punch (rightmost character of code value) - The code punch is meaningful if you are using punch format for column binary output. By convention, the code punch in this format is the rightmost character in the Output code value. The remaining digits to the left are the column. For example:<br>123 = punch 3, column 12<br>645x = punch x, column 645</td></tr><tr><td valign="top">[CRegExp]</td><td valign="top">Regular expression - The regular expression for the code.</td></tr><tr><td valign="top">[CText]</td><td valign="top">Code description - The description of the code. This is the text associated with a code.</td></tr><tr><td valign="top">[NL]</td><td valign="top">Insert line break - This value ends the current line and starts a new line. You must insert [NL] values unless you want all of the output on a single line.</td></tr><tr><td valign="top">[RID]</td><td valign="top">Respondent ID - The respondent ID: the identifier for the respondent in the loaded data.</td></tr><tr><td valign="top">[RTrans]</td><td valign="top">Transcription - The transcription text associated with this response.</td></tr><tr><td valign="top">[RVerbatim]</td><td valign="top">Verbatim response - The text response from the respondent.</td></tr><tr><td valign="top">[QCard]</td><td valign="top">Question card - Outputs the card number of the question.</td></tr><tr><td valign="top">[QID]</td><td valign="top">Question ID - Outputs the Question ID text.</td></tr><tr><td valign="top">[QColumns]</td><td valign="top">Question columns - Outputs the question columns value.</td></tr><tr><td valign="top">[QColumn]</td><td valign="top">Question column - Outputs the question column value.</td></tr><tr><td valign="top">[QHelp]</td><td valign="top">Question help - Outputs the Question help text.</td></tr><tr><td valign="top">[QLabel]</td><td valign="top">Question label - Outputs the Question label text.</td></tr><tr><td valign="top">[QMaxCodes]</td><td valign="top">Maximum number of codes to output - Outputs the Maximum codes value for the question.</td></tr><tr><td valign="top">[QText]</td><td valign="top">Question text - Outputs the question text.</td></tr><tr><td valign="top">[SCardCols]</td><td valign="top">Columns per card/respondent - Outputs the Columns per card/respondent value for the study.</td></tr><tr><td valign="top">[SCardNumCol]</td><td valign="top">Card number column - Outputs the Card number column value for the study.</td></tr><tr><td valign="top">[SCardNumCols]</td><td valign="top">Card number columns - Outputs the Card number columns value for the study.</td></tr><tr><td valign="top">[SDesc]</td><td valign="top">Study description - Outputs the Study description text.</td></tr><tr><td valign="top">[SID]</td><td valign="top">Study ID - Outputs the Study ID text.</td></tr><tr><td valign="top">[SName]</td><td valign="top">Study name - Outputs the Study name text.</td></tr><tr><td valign="top">[SRIDCol]</td><td valign="top">Respondent ID column - Outputs the Respondent ID column value for the study.</td></tr><tr><td valign="top">[SRIDCols]</td><td valign="top">Respondent ID columns - Outputs the Respondent ID columns value for the study.</td></tr><tr><td valign="top">[Tab]</td><td valign="top">Insert a tab character - This value puts a tab character in the output. It is useful when you want to import the data to Excel. Excel uses a tab character to mean 'start a new column'.</td></tr></tbody></table>

## Download Codebooks <a href="#minitocbookmark5" id="minitocbookmark5"></a>

_Navigate: Supervisor/Studies/Right-click study/Select Download Data/Select Codebooks and Results/Select Download Codebooks_\
_Client/Studies/Right-click study/Select Download Data/Select Codebooks and Results/Select Download Codebooks_

You can download the codebooks for any or all questions in the study. Codebooks may be downloaded in several formats. To download a codebook, select one of the formats from the list:

<table><thead><tr><th width="231.3333740234375" valign="top">Format</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Table format, one row for each code</td><td valign="top">This format gives a file with one text row per code. Each row contains the question ID, the respondent ID, and the output code value of the code applied. If a given response has more than one code applied, it will be written to successive rows. The number of fields is fixed at three. Fields are separated by tab characters. Table formats may be pasted directly into Word.</td></tr><tr><td valign="top">Comma separated variable format, one row for each code</td><td valign="top">This format is identical to the above option, except that fields are separated by commas, and all fields except the respondent ID are enclosed in quotation marks. Comma separated variables provide fast and easy integration into Microsoft products and other applications.</td></tr><tr><td valign="top">User defined</td><td valign="top">You can define your own format. It is commonly used to generate statements that instruct other software to insert data into specific locations. For example, you can use an emit statement in Quantum. For more information, see <a href="./#minitocbookmark6">User Defined Codebook Formats</a>.</td></tr></tbody></table>

## User Defined Codebook Formats <a href="#minitocbookmark6" id="minitocbookmark6"></a>

_Navigate: Supervisor/Studies/Right-click study/Select Download Data/Select Codebooks and Results/Select Download Codebooks/Select User Defined/Click Edit or New_\
_Client/Studies/Right-click study/Select Download Data/Select Codebooks and Results/Select Download Codebooks/Select User Defined/Click Edit_

The user defined codebook output format allows the user to construct a custom file of codebook information. The user can specify the text included in the output, and include substitution values that are replaced with information from codebooks.

<table><thead><tr><th width="229.33331298828125">Entry</th><th>Description</th></tr></thead><tbody><tr><td>Name</td><td>The name of this user defined codebook specification. This name will appear in the drop-down list of user defined codebooks available to all users.</td></tr><tr><td>Start of the Study</td><td>This value is output first, and will appear on the first line of the file. Only study substitution values are legal.</td></tr><tr><td>Start of a Question</td><td>This value is output at the start of each question, and before any codes in the question. Study and question substitution values are legal, but code substitution values are not.</td></tr><tr><td>Start of a Net</td><td>This value is output at the start of each net (any code that has children).</td></tr><tr><td>End of a Net</td><td>This value is output at the end of each net (any code that has children). Codes that are children of this net are output between the Start of a net and the End of a net.</td></tr><tr><td>Code</td><td>This value is output for each code that has no children (is not a net).</td></tr></tbody></table>

Example of User Defined Codebook:

![](https://static.goascribe.com/Help/10_-_Data_Management_recd_020909_julie_files/image038.jpg)

Static Hair Master - Punch using Column Offset

```
q7   7. What, if anything, did you particularly LIKE about the Static Free product? (PLEASE BE AS SPECIFIC AS POSSIBLE)

                     Efficacy (Net)

                     Appearance to Hair ( Subnet)

1    20   1         Straightens hair

1    20   2         All other appearance to hair mentions

                     Control ( Subnet)

1    20   3         Controls fly away hair

1    20   4         Controls frizziness

1    20   5         Controls static

1    20   6         Manageable hair

1    20   7         All other control mentions

                     Static ( Subnet)

1    20   8         Eliminates Static

1    20   9         Eliminates winter static

1    21   0         All other static mentions

                     Miscellaneous Efficacy

1    21   1         Works well

1    21   2         Works quickly

1    21   3         All other efficacy mentions
```

## Substitution Values for User Defined Codebook Formats <a href="#minitocbookmark7" id="minitocbookmark7"></a>

Here are the substitution values for user defined codebook formats:

<table><thead><tr><th width="207.3333740234375" valign="top">Value</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">[NL]</td><td valign="top">Insert line break -This value ends the current line and starts a new line. You must insert [NL] values unless you want all of the output on a single line.</td></tr><tr><td valign="top">[Tab]</td><td valign="top">Insert a tab character - This value puts a tab character in the output. It is useful when you want to import the data to Excel.  Excel uses a tab character to mean 'start a new column'.</td></tr><tr><td valign="top"><strong>Codes</strong></td><td valign="top"><hr></td></tr><tr><td valign="top">[CChildren]</td><td valign="top">Count of children (sub-codes) of this code - This is the number of codes that are directly below the current code (including nets), but it does not include codes below those codes. In other words, it is a count of all codes at the next indentation level in the codebook, but not at lower levels. If you want a count of all codes below the current code regardless of level, use the [CDescendants] value.</td></tr><tr><td valign="top">[CColumn]</td><td valign="top">Code column (all characters of code value except punch) - The code column is meaningful if you are using punch format for column binary output. By convention, the code column in this format is all digits in the Output value except for the rightmost digit. The rightmost digit is the punch. For example:<br>123 = punch 3, column 12<br>645x = punch x, column 645</td></tr><tr><td valign="top">[CDescendants]</td><td valign="top">Count of descendants (sub-codes and their sub-codes) of this code - This is a count of all sub-codes of the current code (including nets), regardless of level. If you want a count of only the codes at the next level, use the [CChildren] value.</td></tr><tr><td valign="top">[CGroup]</td><td valign="top">Code group number (e.g. 1.3.2) - The code group number is an outline-style number for the net that contains the code. The value 1.3.2 means 'this code belongs to the second net below the third net below the first net in the codebook'. The CGroup is the same for each sub-code of a given net.</td></tr><tr><td valign="top">[CHelp]</td><td valign="top">Code help - Outputs the long help for the code.</td></tr><tr><td valign="top">[CHover]</td><td valign="top">Code hover help - Outputs the hover help for the code.</td></tr><tr><td valign="top">[CID]</td><td valign="top">Output code value - This is the same as [COutputID]</td></tr><tr><td valign="top">[CIndent]</td><td valign="top">Insert [CLevel] tab characters - This value writes the number of tab characters corresponding to the indentation level of the code in the codebook. This is useful for creating a formatted view of the codebook, when you want to put a copy of the codebook in a text document.</td></tr><tr><td valign="top">[CInputID]</td><td valign="top">Input code value - Outputs the input code value for the code.</td></tr><tr><td valign="top">[CKey]</td><td valign="top">Key number for code (guaranteed unique) - Outputs a number that is guaranteed to be unique for each code in the codebook. You should consider this to be a random number. It will not change as long as the codebook is stored in Ascribe. It will change if you save the study and restore it.</td></tr><tr><td valign="top">[CLevel]</td><td valign="top">Level of code in code book (1 = top level) - This is the indentation level of the code in the codebook. The value 1 means this is a top-level code. Sub-codes of top level codes have CLevel = 2, etc.</td></tr><tr><td valign="top">[CList]</td><td valign="top">List of all descendant code values (but no nets), separated by commas - Outputs the COutputID value for each sub-code of this code, at all levels below this code. Nets are not included in this list. Each COutputID is separated by a comma.</td></tr><tr><td valign="top">[CNumber]</td><td valign="top">Code row number - This is the position of the code in the code book, where the first code is number 1, the second 2, and so on. The indentation level of the code is ignored. This is simply the vertical position of the code in the codebook.</td></tr><tr><td valign="top">[ColPunch]</td><td valign="top">Same as [CColumn]'[CPunch]' - For example, if the Output code value is 1234, it will output 123'4'</td></tr><tr><td valign="top">[COutputID]</td><td valign="top">Output code value - Writes the Output code value for the code.</td></tr><tr><td valign="top">[CPunch]</td><td valign="top">Code punch (rightmost character of code value)<br>The code punch is meaningful if you are using punch format for column binary output. By convention, the code punch in this format is the rightmost character in the Output code value. The remaining digits to the left are the column. For example:<br>123 = punch 3, column 12<br>645x = punch x, column 645</td></tr><tr><td valign="top">[CPunchList]</td><td valign="top">List of all descendant code [ColPunch] values (but no nets), separated by commas - This is similar to CList, except that the values in the list are in the ColPunch format, for example 34'5'</td></tr><tr><td valign="top">[CPunchListOr]</td><td valign="top">c23'534'.or.c26'18-x'.or.c34'2579'...<br>This is similar to CPunchList, except that a 'c' character precedes each code, and the codes are separated by .or.</td></tr><tr><td valign="top">[CRegExp]</td><td valign="top">Regular expression - Outputs the Regular Expression for the code.</td></tr><tr><td valign="top">[CText]</td><td valign="top">Code description - Outputs the Description of the code.</td></tr><tr><td valign="top">[CCodesApplied]</td><td valign="top">Codes applied - Outputs the number of times this code has been applied to responses in the current question.</td></tr></tbody></table>

<table data-header-hidden><thead><tr><th width="213.333251953125" valign="top"></th><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><strong>Questions</strong></td><td valign="top"><hr></td></tr><tr><td valign="top">[QCard]</td><td valign="top">Question card - Outputs the card number of the question.</td></tr><tr><td valign="top">[QCBKey]</td><td valign="top">Key number of code book (guaranteed unique) - Outputs a number that is guaranteed to be unique for each codebook. You should consider this to be a random number. It will not change as long as the codebook is stored in Ascribe. It will change if you save the study and restore it. If the codebook is shared, the same number is output for each instance of the codebook. For example, if questions A and B share the same codebook, the same value for QCBKey will be output for question A as for question B.</td></tr><tr><td valign="top">[QCodesApplied]</td><td valign="top">Codes applied - Outputs the number of codes that have been applied for this question, totaled across all responses.</td></tr><tr><td valign="top">[QColumn]</td><td valign="top">Question column - Outputs the question columns value.</td></tr><tr><td valign="top">[QID]</td><td valign="top">Question ID - Outputs the Question ID text.</td></tr><tr><td valign="top">[QKey]</td><td valign="top">Key number for question (guaranteed unique) - Outputs a number that is guaranteed to be unique for each question. You should consider this to be a random number. It will not change as long as the study is stored in Ascribe. It will change if you save the study and restore it.</td></tr><tr><td valign="top">[QLabel]</td><td valign="top">Question label - Outputs the Question label text.</td></tr><tr><td valign="top">[QResponsesCoded]</td><td valign="top">Responses coded - Outputs the number of responses that have been coded for the current question.</td></tr><tr><td valign="top">[QResponsesCurrent]</td><td valign="top">Responses after reclassify - Outputs the current number of responses stored for this question. It is possible for this number to be larger than the number of responses loaded, because a response may have been reclassified to this question from another question in the study.</td></tr><tr><td valign="top">[QResponsesLoaded]</td><td valign="top">Responses loaded - Outputs the number of responses that were loaded for this question. It is possible for this number to be smaller than the number of responses currently stored for this question, because a response may have been reclassified to this question from another question in the study.</td></tr><tr><td valign="top">[QResponsesRef]</td><td valign="top">Responses currently referred - Outputs current number of responses to this question that have been referred to supervisor for help.</td></tr><tr><td valign="top">[QText]</td><td valign="top">Question text - Outputs the question text.</td></tr><tr><td valign="top">[QType]</td><td valign="top">Question type (0: Open, 1: Closed, 2: Other specify, 3: Value) - Outputs a number as listed above that specifies the type of the question. If you want the name of the question type instead, use [QTypeName]</td></tr><tr><td valign="top">[QTypeName]</td><td valign="top">Question type - Outputs the name of the question type, for example Closed.</td></tr><tr><td valign="top"><strong>Study</strong></td><td valign="top"> </td></tr><tr><td valign="top">[SCardCols]</td><td valign="top">Columns per card/respondent - Outputs the Columns per card/respondent value for the study.</td></tr><tr><td valign="top">[SCardNumCol]</td><td valign="top">Card number column - Outputs the Card number column value for the study.</td></tr><tr><td valign="top">[SCardNumCols]</td><td valign="top">Card number columns - Outputs the Card numbers column value for the study.</td></tr><tr><td valign="top">[SClosedQuestions]</td><td valign="top">Closed questions - Outputs the number of closed questions in the study.</td></tr><tr><td valign="top">[SResponsesCoded]</td><td valign="top">Responses coded - Outputs the number of responses that have been coded for all questions in the study.</td></tr><tr><td valign="top">[SCodesApplied]</td><td valign="top">Codes applied - Outputs the number of codes applied for all questions in the study.</td></tr><tr><td valign="top">[SDesc]</td><td valign="top">Study description - Outputs the Study description text.</td></tr><tr><td valign="top">[SID]</td><td valign="top">Study ID - Outputs the Study ID text.</td></tr><tr><td valign="top">[SName]</td><td valign="top">Study name - Outputs the Study name text.</td></tr><tr><td valign="top">[SOpenQuestions]</td><td valign="top">Open questions - Outputs the number of open questions in the study.</td></tr><tr><td valign="top">[SOSQuestions]</td><td valign="top">Other specify questions - Outputs the number of Other specify questions in the study.</td></tr><tr><td valign="top">[SResponses]</td><td valign="top">Responses - Outputs the total number of responses to all questions currently stored for the study.</td></tr><tr><td valign="top">[SRespondents]</td><td valign="top">Respondents - Outputs the total number of respondents to all questions currently stored for the study. This is the number of responses that have a unique respondent ID.</td></tr><tr><td valign="top">[SRIDCol]</td><td valign="top">Respondent ID column - Outputs the Respondent ID column value for the study.</td></tr><tr><td valign="top">[SRIDCols]</td><td valign="top">Respondent ID columns - Outputs the Respondent ID columns value for the study.</td></tr><tr><td valign="top">[SValueQuestions]</td><td valign="top">Value questions - Outputs the number of Value questions in the study.</td></tr></tbody></table>
