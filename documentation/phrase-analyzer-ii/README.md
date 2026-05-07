---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/phrase-analyzer-ii
---

# Phrase Analyzer II

The Phrase Analyzer II feature is useful for coding short response answers, like other specify and brand lists. With it, you can code responses to all questions that share a codebook, code responses automatically, and create codebooks.&#x20;

There are two basic ways to use Phrase Analyzer II:

* When you already have a codebook in place, like a brand list
* When you create a codebook from the loaded data.

## Training Video <a href="#minitocbookmark2" id="minitocbookmark2"></a>

{% embed url="https://www.youtube.com/watch?v=C7soBMRSSaM" %}

### Theory of Operation <a href="#minitocbookmark3" id="minitocbookmark3"></a>

Phrase Analyzer II operates on segments of responses, rather than on the full response text. It analyzes the uncoded responses and breaks them into segments as specified by user-provided delimiters. This analysis is deleted about 30 days after the most recent update to the analysis.  The analysis is unique to the user, codebook, and source questions.&#x20;

Each time the data structure is modified, a copy is made and operations can be undone to the point at which the segmentation analysis was created. The analysis is always updated if the user makes any changes, and is deleted and replaced by a new analysis if the user creates a new analysis.&#x20;

On entry to the page, and if there is any ambiguity about which questions should be analyzed, the user is prompted to confirm which questions to consider. This can occur, for example, if the codebook for the question is shared by other questions with uncoded responses. Once the set of questions is determined, if there is no analysis stored the user is prompted for the analysis options, and a new analysis is created and displayed. In the case where there is a single question sharing the codebook and there is an existing analysis, the analysis is simply displayed and the user is not prompted for any information.

## Page Layout <a href="#minitocbookmark4" id="minitocbookmark4"></a>

The page is laid out identically to Ascribe Coder, with three panes. The left pane shows text to be coded. It displays response segments with their associated counts. Segments from coded responses are never displayed in the left pane. When you apply a code to a segment, the segment is removed from display (if all segments in the response are coded.)

The right pane displays the codebook. The codebook can contain existing codes and/or allow for new codes to be created.

The bottom pan displays the questions that are being coded. These questions must all share the same codebook. The questions may span multiple studies. The text to be segmented is determined by the coding source for each of the questions, which may differ from one question to another.

