---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/ascribe-coder/codebook-merge-map
---

# Codebook Merge/Map

The Codebook Merge/Map tool allows you to merge the coding of one codebook to another and share the codebook between questions. In this process, one codebook is considered the target and one is considered the source codebook. The target codebook is the one to survive the merge process and will be the one shared among the questions selected for the merge operation.

For example, two different, but perhaps similar, codebooks were used to code two different questions. After coding was complete, a client asked for the two questions to have the same codebook. We can do use the Codebook Merge/Map tool to accomplish this action.

Here is a step-by-step guide: [Codebook Merge-Map Process](../../guides-and-tutorials/codebook-merge-map-step-by-step-process.md)

## Terminology <a href="#minitocbookmark2" id="minitocbookmark2"></a>

**Target Codebook -** the codebook that is the final result of the merge. It displays on the left side of the screen.

**Source Codebook -** the codebook that contains codes to be merged; it will be shared with the target codebook at the end of the process. It displays on the right side of the screen.

**Used code -** a code was applied to a response. A red dot (<img src="https://static.goascribe.com/Help/red_dot.gif" alt="" data-size="line">) next to a code indicates that the code was used.

**Unused code -** a red circle (<img src="https://static.goascribe.com/Help/red_circle.gif" alt="" data-size="line">) indicates a code has not been used.

## Rules <a href="#minitocbookmark3" id="minitocbookmark3"></a>

All **used** codes in the source codebook must be matched to a code in the target codebook. You can either match the source code to a code in the target codebook or you can add the code to the target codebook.

If the source codebook contains unused codes, you do not have to add them to the target. (If you need them in the target codebook, then yes, add them.)

## Navigation <a href="#minitocbookmark4" id="minitocbookmark4"></a>

Navigate to the Codebook Merge/Map tool by any of these options

* the Supervisor menu option of Codebook Merge/Map
* the Questions menu option of Copy/Share>Dual Codebooks
* the Ascribe Coder menu option of Dual Codebooks.

If you navigate to Dual Codebooks, click the Navigation icon and select Codebook Merge/Map.

## Toolbar and Icons <a href="#minitocbookmark5" id="minitocbookmark5"></a>

Codebook Merge/Map has the following icons:

<table><thead><tr><th width="267.3333740234375" align="center" valign="top">Icon</th><th valign="top">Description</th></tr></thead><tbody><tr><td align="center" valign="top"><img src="https://static.goascribe.com/Help/Left_codebook_icon_full_size.gif" alt=""> <br>Left Codebook</td><td valign="top">Use this icon to display the search facility for the Target Codebook pane.</td></tr><tr><td align="center" valign="top"><img src="https://static.goascribe.com/Help/right_codebook_icon_full_size.gif" alt=""> <br>Right Codebook</td><td valign="top">Use this icon to display the search facility for the Source Codebook pane.</td></tr><tr><td align="center" valign="top"><img src="https://static.goascribe.com/Help/match_codes_icon_full_size.gif" alt=""> <br>Match Codes</td><td valign="top">Click this icon to use <a href="codebook-merge-map.md#minitocbookmark7">automatic codebook matching criteria</a>. This icon is grayed out until both a target codebook and a source codebook are loaded.</td></tr><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/save_to_target_codebook_full_size.gif" alt=""> <br>Save To</p><p>  Target Codebook</p></td><td valign="top">This icon is grayed out until all of the used codes from the source codebook have been matched to the target codebook. When icon is active, <a href="codebook-merge-map.md#minitocbookmark9">click it to execute the merge.</a></td></tr><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/search_within_codebook.gif" alt=""> <br>Search</p><p> (Within Codebook)</p></td><td valign="top">This icon is grayed out until a codebook is loaded to the pane. When active, click this icon to search for a code within the codebook.</td></tr><tr><td align="center" valign="top"><img src="https://static.goascribe.com/Help/settings_icon_full_size.gif" alt=""> <br>Settings</td><td valign="top">This icon is grayed out until a codebook is loaded to the pane. When active, click this icon to display the Settings dialog, where you can change which fields display and how they are formatted. The Settings dialog is the same as the one found in Ascribe Coder and has a tab for When Unlocked; however, you cannot unlock the codebook when in Codebook Merge/Map.</td></tr><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/hide_matched_codes.gif" alt=""></p><p>Hide Matched Codes</p></td><td valign="top">This icon is grayed out until a source code is matched to a target code. Once a code is matched, click this icon to hide any matched codes. It may be useful to hide matched codes when codebooks are large; it makes the unmatched codes more visible.</td></tr></tbody></table>

## Find and Load the Source and Target Codebooks <a href="#minitocbookmark6" id="minitocbookmark6"></a>

When you navigate to Codebook Merge/Map from Ascribe Coder>Dual Codebooks or Questions>Copy/Share>Dual Codebooks, the Source Codebook pane is populated with a codebook so you are ready to find the target codebook.

When you navigate to Codebook Merge/Map from the Supervisor menu, you have to select both a source codebook and a target codebook.

To find a question or codebook, you can manually scroll through the list of Account Codebooks and Studies. Only questions with existing codebooks are in the list; if a codebook is empty, you can share the codebook instead of using Codebook Merge/Map.

