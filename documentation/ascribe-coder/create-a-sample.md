---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/ascribe-coder/create-a-sample
---

# Create a Sample

Samples are a way to look at a portion of the data; they are simply a named sub-set of the responses. The sample responses are still part of the source responses and do not exist separately. If you delete the source of the sample, the sample is also deleted. A sample cannot be edited and remain valid.

Samples can be helpful if you load a large number of responses and only want to code part of them. Or you can just use it as a way to filter the responses by a particular word or concept and be able to return to that sub-set. The sample could be used for a partial quality review of coding.

Samples improve the performance of Ascribe Coder when you are working on a filtered set of responses. Suppose for example you are coding a question where you need to apply a filter for responses based on two closed-end questions, say Gender and Region. Let's say you need to filter by respondents who answered Female to the Gender question and East to the Region question. You can do this by setting the desired filter in the Filters and Sorting dialog. Now you are coding the desired set of respondents. But, Ascribe Coder must apply this filter every time you search for responses. Complex filters can slow the performance of Ascribe Coder. You can improve performance by creating a sample of the filtered responses and coding the sample. Since the sample is already filtered for the desired responses, Ascribe Coder can display the responses faster.

Another reason for coding from a sample is to change the base count. In the previous example, suppose that our original question had 1000 responses. When coding this question with the filter for Gender and Region applied, Ascribe Coder will still use 1000 as the base, because that is the number of responses in our source question. If you are coding the females in the Eastern region, there may be only 200 of them. You might want Ascribe Coder to use 200 as the base count. To do this, simply create a sample using this filter and code the sample. While coding the sample, the base count will be 200, because that is the number of responses in the sample.

To use a sample, see [Sources](sources.md). To view permanent samples created on the account, navigate to the [Samples page](samples-page.md) via Supervisor/Samples.

The Questions page has a column for Samples; a dot in the column indicates that a sample has been created for the question.

## Create a Sample using Ascribe Coder <a href="#minitocbookmark2" id="minitocbookmark2"></a>

To create a sample from within Ascribe Coder, display some responses. Right-click a response and select Create Sample. The Create Sample dialog opens with these fields:

<table><thead><tr><th width="199.3333740234375" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Temporary</td><td valign="top">If selected, the sample will be temporary. For more information, see Temporary Samples. If not selected, the sample displays on the Samples page and can be accessed by other users through the Samples tab of the Sources dialog.</td></tr><tr><td valign="top">ID</td><td valign="top">Temporary samples do not require an ID; a permanent sample requires a unique ID.</td></tr><tr><td valign="top">Description</td><td valign="top">This field is optional but can be used for information about the sample. It is initially populated with the study and question IDs from which the sample is taken.</td></tr></tbody></table>

All responses from the current search results are added to the newly-created sample, even ones on other pages of the search results.

When you create a sample with Ascribe Coder, you cannot select a certain percentage of the responses. The search results determine the number of responses in the sample.

To use a sample, see [Sources](sources.md).  To view permanent samples created on the account, navigate to the [Samples page](samples-page.md) via Supervisor/Samples.

The Questions page has a column for Samples; a dot in the column indicates that a sample has been created for the question.

## Temporary Samples <a href="#minitocbookmark3" id="minitocbookmark3"></a>

A temporary sample is available only to you, the person who created the sample. It exists only until you log out, at which time it is automatically deleted. When you create a temporary sample, you are not required to specify an ID for the sample.

When you create a temporary sample, Ascribe Coder immediately switches to using the temporary sample as the source of responses to code and clears any filters you have specified. Ascribe Coder clears your current filter settings because the sample is already filtered in this way, and the filters you had set are no longer needed. You can revert back to coding a set of questions using the Sources dialog.

## Create a Sample using Show Details/Question Details Dialog <a href="#minitocbookmark4" id="minitocbookmark4"></a>

To create a sample from the Questions page, right-click a question and select Show Details. Click the Samples tab. The View tab displays existing samples. Click the Create tab to create a new sample. See [Samples](../study/question-details-dialog.md#minitocbookmark10) for more information.

To use a sample, see [Sources](sources.md). To view permanent samples created on the account, navigate to the [Samples page](samples-page.md) via Supervisor/Samples.
