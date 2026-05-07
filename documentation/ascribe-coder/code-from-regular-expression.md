---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/ascribe-coder/code-from-regular-expression
---

# Code from Regular Expression

This features allows a user to code the responses using regular expressions defined in the codebook. Click the Code from Regular Expressions icon (<img src="https://static.goascribe.com/Help/code_from_regular_expressions.gif" alt="" data-size="line"> ) in the toolbar to open the Code from Regular Expressions dialog. The dialog has two tabs: [Apply Codes](code-from-regular-expression.md#apply-codes) and [Remove Codes](code-from-regular-expression.md#remove-codes). When using this feature, keep in mind considerations for [singleton codes in the codebook](code-from-regular-expression.md#singleton-codes-in-codebook), [display of distinct verbatim](code-from-regular-expression.md#display-distinct-verbatim), and [coding duplicate responses](code-from-regular-expression.md#code-duplicate-responses).

## Apply Codes

Here are the options for the Apply Codes tab:

<table><thead><tr><th width="238.66668701171875" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">X/Y codes have regular expressions</td><td valign="top">This statement indicates how many codes in the codebook have regular expressions. If the codebook doesn't contain any regular expressions, a message displays indicating there are no regular expressions and that this feature cannot be used.</td></tr><tr><td valign="top"><strong>Code Responses</strong></td><td valign="top"> </td></tr><tr><td valign="top">All</td><td valign="top">All responses in the question source will be coded according to regular expressions found in the codebook.</td></tr><tr><td valign="top">Uncoded</td><td valign="top">Only uncoded responses will be coded according to regular expressions found in the codebook.</td></tr><tr><td valign="top">Displayed</td><td valign="top">Only displayed responses will be coded according to regular expressions found in the codebook. If no responses are displayed, this option is grayed out/unavailable.</td></tr><tr><td valign="top"><strong>Codes To Apply</strong></td><td valign="top"> </td></tr><tr><td valign="top">All Matching Codes</td><td valign="top">Applies all codes when their expressions are found in the responses.</td></tr><tr><td valign="top">First Matching Code In Response</td><td valign="top">Applies only the first matching code found in the response; only 1 code per response is applied.</td></tr><tr><td valign="top"><strong>In Case Of Overlapping Matches</strong></td><td valign="top"><p>Some codes may have overlapping expressions. This section aids in deciding which code to apply. It is only displayed when All Matching Codes in the Codes to Apply section is selected; it is not applicable when only 1 code per response is applied.</p><p> </p><p>Codes that do not have overlapping expressions are also applied when this section is used.</p></td></tr><tr><td valign="top">Apply Code Matching Longer Text Match</td><td valign="top">Apply the code whose expression matches more text in the response.</td></tr><tr><td valign="top">Apply First Matching Code In Codeframe</td><td valign="top">Apply the code which appears first in the codeframe.</td></tr><tr><td valign="top">Apply All Codes</td><td valign="top">Apply all codes including ones that have overlapping expressions.</td></tr></tbody></table>

## Singleton Codes in Codebook

A code may be marked as a singleton, meaning it should not be applied to a response with any other code. (See [Singleton](codebooks/edit-code.md) for more information about how to designate a code as singleton.

If a response has already been coded with a singleton code, Code from Regular Expressions will ignore that response. No other codes will be added, no matter what options are selected.

If All Matching Codes is selected, all codes are applied and the singleton requirement is ignored. In this situation, a message displays indicating that a singleton code has been applied in addition to other codes. There is a link to the [Singleton tab in the Codebook Tools](codebooks/codebook-tools.md#singleton) dialog where you can see the problems. You can find where the code has been applied with other codes by searching for the code (right-click the code and select Search Any). When looking for singletons applied with other codes, it is helpful to sort the list of responses by the number of codes applied.&#x20;

## Code Duplicate Responses

When you have [Code Duplicates All](responses-settings.md#minitocbookmark4) selected in Responses Settings, this setting is ignored if you choose [Displayed in the Code Responses section](code-from-regular-expression.md). In this situation, a warning message indicates all duplicates may not be coded. Only the displayed responses are considered for coding when Displayed is selected.

## Display Distinct Verbatim

When you use the [Distinct Verbatim search](search-responses.md#minitocbookmark3), you only display the first occurrence of a duplicate response. If you choose [Displayed in the Code Responses section](code-from-regular-expression.md), only that first occurrence which is displayed would be coded. The other duplicates are not coded. To code all duplicates when using the Distinct Verbatim option, choose All or Uncoded in the Code Responses section.

## Remove Codes

Here are the options for the Remove Codes tab:

<table><thead><tr><th width="255.6666259765625" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">X/Y codes have regular expression codes applied</td><td valign="top">This statement indicates how many responses have codes applied by regular expression.</td></tr><tr><td valign="top"><strong>Remove Codes Applied From Regular Expressions</strong></td><td valign="top"> </td></tr><tr><td valign="top">All</td><td valign="top">Remove all codes applied by regular expression. Codes applied in another method are not removed.</td></tr><tr><td valign="top">Without Coding Quality Checked</td><td valign="top">If the coding has not been quality reviewed, remove the codes applied by regular expression. Codes applied in another method are not removed.</td></tr></tbody></table>

## View the Responses in Ascribe Coder

You can view the responses and applied codes in Ascribe Coder and make changes as necessary. You can view which segments received codes by selecting the [Code Segments on Hover](responses-settings.md#minitocbookmark4) option in the Applied Codes tab of Responses Settings.&#x20;
