---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/client-access-to-data/client-reports/study-quality-report
---

# Study Quality Report

The Study Quality Report typically is used for training. It shows the difference between codes applied to a study and the saved set of 'quality codes' for the study. The intention of the quality report is to allow you to store a set of 'known good' codes for a study, and then compare a coder's work against this set.

**Location**: Supervisor/Right-click study/Select Reports/Click Quality

Quality coding refers to a process by which an expert codes a study "perfectly," or as close to the way it should be. After the study has been coded, it is converted to quality mode, and a trainee codes it. The trainee's coding is then compared to and measured against the expert’s coding. A report is created that shows the differences in coding.

### Set Quality Codes <a href="#minitocbookmark2" id="minitocbookmark2"></a>

**Location**: Supervisor/Studies/Right-click study/Select Set Quality Codes

To create quality codes, first you must have coded (or partially coded) a study. Then navigate to the Set Quality Codes screen. Select each question or group of questions for which you want to set quality codes and click OK.

When you set quality codes for a question, any existing quality codes are deleted and replaced with the current set of codes for the question. Questions you have not selected in the set quality codes window are not affected when you click the OK button.

You can set quality codes only for open or other specify questions.

After you set quality codes, you should delete the current coding. Navigate to the Questions screen, right-click any question, and choose Delete Questions. Select the questions for which quality codes have been set, and then choose "Codes" from the right-hand deletion column.&#x20;

Now the study is ready for the trainee to proceed with coding.

{% hint style="info" %}
#### Notes

* Any notes, translations, or transcriptions the expert coder added continue to display for the trainee unless you use Edit Responses to get rid of them.
* The codebook is already built for the trainee (otherwise the expert could not have coded the study.) Therefore, codes used for quality coding cannot be deleted from the codebook.
* If you need to delete the quality codes that have been applied, you use Delete Questions and choose Quality Codes for deletion.
{% endhint %}

### About the Study Quality Report <a href="#minitocbookmark3" id="minitocbookmark3"></a>

**Location**: Supervisor/Right-click study/Select Reports/Click Quality

The report lists each question in the study, and provides summary information about the difference between the codes applied and the quality codes.

<table><thead><tr><th width="265.333251953125" valign="top">Summary Information</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Total Responses</td><td valign="top">The number of responses to this question, both coded and uncoded.</td></tr><tr><td valign="top">Responses Coded</td><td valign="top">The number of responses that have at least one code applied, shown as a count and as a percentage of responses.</td></tr><tr><td valign="top">Responses Quality Coded</td><td valign="top">The number of responses that have at least one <strong>quality code</strong> applied, shown as a count and as a percentage of responses.</td></tr><tr><td valign="top">Responses Both Coded and Quality Coded</td><td valign="top">The number of responses that have at least one code and at least one <strong>quality code</strong> applied.</td></tr><tr><td valign="top">Codes Applied</td><td valign="top">The total number of codes (not <strong>quality codes</strong>) applied to responses in this question.</td></tr><tr><td valign="top">Quality Codes Applied</td><td valign="top">The total number of <strong>quality codes</strong> applied to responses in this question.</td></tr><tr><td valign="top">Codes Added</td><td valign="top">The number of codes applied to a response when there is no matching <strong>quality code.</strong></td></tr><tr><td valign="top">Codes Missing</td><td valign="top">The number of <strong>quality codes</strong> applied to a response where there is no matching code.</td></tr><tr><td valign="top">Quality Ranking</td><td valign="top">An index that scores the coder on their conformity to an expert’s results. The actual score consists of codes missing vs. the expert and codes added vs. the expert. Missing codes count off more than codes added. You may want to begin to take action if the ranking is below the 80<sup>th</sup> percentile. The quality ranking is only displayed to people with supervisory access or above. Clients may not see the quality ranking.</td></tr></tbody></table>

The idea of this report is to give an overview of how the coding of the question differs from the quality coding. The _Codes added_ and _Codes missing_ rows contain the important information. These are based only on those responses that have both a code and a **quality code** applied. In other words, it is based only on the responses listed in the _Responses both coded and quality coded_ row of the table.

* The _Codes added_ row lists the number of codes applied where there is no matching quality code. The coder has applied codes that the **quality coder** did not apply.
* The _Codes missing_ row lists the number of codes the coder "missed." The **quality coder** applied codes that the coder did not apply.

Percentile scores are assigned to the _Codes added_ and _Codes missing_ rows. These are intended merely to give a quick assessment of the overall quality. You should use the detailed report of the coding differences to assess quality issues, rather than relying on the percentile numbers.

The percentile ranking for _Codes added_ is calculated as: (1 - (Codes added) / (Correct codes)) \* 100, where (Correct codes) is the number of quality codes that match codes applied by the coder.

Similarly, the percentile rank for _Codes missing_ is: (1 - (Codes missing) / (Correct codes)) \* 100.

Finally the Quality ranking for the question is computed as the average of the Codes added and Codes missing percentiles.

You can see a detailed report of those responses that were coded differently if you click the ![](https://static.goascribe.com/Help/09_-_Client_Access_to_Data_julie_files/image024.gif) icon for the question.
