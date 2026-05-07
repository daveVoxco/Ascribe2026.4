---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/ascribe-coder/code-single-responses
---

# Code Single Responses

In the Single Response Coding mode, responses are presented one at a time. To use this mode, select the "Code single responses" setting in Responses Settings dialog or press Ctrl/Click on the Responses Settings icon.

![](https://static.goascribe.com/Help/Single_Response_coding_setting.gif)

## Display First Response <a href="#minitocbookmark2" id="minitocbookmark2"></a>

Simply click the forward arrow or the Tab key to display the first response to be coded.

![](https://static.goascribe.com/Help/Click_forward_arrow.gif)

## Messages <a href="#minitocbookmark3" id="minitocbookmark3"></a>

Here is an example of the Response pane with a response to be coded:

![](https://static.goascribe.com/Help/Single_Response_coding_aug_2021.png)

Note the messages that display in the toolbar. The yellow messages will let you know if the responses are filtered or sorted. For more information, see [Statistics for Displayed Responses](statistics-for-displayed-responses.md).

## Code Segments <a href="#minitocbookmark4" id="minitocbookmark4"></a>

The Code Segments option allows for users to highlight a piece of a response, apply code and retain the relationship between that piece (or segment) and the code. When you toggle on Code Segments and move to the first response, the screen adds a Create/View Segments pane, as shown below:

![](https://static.goascribe.com/Help/Code_Segments_option.png)

Both panes display the response text and scroll together. The left pane is for segment selection and display. The right pane displays the 'normal' view of the response and codes applied and has normal right-click menu features. The right pane can be hidden by clicking the Hide Response Pane button.

To select a segment, click and drag mouse over the response in the left pane while holding the mouse button down. When you release the mouse button, the selected text turns green, and will not disappear when you click a code or type. The selected segment displays in the non-scrollable pane at the top. See below.

![](https://static.goascribe.com/Help/selected_segment.png)

Apply a code (in any fashion - see[ Methods to Apply Codes](code-single-responses.md#minitocbookmark6).) The code is applied to the segment, which changes color.

The applied code displays below the response in the right pane.&#x20;

![](https://static.goascribe.com/Help/coded_segment.png)

The purple forward arrow indicates that segment coding was used. The [coding method](response-filters-and-sorting.md#minitocbookmark2) is marked as Code Segments.&#x20;

You can continue to create and code segments as you wish. The coded segments alternate colors.

You can apply multiple codes to a segment. A double line displays under a segment which has multiple codes applied.

When you hover over the coded segment, the applied code or codes display.&#x20;

![](https://static.goascribe.com/Help/hover_over_segment.png)

When you hover over the applied code in the right pane, the associated segment is highlighted in the right pane.

![](https://static.goascribe.com/Help/hover_over_applied_code.png)

You can change the coding as necessary (remove, add or swap codes as normal.)&#x20;

To remove a segment, remove the associated code.&#x20;

When using Code Segments,  [Drag Selected Responses to Codebook](responses-settings.md#minitocbookmark2) is ignored, and [Coding Assistant](coding-assistant.md) is not active. &#x20;

## How to Change Coding of Segments <a href="#minitocbookmark5" id="minitocbookmark5"></a>

In Single Response Coding mode, once you advance to the next response, you can't change the coding or the segments.

You can review the coding of segments in Multi Response Coding mode. You can swap codes to change the coding. You can also right-click a response and select Code Single Responses. This action returns that response to Single Response Coding mode where you can change the segments and codes. To remove a segment, remove the associated code. When you move forward, only uncoded responses will display. You can continue working there or change back to Multi Response Coding mode.

## Methods to Apply Codes <a href="#minitocbookmark6" id="minitocbookmark6"></a>

There are several ways to code in this mode:

* Click the regular expression hyperlink in the response; see [Regular Expressions](codebooks/regular-expressions.md) for more information.
* Click on a code in a codebook.
* Select any number of codes and hit the Apply Code target for individual responses. This method requires a Responses Settings configuration. The option to display the “Apply Selected Codes Button” must be toggled-on for this method to work.
* Drag a code to a response. &#x20;

Codes are applied immediately, just as in the Multiple Response pane. Click the forward arrow button or the Tab key to view the next response.

When a code is applied to a response, and until the newly applied code is displayed, the response is highlighted orange. This gives you a visual indication of response with a pending coding operation. Similarly, codes removed from a response are highlighted red until the code is removed from the display. If you do not want to see these highlights, you can turn them off with the [Pending Operation Highlights](responses-settings.md#minitocbookmark5) option on the Responses Settings/Appearance tab.

Note that the next response to code is also retrieved and locked. You will see that the forward arrow button goes dim just after clicking it. When it returns to normal, the next response is cached, and it will display immediately when you click the next button.

## Find Text Box <a href="#minitocbookmark7" id="minitocbookmark7"></a>

The Find text box at the top of the pane lets you find a code by output ID or code description. If the text you enter exactly matches the output ID of a code, that code is applied. Otherwise, the first code whose description contains the text you enter is applied.