![](https://static.goascribe.com/Help/PAII_layout.png)

## Process for the Initial Analysis/Segmentation of the Data

The first step is to select the source for analysis. When you enter the page, the Sources dialog displays with available questions. Select questions from the left pane and move them to the right pane. Only shared questions display in the left pane. Questions may span multiple questions.&#x20;

Next, the [Segmentation Settings dialog](segmentation-settings.md) displays. Select the options and click OK to start the analysis. The responses are split into segments and display with their corresponding count.&#x20;

## Response Pane Toolbar <a href="#minitocbookmark6" id="minitocbookmark6"></a>

Here are the options on the Response Pane Toolbar:

<table><thead><tr><th width="295.3333740234375" align="center" valign="top">Icons</th><th valign="top">Description</th></tr></thead><tbody><tr><td align="center" valign="top"> <img src="https://static.goascribe.com/Help/Navigation_Icon_02.gif" alt="">  <br>Navigation</td><td valign="top">Click the Navigation icon to access the Sources dialog, the Questions page, Ascribe Coder and other main navigation items.</td></tr><tr><td align="center" valign="top"> <img src="https://static.goascribe.com/Help/Suggest_Codes.png" alt=""> <br>Suggest Codes</td><td valign="top"><p>This option is used to match segments to existing codes in the codebook based on this criteria in the<a href="phrase-analyzer-ii-settings.md"> Settings dialog</a>:</p><ul><li>If the input ID of the code matches the segment by case insensitive comparison, it is a match</li><li>Otherwise, if the regular expression of the code matches the segment, it is a match</li><li>Otherwise, if the description of the code is the same as the segment it is a match.</li></ul></td></tr><tr><td align="center" valign="top"><img src="https://static.goascribe.com/Help/Apply_codes_paii.png" alt=""> <br>Apply Codes</td><td valign="top">This icon is active once a segment is marked with a provisional code. Click the icon to apply the codes.</td></tr><tr><td align="center" valign="top"><img src="https://static.goascribe.com/Help/Clear_suggestions.png" alt=""> <br>Clear Suggestions</td><td valign="top">This icon is active once a segment is highlighted. Click the icon to clear coding marks from the highlighted segments.</td></tr><tr><td align="center" valign="top"><img src="https://static.goascribe.com/Help/Create_codes_from_selected_segments.png" alt=""> <br>Create Codes From Selected Segments</td><td valign="top">Creates codes in the codebook from the highlighted segments. The codes are inserted in the codebook at the top and in segment order (the last selected segment will be first in the codebook.)</td></tr><tr><td align="center" valign="top"><img src="https://static.goascribe.com/Help/Combine_selected_segments_into_last_selected_segment.png" alt=""> <br>Combine Selected Segments Into Last Selected Segment</td><td valign="top">Combines segments (source segments) into the last selected segment (target segment). If the source segments have marks, they are discarded.</td></tr><tr><td align="center" valign="top"><img src="https://static.goascribe.com/Help/Discard_all_segments.png" alt=""> <br>Discard All Segments And Create New Segments (Cannot Be Undone)</td><td valign="top">Opens the <a href="segmentation-settings.md">Segmentation Settings dialog</a>. Clicking OK re-segments all uncoded responses and saves the segmentation, replacing any previously-saved segmentation.</td></tr><tr><td align="center" valign="top"><img src="https://static.goascribe.com/Help/paii_settings.png" alt=""> <br>Settings</td><td valign="top">Opens the <a href="phrase-analyzer-ii-settings.md">Settings</a> dialog.</td></tr><tr><td align="center" valign="top"><img src="https://static.goascribe.com/Help/paii_undo.png" alt=""> <br>Undo Last Action</td><td valign="top">Undoes the last operation that modified the segmentation analysis. any highlights on segments are discarded. The operation also undoes addition of codes to the codebook and applying codes to responses. It does not undo capitalization or renumbering of the codebook.</td></tr><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/paii_delete_icon.png" alt=""></p><p>Delete Selected Segments</p></td><td valign="top">This icon is active if at least one segment is highlighted. It removes selected segments from the segmentation analysis.</td></tr><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/Toggle_codebook_view.png" alt=""></p><p>Toggle Codebook View</p></td><td valign="top">Click this icon to display the codebook in alphanumeric order with the number of responses coded in parentheses. Click the drop-down arrow to display the unique responses that were coded. Click the icon again to return to the original display.  </td></tr><tr><td align="center" valign="top"><img src="https://static.goascribe.com/Help/selection_count.png" alt=""> <br>Selection Count</td><td valign="top">Displays the number of highlighted segments. If the count is zero, clicking the count selects all segments. If the count is greater than zero, clicking the count clears all segment highlights.</td></tr><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/paii_search_text_box.png" alt=""></p><p>Search Text Box</p></td><td valign="top">Enter search criteria to filter the segments.</td></tr><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/paii_sort.png" alt=""></p><p>Sort Options</p></td><td valign="top">Sort the segments by frequency, state (marks are applied), text, or length. Use the arrow to reverse the order (low to high, etc.)</td></tr></tbody></table>

## Codebook Toolbar <a href="#minitocbookmark7" id="minitocbookmark7"></a>

The Phrase Analyzer II codebook pane toolbar is very similar to the [codebook toolbar in Ascribe Coder](../ascribe-coder/#minitocbookmark6). However, there is no access to Codebook Builder, and there is an option to send feedback about Phrase Analyzer II to Support.&#x20;

## Segments and Marks <a href="#minitocbookmark8" id="minitocbookmark8"></a>

A _segment_ is string of non-zero length, with no leading or trailing whitespace. Segments display in lower-case text. Segments are constructed only from contiguous characters in the set of responses analyzed. &#x20;

A _mark_ is a provisional code applied to the segment, and in turn applied to the verbatims from which the segment was derived when the user applies codes. The user creates marks by various operations that match segments to codes in the codebook. Marks can never overlap, and each mark specifies exactly one provisional code. Marks are displayed in the segment in blue font with underscore. The code associated with a mark is displayed in hover help when the mouse is over the mark. A segment may have only one mark for a given code.

A given segment is contained in one or more verbatims, and each of those verbatims in turn has one or more segments. We call all these segments the segment's _associated segments_.

A given segment can be in one of five states:

* **Unmarked** (white)\
  None of the associated segments has any marks. When a segmentation analysis is initially created, all segments are in this state.
* **Orphaned** (red)\
  The segment does not have a mark, but at least one of the associated segments does.
* **Partially marked** (orange)\
  The segment has a mark, but at least one of the associated segments has no marks and no segment is fully marked.
* **Some fully marked** (green/yellow)\
  The segment has a mark, and at least one, but not all, verbatims have marks on all segments.
* **All fully marked** (green)\
  The segment and all associated segments have a mark.

The segment state is indicated by the color of the left edge of the segment in the user interface.

## Selecting Segments <a href="#minitocbookmark9" id="minitocbookmark9"></a>

There are several ways to select segments:

* Click a row
* Click the checkbox at the beginning of a row
* Select multiple rows using Shift/Click.

## Split Segments with Ctrl/Click <a href="#minitocbookmark10" id="minitocbookmark10"></a>

You may want to split a segment into different parts in order to apply multiple codes to the segment. You can split segments using a [text selection method](./#minitocbookmark13) or by using Ctrl/Click. On the Mac, use&#x20;

To add a split-mark to a segment, hold the Ctrl key and left-click at the point you want the split-mark to appear. The split-mark displays as a vertical red line at the point of the click. You can't put a split-mark on a code-mark (the blue underline).

Split-marks can be placed on only one segment at a time. If you put split-marks on a segment, and then put a split-mark on a second segment, the split-marks on the first segment are discarded. Anything you do that would update the segment, such as putting a code-mark on it or splitting it using text selection or doing a search, will cause the split-marks to be discarded.

To remove a split-mark, Ctrl/click it. Note that the clicking the Undo button reverses the last change to segments and as a side effect, removes the split-marks. For example, a user creates three split-marks in a segment, and then clicks the Undo button. One might think that the Undo button would result in two split-marks, removing only the last one applied. However, the Undo button would reverse the last change to the segment, and as a side effect, would remove all split-marks.&#x20;

Adding split-marks does not change the segment. To actually perform the split, click on the red scissors icon that appears when there are any split-marks. This action splits the segment on all the split-marks in it. This action changes the segment, is saved to the server, and can be undone.

## Combine Segments <a href="#minitocbookmark11" id="minitocbookmark11"></a>

When you hover over the beginning of a row, a move arrow (<img src="https://static.goascribe.com/Help/move_arrow.png" alt="" data-size="line">) displays. Click the move arrow and drag the row to the segment row that you want to combine.

## Marking Segments Using Codes in the Codebook <a href="#minitocbookmark12" id="minitocbookmark12"></a>

Several operations support marking segments by matching them against codes in the codebook. Depending on the operation, either the segments, the codes, or both may be restricted to a subset of all available codes or segments. &#x20;

A code is matched to a segment by considering the properties the code. For each segment, an attempt is made to match each code in the codebook to the segment using these rules, in the order of the codes in the codebook.  Once a match is found the remaining codes in the codebook are not tested.

* If the input ID of the code matches the segment by case insensitive comparison, it is a match
* Otherwise, if the input ID of the code is of the form NNN:MMM where NNN and MMM are integers, and if the segment is an integer, then if the segment is in the range defined by the input ID, it is a match
* Otherwise, if the regular expression of the code matches the segment, it is a match
* Otherwise, if the description of the code is the same as the segment, it is a match.

Matching by input ID, regular expression, and code description can be enabled or disabled individually in the [user's options.](phrase-analyzer-ii-settings.md)&#x20;

## Text Selection Operations <a href="#minitocbookmark13" id="minitocbookmark13"></a>

When you select text in a segment, a toolbox displays with these options:

<table><thead><tr><th width="271.99993896484375" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Split this segment at left edge of selection</td><td valign="top">Splits only this segment into two segments at the left edge of the selection. The new segments replace the current segment. The segment from the right side of the split is placed below the segment from the left side of the split.</td></tr><tr><td valign="top">Split this segment at selection</td><td valign="top">Splits only this segment into two or three segments. There will be two segments if the start of the selection is at the left-most edge of the segment; otherwise, there will be three segments. The new segments replace the current segment and are placed in left, middle and right order.</td></tr><tr><td valign="top">Split all segments at selection</td><td valign="top">All segments are scanned for the selected text. If a segment already has a mark (or selected code), that segment is ignored and not changed. Otherwise, split at each occurrence of the selected text.</td></tr><tr><td valign="top">Delete selection from this segment</td><td valign="top">Removes the selected text from only this segment.</td></tr><tr><td valign="top">Delete selection from all segments</td><td valign="top">All segments are scanned for the selected text. Remove the selected text from all segments, except those that already have a mark. If a segment already has a mark, that segment is ignored and not changed.</td></tr><tr><td valign="top">Mark all segments with first code matching selection</td><td valign="top">Using the selection text, mark all matching segments with the first matching code in the codebook. If the matched text in the segment already has a mark, it is not marked with the matching code.</td></tr><tr><td valign="top">Create a code from selected text</td><td valign="top">Create a new code in the codebook using the selected text. The selected text becomes the code description and the regular expression. The new code is added to the top of the codebook, unless a code is selected. If a code is selected, the new code is inserted below that code.</td></tr></tbody></table>

## Punctuation Marks and Splitting Segments <a href="#minitocbookmark14" id="minitocbookmark14"></a>

Punctuation marks are a sequence of characters in the Unicode punctuation character class and white space characters. When splitting a segment, we look for contiguous punctuation marks at the start and end of splits, but only when the split edge is not at the start or end of the original segment. If we find such marks, we remove them from the split segment, but only if removing them does not cause the split segment to be zero length.

In other words, if you select a sequence of characters that are only punctuation marks and split on that sequence, you will get the punctuation marks in the split segment. But, if you split on a selection that has at least one non-punctuation character, then the split segment will not have the leading and trailing punctuation.&#x20;

## Applying Codes <a href="#minitocbookmark15" id="minitocbookmark15"></a>

The provisional code marks can be applied to segments using the Apply Codes operation.

There are three possibilities for the segments of a given verbatim:

* **None of the segments have marks**\
  This verbatim is never coded when applying codes
* **All of the segments have marks**\
  This verbatim is always coded when applying codes
* **At least one, but not all, of the segments have marks**\
  This verbatim is not coded unless the "Add Orphaned Segments to Notes" option is checked in the Settings dialog.  In this case the codes for the existing marks will be applied to the verbatim.  The text of the orphaned segments is added to the Notes of the verbatim.

Referring to the states of segments describe above, we see that when "Add Orphaned Segments to Notes" **is not checked** the **remaining segments will all be white, red, or orange**:

* **Unmarked** (white)\
  **Orphaned** (red)\
  **Partially marked** (orange)\
  No codes will be applied to verbatims for these segments.  These segments will remain unchanged after the Apply Codes operation.
* **Some fully marked** (green/yellow)\
  Only the fully marked verbatims will be coded, the segments will change to orange, and the counts for these segments will decrease.
* **All fully marked** (green)\
  Verbatims for these segments will be coded, and these segments will disappear from display.

When "Add Orphaned Segments to Notes" is **checked** the **remaining segments will all be white**:

* **Unmarked** (white)\
  No codes will be applied to verbatims for these segments.  These segments will remain unchanged after the Apply Codes operation.
* **Orphaned** (red)\
  These segments will be added to the Notes of the associated verbatims that have any marked segments.  The segment will either disappear (if all verbatims had at least on marked segment), or will change to white with a decreased count.
* **Partially marked** (orange)\
  **Some fully marked** (green/yellow)\
  Codes will be applied to all of these segments and the segments will disappear from display.  Associated orphaned segments will be added to the Notes field of the verbatim.
* **All fully marked** (green)\
  Verbatims for these segments will always be coded, and these segments will disappear from display.

The addition of Notes to verbatims is the one operation that cannot be undone. Suppose the user applies codes with the "Add Orphaned Segments to Notes" option checked, and then undoes the operation. After the undo, the codes that were applied will be removed from the responses, but any text that was added to the Notes will remain.

Phrase Analyzer II attempts to always apply codes by order of mention. It does this by matching the text of the segments for a verbatim to the verbatim text. The result of this matching is shown in the Responses dialog, opened by clicking the response count in a segment. Matched portions of the verbatims are displayed with a blue font and underscore, and the code to be applied is displayed in the tooltip for the box. While the matching of segments to verbatims is normally successful, under some circumstances, the matching will not succeed.

When codes are applied to the verbatims, the segment information is stored with the applied code. The segment information is the starting and ending offset of the segment, as determined by the matching described above.  If the matching is unsuccessful the code is still applied, but with no record of the starting and ending offsets.

## View the Responses in Ascribe Coder <a href="#minitocbookmark16" id="minitocbookmark16"></a>

You can view the responses and applied codes in Ascribe Coder and make changes as necessary. You can view which segments received codes by selecting the [Code Segments on Hover](../ascribe-coder/responses-settings.md#minitocbookmark4) option in the Applied Codes tab of Responses Settings.&#x20;
