---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/data-management/download-data/download-data-with-scripted-output/column-binary-output-script
---

# Column Binary Output Script

_Navigate: Client/Studies/Right-click study/Select Download Data/Select Scripted Output/Select Column Binary_\
_Supervisor/Studies/Right-click study/Select Download Data/Select Scripted Output/Select Column Binary_

This script generates a data file from the coded responses sometimes called **"Tabulation Data."** Account options or study setup determines how the data will be output when you choose to run this script.

On the Data Tab of the Study Edit screen, choose your desired file format (almost always ASCII) and layout formats (see [Layout Types](column-binary-output-script.md#minitocbookmark2).)

## Layout Types <a href="#minitocbookmark2" id="minitocbookmark2"></a>

There are three layout types available for questions. These layout types are used only for column binary output.

You can change the layout type if you edit the study. If the layout setting for the study is use question settings, then you can specify different layout types for each question in the study if you edit the question.

In column binary output, rows in the output file represent cards, and data locations on the cards are called columns. This terminology dates from the use of IBM punch cards for data. Column numbering starts at 1 and extends to the value of card number columns specified for the study.

In addition to code values, the respondent ID and card number are also output for each card. Ascribe always outputs one row (card) in the data file for each unique combination of respondent ID and card number. The respondent ID and card number fields are always output in numeric layout, regardless of the layout setting for the study and questions.

## Numeric Layout <a href="#minitocbookmark3" id="minitocbookmark3"></a>

Ascribe writes a card for each unique combination of respondent ID and card number. The Card field on the Data tab of the Edit Question page determines the card number for that question.

While numeric layout sounds as if it can only output numbers, you may use any ASCII character for the output ID of the codes.

In a numeric layout, the column binary output script contains the respondent ID followed by the code output IDs. The output is written across the card in this format:

<table><thead><tr><th width="229.33331298828125" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Respondent ID</td><td valign="top">The respondent ID starts in the column indicated by the <strong>Respondent Column</strong> on the Data tab of the Edit Study page. The length of the respondent ID is controlled by the <strong>Respondent ID Columns</strong> on the Data tab of the Edit Study page.</td></tr><tr><td valign="top">Starting Column</td><td valign="top">The first code for a question starts in the column indicated by the <strong>Column</strong> field. The Column field is on the Data tab of the Edit Question page.</td></tr><tr><td valign="top">Code Length</td><td valign="top">The length of the code output ID is set by the <strong>Columns</strong> field, which is on the Data tab of the Edit Question page. If the output ID is less than the Columns field, it will have leading zeroes.</td></tr><tr><td valign="top">Successive Codes</td><td valign="top"><p>Codes for each question follow one another.</p><p>Here are some examples:</p><p>Question 1 has 20 in the <strong>Column</strong> field and 3 in the <strong>Columns</strong> field.</p><ul><li>The first code is written in columns 20, 21, and 22.</li><li>The next code is written in 23, 24, and 25, and so on.</li></ul><p>Question 2 has 50 in the <strong>Column</strong> field and 3 in the <strong>Columns</strong> field.</p><ul><li>The first code for Question 2 is written in 50, 51, and 52.</li><li>The next code is written in 53, 54, and 55, and so on.</li></ul></td></tr><tr><td valign="top">Number of Columns Used by a Question</td><td valign="top"><p>You can see the number of columns used by each question on the Card Layout Report. The number of columns used by a question depends on the <strong>Maximum Codes</strong> field on the Data tab of the Edit Question page.</p><ul><li><strong>If the Maximum Codes field equals zero</strong>, an unlimited number of codes may be written to the output, and you cannot determine in advance the number of columns a question will use.</li><li><strong>If the Maximum Codes field is greater than zero</strong>, the number of codes written to output is limited to that number. (The Maximum Codes field does not affect the number of codes a coder may apply; it only affects output.) <strong>The number of columns used equals Maximum Codes multiplied by the Columns field.</strong></li></ul></td></tr></tbody></table>

## Punch Layout <a href="#minitocbookmark4" id="minitocbookmark4"></a>

Ascribe writes a card for each unique combination of respondent ID and card number. The Card field on the Data tab of the Edit Question page determines the card number for that question.

In a punch layout, the column binary output contains the respondent ID followed by a single digit which represents the code output ID. The output is written across the card in this format:

<table><thead><tr><th width="221.3333740234375" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Respondent ID</td><td valign="top"><ul><li>The respondent ID starts in the column indicated by the <strong>Respondent Column</strong> on the Data tab of the Edit Study page.</li><li>The length of the respondent ID is controlled by the <strong>Respondent ID Columns</strong> on the Data tab of the Edit Study page.</li></ul></td></tr><tr><td valign="top">Punch Value of the Code Output ID</td><td valign="top"><p>A single bit or digit represents each applied code in the output file. This bit is the <strong>rightmost digit of the code output ID</strong> and is called the punch value.</p><ul><li>For example, output ID 123 has a punch value of 3.</li></ul></td></tr><tr><td valign="top">Punch Column</td><td valign="top"><p>The column where the bit is written is determined by the <strong>digits in the output ID to the left of the punch value</strong>.</p><ul><li>For example, output ID 123 would have a 3 written or punched at column 12.</li></ul></td></tr></tbody></table>

Punch layout also has these rules:

* **The rightmost digit of the output ID (the punch value) must be a digit or the characters ‘x’, ‘X’, ‘y’, ‘Y’, ‘&’, or ‘-‘.**
* **The column characters in the output ID must be digits.**
* **A single digit is not allowed to be an output ID.** Ascribe interprets a single digit output ID as having zeroes in front of the punch value, and there is no column 0 on a card. The Card Layout Report detects this problem, and the Column Binary Script will fail if the problem is not corrected.
* **Duplicate code output IDs are not allowed**. Duplicate output IDs would punch the same value in the same column for both codes. There would be no way to determine which code was output. The Card Layout Report detects this problem, and the Column Binary Script will fail if the problem is not corrected.

Here are some examples of output IDs and how they are used:

* 142 – Punch 2 at column 14.
* 3 – Punch 3 at column 0; not allowed since there is no column 0 on a card.
* 12Y – Punch Y at column 12.

## Punch Using Column Offset Layout <a href="#minitocbookmark5" id="minitocbookmark5"></a>

Punch using column offset layout is similar to the punch layout. **However,** **the column where the code is written or punched is determined in a different way.**

The output is written across the card in this format:

<table data-header-hidden><thead><tr><th width="217.333251953125" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Respondent ID</td><td valign="top"><ul><li>The respondent ID starts in the column indicated by the <strong>Respondent Column</strong> on the Data tab of the Edit Study page.</li><li>The length of the respondent ID is controlled by the <strong>Respondent ID Columns</strong> on the Data tab of the Edit Study page.</li></ul></td></tr><tr><td valign="top">Punch Value of the Code Output ID</td><td valign="top"><p>A single bit or digit represents each applied code in the output file. This bit is the <strong>rightmost digit of the code output ID</strong> and is called the punch value. <strong>(This part is the same as the punch layout.)</strong></p><ul><li>For example, output ID 123 has a punch value of 3.</li></ul></td></tr><tr><td valign="top">Punch Column</td><td valign="top"><p>The column where the bit is written or punched is determined by the <strong>digits in the output ID to the left of the punch value plus the Column field.</strong> (The Column field is set on the Data tab of the Edit Question page.) Simply drop the punch or last digit of the output code value, and then add the remaining number to the Column field.</p><p>For example:</p><ul><li>The output ID is 123, and the Column field is 20.</li><li>The punch value is 3.</li><li>The punch column is equal to the digits to the left of the punch value (12) + the Columns field (20) or 32.</li><li>3 would be written at column 32.</li></ul></td></tr></tbody></table>

**Another difference from the punch layout is that a code output ID can be a single digit.** Here is an example:

* The Column field is 20, and the output ID is 5.
* Ascribe interprets the output ID as 005.
* The punch value is 5.
* The punch column is computed as 0 + 20 = 20.
* Therefore, 5 would be written at column 20.

Here are some examples of output IDs and how they are used when the Column field is 10:

* 142 – Punch 2 at column 24 (14 + 10).
* 3 – Punch 3 at column 10 (0 + 10).
* 12Y – Punch Y at column 22 (12 + 10).

{% hint style="info" %}
#### Note

Remember, Punch using Column Offset is dependent upon the Column field on the Edit Question page.
{% endhint %}

Remember to simply drop the punch or last digit of the output code value, and then add the remaining number to the Column field on the Edit Question page.

For instance, in the Question Edit box your Card is 41 and the starting column is 10.

* The codebook is numbered starting at code 1 and incrementing by 1.
* Then Codes 1 through 9 will be Card 41, Column 10, punches 1 through 9 or the equivalent of 101, 102, 103, 104, 105, 106, 107, 108, 109 in a regular Punch codebook.
* Codes 10 through 19 will be Column 11, punches 0 through 9 or 111, 112, 113, 114, 115, 116, 117, 118, 119 in a regular Punch codebook.

If the last code is 68, that is an 8 punch in column 16 (drop the 8 then add 6 to 10)—but if the starting column is 25, then code 68 would be an 8 punch in column 31 (drop the 8 add 6 to 25 to get 31).

### **Reasons to Use Punch Using Column Offset**

* Punch using column offset gives you more flexibility when you deliver a study. You can keep codebooks shared and numbered the same, but still output each question to separate columns.
* You share codebooks and want to maintain the share but still output each question to a different starting column (often used for trackers.)
* You have a tracker that maintains the same questions with the same codebooks. You want to retain their original punches, but the column locations change each month. (This used to be a tedious process that required careful renumbering of each code.)
* You output Quantum Edit specs and need to write across cards. This requires both the card value and the column value to be concatenated into one number and entered as the Column value on the Edit Question screen.

For instance, card 10 column 08 would be 1008. Now, to write to the next card (card 11), you simply figure out what it would take to jump from 1008 to 1108, meaning increment anything writing to card 11 by 100. An example, you have a code that the data analyst needs to fall on card 11, column 08, punch 3. The rest of the codebook needs to write to card 10 starting with column 08 punch 1. All of the codebooks can be numbered normally, starting with 1 by increments of 1 except for the oddball Card 11 code. This code will be numbered 1003 because 100 plus 1008 equals 1108 which deciphers to Card 11 column 08.

### Study and Question Setup Example

Study Setup for Punch Using Column Offset:

![](https://static.goascribe.com/Help/Study_Setup_for_Punch_Using_Column_Offset.gif)

Questions Setup for Punch Using Column Offset:

<figure><img src="https://static.goascribe.com/Help/Question_Setup_for_Punch_Using_Column_Offset.gif" alt=""><figcaption></figcaption></figure>

When setting up a study as Punch Using Column Offset, one major difference takes place from the Punch setting: the Column field from the Edit Question page becomes active. (See below). When a study is set up as Punch, Column means absolutely nothing to the deliverables at the end of the study. The data will be output the same way no matter what the Column field contains. Punch Using Column Offset changes that completely. The Column for each question tells Ascribe where to start writing the data. It also tells Ascribe that each code will be offset by that column number. This allows the codebooks to be numbered starting at 1 by increments of 1. The output code value of Column Using Punch Offset codebooks represents the punch (the single digit to the rightmost of the Output value will be the punch) and the number that the Column will be offset by (any numbers to the left of the punch will offset the Column). This is really a simple math game.

Q8 below will start in column 40. The codebook is numbered 1-???. Let’s look at a few codes from the Q8 codebook.

![](https://static.goascribe.com/Help/Codebook_Example.gif)

* Code 11 will be written to Column 41 Punch 1 or 41’1.\
  Here’s the math: Drop the punch off the code value (Remember the punch is the digit farthest to the right). That leaves us with 1. Add that 1 to the column (40) and you get column 41. Now we bring the punch back up and get 41’1.
* Code 14 will be written to Column 41 Punch 4 or 41’4\
  Here’s the math: Drop the punch off the code value (Remember the punch is the digit farthest to the right). That leaves us with 1. Add that 1 to the column (40) and you get column 41. Now we bring the punch back up and get 41’4.
* Code 236 will be written to Column 63 Punch 6 or 63’6 Here’s the math:\
  Drop the punch off the code value (Remember the punch is the digit farthest to the right). That leaves us with 23. Add that 23 to the column (40) and you get column 63. Now we bring the punch back up and get 63’6.

Card Layout Report for Punch Using Column Offset:

![](https://static.goascribe.com/Help/Card_Layout_Report_for_Punch_Using_Col_Offset.gif)

&#x20;Tabulation Data for Punch using Column Offset:

![](https://static.goascribe.com/Help/10_-_Data_Management_recd_020909_julie_files/image052.jpg)

### More Information about 1130 Column Binary Setup and Output <a href="#minitocbookmark6" id="minitocbookmark6"></a>

Use the [Card Layout Report](../../../client-access-to-data/client-reports/card-layout-report.md) under Client/Reports to check the layout of you data before you use the Column Binary scripted output. The Card Layout Report allows the user to check all aspects of setup to make sure the data will be written out as desired. It also tells the user where problems with the layout might exist.

When downloading the data using the binary option (as opposed to the ASCII option under Study Setup), it will be written in what is referred to as 1130 column binary. This refers to the bit configuration in the resulting two-byte words. To read the file with a utility called MTR, use this syntax:

```
mtr -1 –r192 –b192 –i<filename> -o<filename
```

Where:&#x20;

* r = the record length
* b = blocking factor
* i = input filename
* o = output filename

The record length will be 2 times the number of columns that are in your output file plus 2. In the example above, there are 80 columns of data with a record terminator of two bytes (hence the plus 2). The blocking factor should be exactly the same as the record length.
