---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/ascribe-coder/coding-assistant
---

# Coding Assistant

The intention of Coding Assistant is to reduce manual coding time. Coding Assistant monitors coding activity in Ascribe Coder. It suggests responses to code based on their similarity to the most recently coded responses. The user can accept one or more suggestions to cause the same codes to be applied to these responses.

## License Required <a href="#minitocbookmark2" id="minitocbookmark2"></a>

Coding Assistant is available on an account only if it has been given the Coding Assistant license. A user must also be given the Coding Assistant privilege (see [Associates](../user-administration/associates.md) page.)

## Theory of Operation <a href="#minitocbookmark3" id="minitocbookmark3"></a>

Coding Assistant works by computing the similarity between all responses in a question. The strings considered are the text of the coding source for the question.

If a question has N responses, then the number of pairs is N(n-1)/2. If the question has 1000 responses, the number of pairs to consider is 449,500...nearly half a million If we have 10,000 responses, the number of pairs is 49,995,000...nearly 50 million!

For Coding Assistant, we use a technique called paraphrase mining. Its job is to consider each pair of strings and determine a similarity value between each pair of strings. This is a decimal value ranging from 0 to 1. Low values mean the strings are not similar, and high values mean the strings are very similar.

If we were to store all the similarity values, we would store a lot of numbers. But in practice, we do not care about dissimilar pairs. We only want pairs that are fairly similar. So, we discard the similarity values unless they are greater than some threshold (currently 0.8). This keeps the size of the stored similarity values manageable.&#x20;

Now suppose the user codes a response. With our stored similarity information, we can ask, "what responses are similar to the ones the user just coded?" We use this to provide a set of suggestions for other responses to code. The suggestions are simply those responses that are similar to the ones just coded.

There are two good things about this approach:

* We only need to compute the similarity values when the responses are just loaded (or have changed). Hence, we do not need to run any (slow) NLP processing when the user is coding away.
* Once we have computed the similarities, the process of finding similar strings is fast, very fast.

The paraphrase mining operation runs in an AWS lambda function. This is a serverless technology that lets us run paraphrase mining on any number of questions in parallel. In practice, paraphrase mining for questions with a few hundred responses takes about 10 seconds to a minute. The times increase with the number of responses, but even questions with 100,00 responses run in a few minutes.

## Coding Assistant in Action <a href="#minitocbookmark4" id="minitocbookmark4"></a>

Coding Assistant displays at the bottom of the Responses Pane. The bar is gray until you start coding.