It may be faster and more convenient to enter search criteria in the search text box and click the Search button. A filtered list displays as shown below:

![](https://static.goascribe.com/Help/filtered_list_displays.gif)

&#x20;

Each study has a list of questions and codebooks associated with it. To display the questions or codebooks associated with the study, click the drop-down arrow next to Questions or Codebooks:

![](https://static.goascribe.com/Help/click_the_drop_down_arrow.gif)

&#x20;

The icons next to the questions or codebooks indicate whether the question or codebook is shared:

<table><thead><tr><th width="171.3333740234375" align="center" valign="top">Icon</th><th valign="top">Description</th></tr></thead><tbody><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/shared_codebook_icon.gif" alt=""></p></td><td valign="top">Indicates question/codebook is shared</td></tr><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/not_shared_codebook_icon.gif" alt=""></p></td><td valign="top">Indicates question/codebook is not shared </td></tr></tbody></table>

Click the question or codebook that you want to load.

Once you have the source loaded, you can hover over the words Source Codebook in the title bar, and the study name and question ID display; you can do the same for the target codebook.

If you decide to use a different source codebook, click the Right Codebook icon (<img src="https://static.goascribe.com/Help/right_codebook_icon.gif" alt="" data-size="line">) to load the search facility again.

If you decide to use a different target codebook, click the Left Codebook icon (<img src="https://static.goascribe.com/Help/left_codebook_icon.gif" alt="" data-size="line">) to load the search facility again.

## Match the Codes Automatically <a href="#minitocbookmark7" id="minitocbookmark7"></a>

Once you have both the source and target codebooks selected, the next step is to match the codes. The number of unmatched codes (from the source codebook) is indicated at the top of the page.

You can manually match the codes or use the automatic features with the Match Codes option. You cannot match nets. If you need to add a net heading to the target codebook, you can edit the codebook in Ascribe Coder or in Dual Codebooks either before or after using Codebook Merge/Map.

Click the Match Codes icon (<img src="https://static.goascribe.com/Help/match_codes_icon.gif" alt="" data-size="line">) to use these options:

<table><thead><tr><th width="279.3333740234375" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Code Description</td><td valign="top">Search the code descriptions of the source and target codebooks to find matches.</td></tr><tr><td valign="top">Input ID</td><td valign="top">Search the input IDs of the source and target codebooks to find matches.  </td></tr><tr><td valign="top">Output ID</td><td valign="top">Search the output IDs of the source and target codebooks to find matches.  </td></tr><tr><td valign="top">Numeric InputID</td><td valign="top">Search only numeric  input IDs of the source and target codebooks to find matches.  </td></tr><tr><td valign="top">Numeric OutputID</td><td valign="top">Search only numeric  output IDs of the source and target codebooks to find matches.  </td></tr><tr><td valign="top">Regular Expression</td><td valign="top">Search regular expressions of the source and target codebooks to find matches.  </td></tr><tr><td valign="top">Code ID</td><td valign="top">Search code IDs  of the source and target codebooks to find matches.  </td></tr></tbody></table>

These options can be used together or individually. If used together, each of the criteria items must be equal between the source and target codes for the items to be considered matched. Equality is determined by a case insensitive comparison of the items.

Matched codes have a green dot (<img src="https://static.goascribe.com/Help/green_dot.gif" alt="" data-size="line">) for used codes and a green circle (<img src="https://static.goascribe.com/Help/green_circle.gif" alt="" data-size="line">) for unused codes. The matched codes also have a strike-through line.

In the bottom pane, the left column lists the target codes, and the right column lists the mapped codes from the source codebook. The red X next to a target code is used to remove a match.

If not all of the used codes are matched, you have to [manually match the codes](codebook-merge-map.md#minitocbookmark8).

Once all of the used codes in the source codebook have been matched, the Save to Target Codebook icon (<img src="https://static.goascribe.com/Help/merge_icon.gif" alt="" data-size="line">) becomes available to use. (If there are unused codes in the source codebook,  it is optional to add them to the target codebook.)

## Match the Codes Manually <a href="#minitocbookmark8" id="minitocbookmark8"></a>

To manually match the codes, click a code in the target codebook. This action highlights the code. Then click the matching code in the source codebook. The codes are then mapped in the bottom pane with the target codes on the left and the source (mapped) codes on the right.

The red X next to a target code is used to remove a match. If you map more than one source code to a target code, a red X displays next to each source (mapped) code. Click the red X to remove a code from the match.

## Save to Target Codebook <a href="#minitocbookmark9" id="minitocbookmark9"></a>

When you are ready to merge the codebooks, click the Save to Target codebook icon (<img src="https://static.goascribe.com/Help/merge_icon.gif" alt="" data-size="line">) and the Questions to Merge dialog displays.

The dialog lists the source question(s) that could be merged into the target codebook. If the source question is shared with other questions, all of the questions are listed in the dialog.

Select the questions you want to merge and click OK. Any questions not selected will not be merged and shared with the target codebook.

After you select the questions to merge, the confirmation dialog displays. Enter OK to continue. The merge completes, and the target and source questions are shared. The Source Codebook pane returns to search mode, in case you want to find another question to merge. If not, use, the Navigation icon to move to another part of Ascribe.