![](https://static.goascribe.com/Help/coding_assistant_is_gray.png)

The bar changes colors as you code:

* Gray: you have not coded anything yet, so there are no suggestions.
* Red: you coded something, but the similarities for this question have not been calculated yet.
* Yellow: you coded something, and the similarities are calculated, but Coding Assistant found no responses similar to those you coded.
* Green: you coded something, and Coding Assistant found and displayed some similar response for you to approve.

## Suggestions <a href="#minitocbookmark5" id="minitocbookmark5"></a>

When suggestions are available, the bar is green. To see the suggested responses, drag the bar up.

In this example, four Nothing responses were manually coded (applied the code and used Code Duplicates to code exact text matches.) Coding Assistant then suggested similar response

![](https://static.goascribe.com/Help/Coding_assistant_suggestions.png)

&#x20;The blue text below the toolbar is the response that was just coded. The green text is the applied code.&#x20;

Below the blue text are the responses that Coding Assistant thinks are similar. You check or uncheck these to accept or reject the suggestion. You can select all the suggestions by checking the blue response. You can shift/click to check a range of responses.

The list of suggestions are ordered by similarity and are not in alpha order. The ones listed first are considered to be the most similar.

After you check a suggestion, the Code Selected Suggestions button is active. If you click it, Coding Assistant will code these responses with the code(s) you just applied.

After you click the button, the suggestions disappear, and Coding Assistant is waiting for you to code more responses. Note that Coding Assistant may find more suggestions similar to the suggestion you just coded, and they will display in the same format.

To select all of the suggestions, click the checkbox next to the blue response or click the number next to the Code Selected Suggestions button.&#x20;

Use the blue expand/collapse arrow next to the blue response to hide or display the suggestion

If a response already has a code applied, the code displays underneath the response (see example below.) You can still apply the additional code.

![](https://static.goascribe.com/Help/response_has_been_coded.png)

## Coding Assistant Toolbar Layout <a href="#minitocbookmark6" id="minitocbookmark6"></a>

![](https://static.goascribe.com/Help/Coding_assistant_layout_01.png)

The toolbar has this format when there are suggestions:

<table><thead><tr><th width="237.333251953125" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">N / N Suggestions</td><td valign="top">This field lists the number of displayed suggestions followed by the number of total suggestions. When the slider is all the way to the right (at All), all suggestions, excluding duplicates, are displayed. When the slider is not on All, these numbers let you know that there may be other suggestions that are not displayed. Duplicate responses will be coded.</td></tr><tr><td valign="top">Collapse/Expand Coding Assistant Pane</td><td valign="top">Use the up/down arrow to collapse or expand the Coding Assistant pane.</td></tr><tr><td valign="top">Code Selected Suggestions</td><td valign="top">This button is not active until a suggestion is selected. Click the button to code selected suggestions with the same code(s) you just applied.</td></tr><tr><td valign="top">Number of Suggestions Selected for Coding</td><td valign="top">This number displays after the Code Selected Suggestions button. Click it to toggle select all/none.</td></tr><tr><td valign="top">Settings</td><td valign="top"><p><strong>Suggest as you code:</strong></p><ul><li><strong>Suggest uncoded responses only -</strong> As the user codes, Coding Assistant will only show suggestions for uncoded responses.</li><li><strong>Sort coded responses by:</strong> confidence (the responses that Coding Assistant is most confident in are at the top of the list), text or text length.</li><li><strong>Sort suggested responses to code by:</strong> confidence, text or text length</li></ul><p><strong>Suggest all:</strong></p><ul><li><strong>Maximum number of codes to suggest for a response -</strong>increase or decrease the number as you would like.</li><li><strong>Sort -</strong> Select the sort option for responses (confidence, text, or text length) and codes (confidence, position in codebook, or text).</li></ul></td></tr><tr><td valign="top">Lightning Mode</td><td valign="top"><p>Lightning Mode allows you to code responses based on currently coded responses.</p><p>The Suggest All section in the Settings dialog controls the number of codes applied to a response and the order they are applied.</p></td></tr><tr><td valign="top">Suggestion Amount Slider</td><td valign="top">Move the slider to the right to see more or all suggestions, and move it to the left to see fewer suggestions.</td></tr></tbody></table>

## Coding Assistant and Filters <a href="#minitocbookmark7" id="minitocbookmark7"></a>

Coding Assistant respects all of the filter settings in the [Filter dialog of Ascribe Coder.](response-filters-and-sorting.md)&#x20;

It does not respect the filters found in the Search dialog. For example, it does not respect a regular expression search; it does not restrict the suggestions to only those that match the regular expression.&#x20;

## How to Apply Multiple Codes with Coding Assistant <a href="#minitocbookmark8" id="minitocbookmark8"></a>

Keep in mind that Coding Assistant only applies the last code applied; the code in green is what will be applied.

![](https://static.goascribe.com/Help/response_has_two_codes.png)

To apply multiple codes to suggested responses, use 'target' coding with the [Apply Selected Codes button](responses-settings.md#minitocbookmark2) found in Responses Settings.&#x20;

Here is an example:

![](https://static.goascribe.com/Help/both_codes_would_be_applied.png)

## Inconsistently Coded Responses <a href="#minitocbookmark9" id="minitocbookmark9"></a>

As you are working with Coding Assistant, you may notice suggested responses that have a red question mark next to them. The question mark is a sign that duplicate responses have been coded inconsistently. Click the question mark to see the various ways the responses were coded. See example below.

![](https://static.goascribe.com/Help/example_of_inconsistent_coding_3.jpg)

## Other Considerations <a href="#minitocbookmark10" id="minitocbookmark10"></a>

* Coding Assistant will only display a suggestion if it does not already have all the codes you just applied in the Responses pane.
* If two suggestions differ in case alone, only the first is displayed. If you accept the suggestion, both will be coded.
* Coding Assistant keeps a cache of suggestions in memory, to increase performance. These will be kept in memory for a maximum of five minutes.
* Coding Assistant calculates a checksum for the coding source strings for each question. If the checksum of the store set of calculated similarities differs from the current checksum for the question, then the stored set of similarities is discarded and recalculated. This will happen when more responses are added to the question, a response is modified, or the coding source is changed. When this happens, it can take up to five minutes before the new similarities are calculated. This will not affect the accuracy of suggestions, but does mean the Coding Assistant may not product all possible suggestions until the similarities are recalculated.
* The number of transactions charged for a response code by Coding Assistant is no different than for manual coding.
* Responses coded by accepting suggestions from Coding Assistant have their coding method set to Coding Assistant. You can filter by coding method to display these coded responses.
