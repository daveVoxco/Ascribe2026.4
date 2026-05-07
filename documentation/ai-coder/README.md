---
description: >-
  AI Coder is the next generation of a codebook builder/theme extractor. It
  parses responses into segments and groups similar segments into codes.
metaLinks:
  alternates:
    - https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/ai-coder
---

# AI Coder

When you export the codebook to Ascribe Coder, the codes are automatically applied to the responses. AI Coder is available for anyone with coder or supervisor privileges.

<figure><img src="../../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

<details>

<summary>Columns</summary>

{% hint style="info" %}
### Note

Click the [table-manager.md](../study/table-manager.md "mention") menu (![](<../../.gitbook/assets/image (171).png>)) on the side to customize the current view, you can choose which columns are displayed, configure rows appearance, allow multi column sort, export and save the view for later use.&#x20;
{% endhint %}

<table><thead><tr><th width="135.35552978515625" valign="top">Column</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Key</td><td valign="top">Unique project identifier</td></tr><tr><td valign="top">Study ID</td><td valign="top">Study name</td></tr><tr><td valign="top">Question ID(s)</td><td valign="top">Question(s) ID/name analyzed</td></tr><tr><td valign="top">Type</td><td valign="top"><ul><li>GAI: Generative AI Segmentation</li><li>AI: Non Generative AI Segmentation. Instead uses Split words and Characters</li></ul></td></tr><tr><td valign="top">AI Version</td><td valign="top"><p>Displays the AI version used, the AI version used depends on which version of AI Coder <em>Codebook generation method</em> is selected at creation:</p><p><strong>1</strong>: Projects created on versions prior to release 2025.4 continue to work using Version 1 AI analysis, new projects that use either.</p><ul><li>Created using Theme Extractor (Legacy)</li><li>Ascribe Clustering (Legacy) AI analysis</li></ul><p></p><p><strong>2</strong>: All projects created Codebook Builder as their Codebook generation method.</p></td></tr><tr><td valign="top">Date</td><td valign="top">Date the analysis last had changes or an update</td></tr><tr><td valign="top">Responses</td><td valign="top">Total number of responses analyzed within this analysis</td></tr><tr><td valign="top">% Coded</td><td valign="top">Total percent of responses coded within this analysis</td></tr><tr><td valign="top">Creator</td><td valign="top">Project's creator account name</td></tr></tbody></table>

</details>

**Search**: find information in any column of the the AI coder grid .

**View Codebooks button**: Lists previously saved codebooks created with AI Coder. Click the View Codes button to see the codes; click the blue number next to the code to see the associated segments.

You have the choice between [Generative AI](./#minitocbookmark2) and [#how-non-generative-ai-coder-works](./#how-non-generative-ai-coder-works "mention") .

AI Coder **splits a response into one or more segments**, then **groups those segments into codes.**

* AI Coder _summarizes the main idea(s)_ from a response into one or more segments (higher-level, paraphrased ideas) to generate the codes.
* Non-Generative AI Coder creates segments by _splitting the response text_ using split characters / split words (more literal chunks of the original text) before grouping them into codes.

See [Get Started with AI Coder 2025](get-started-with-ai-coder.md) and [AI Coder Trained Codebook Process 2023](../../guides-and-tutorials/ai-coder-trained-codebook-process-for-trackers.md) for more information.

## Concepts

### Generative AI <a href="#minitocbookmark2" id="minitocbookmark2"></a>

**Generative AI allows**:

* Ability to provide context for your analysis
* No need for split words or split characters; the processor generates segments from the response
* Assists with code naming, clear and concise code descriptions
* Allows for multi-level sub-netting
* Assists with net and sub-net naming
* Processes data in any language and generates the segments in English
* Allows the user to determine the codebook language with choice of seven languages (English, Spanish, French, German, Italian, Chinese and Dutch).

### Non-Generative AI

{% stepper %}
{% step %}
**Segment Responses**

Responses are split into segments using split characters and split words defined in the Options dialog.

{% hint style="success" %}
#### Example

"I like cats. I hate dogs" generates 2 segments due to the period (split character).
{% endhint %}
{% endstep %}

{% step %}
**Convert to Vectors**

Using AI, segments are converted to numerical vectors based on models built from word relationships across millions of Wikipedia pages. These vectors can be compared using cosine proximity, which measures semantic similarity.

| Comparison                            | Cosine Proximity         |
| ------------------------------------- | ------------------------ |
| "I like cats" vs. "I love cats"       | \~0.98 (high similarity) |
| "I like cats" vs. "My tailor is rich" | \~0 (no similarity)      |
{% endstep %}

{% step %}
**Cluster Vectors**

A clustering algorithm groups vectors that are:

* Similar within groups
* Dissimilar across groups

A constraint can require minimum cosine similarity (e.g., 0.7) for grouping.
{% endstep %}

{% step %}
**Assign Ungrouped Segments**

For segments not assigned to any cluster:

* Locate the cluster with highest average cosine proximity to that segment
* If average exceeds minimum threshold (e.g., 0.5), assign segment to that cluster
{% endstep %}

{% step %}
**Name Groups**

AI Coder assigns names by parsing the 10 most coherent segments in each group and selecting the shortest one with more than one word. Names can be edited in the Codebook pane.
{% endstep %}

{% step %}
**Reconnect to Source**

Clustered vectors are mapped back to source segments, then to source responses.
{% endstep %}
{% endstepper %}

### AI Coder and Shared Questions <a href="#minitocbookmark4" id="minitocbookmark4"></a>

You can use AI Coder on shared questions. Any [source](../ascribe-coder/sources.md) will be analyzed (excluding samples.)&#x20;

* If you only analyze one of the shared questions and export the results to Ascribe Coder, the share is severed.&#x20;
* If you analyze all of the shared questions and export the results to Ascribe Coder, the share is maintained.

## Analyze Questions <a href="#minitocbookmark5" id="minitocbookmark5"></a>

Unlock the codebook and click the AI Coder icon ( ![](<../../.gitbook/assets/image (41).png>) ) in Ascribe Coder.

<figure><img src="../../.gitbook/assets/image (40).png" alt="" width="563"><figcaption></figcaption></figure>

The [Analyze](ai-coder-analyze.md) dialog displays. Click the run Analysis button to analyze the responses. (If you have already used AI Coder for the question(s), the results automatically display).

## AI Coder Toolbars <a href="#minitocbookmark6" id="minitocbookmark6"></a>

<details>

<summary>Primary (Blue) toolbar options</summary>



<figure><img src="../../.gitbook/assets/image (337).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="254" align="center" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/ai_coder_navigation_dec_2022.jpg" alt="" data-size="original"></p><p>Navigation</p></td><td valign="top">Click the navigation icon to navigate to other pages.</td></tr><tr><td align="center" valign="top">Brands/Short Answer</td><td valign="top">If a bracket displays in front of the question, the data was considered to be brands or short answer. Only displays if the responses are two words or less.</td></tr><tr><td align="center" valign="top"><img src="https://static.goascribe.com/Help/AI_Coder_question_dropdown.jpg" alt="" data-size="original"></td><td valign="top">If multiple questions were analyzed, this drop-down lists each question, which allows you to view the result by question.</td></tr><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/ai_coder_home.jpg" alt="" data-size="original"></p><p>Home</p></td><td valign="top">Navigates to the AI Coder Projects page which lists the projects and allows you to open other projects. You can also clear/reset analysis from this page.</td></tr><tr><td align="center" valign="top"><div><figure><img src="../../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure></div></td><td valign="top">Indicates that you are on the Edit page..</td></tr><tr><td align="center" valign="top"><div><figure><img src="../../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure></div></td><td valign="top">Must have a license for this option to display. Allows you to visualize the data. <br>See: <a data-mention href="ai-coder-visualize.md">ai-coder-visualize.md</a></td></tr><tr><td align="center" valign="top"><div><figure><img src="../../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure></div></td><td valign="top">Opens the <a data-mention href="ask-ascribe.md">ask-ascribe.md</a> dialog, where you can get summaries of the data.</td></tr><tr><td align="center" valign="top"><img src="https://static.goascribe.com/Help/AI_Coder_Analyze.jpg" alt="" data-size="original"></td><td valign="top">See <a data-mention href="ai-coder-analyze.md">ai-coder-analyze.md</a> for more information.</td></tr><tr><td align="center" valign="top"><img src="https://static.goascribe.com/Help/AI_coder_sentiment_01.jpg" alt="" data-size="original"></td><td valign="top">Creates positive, neutral and negative nets, as well as a net for codes without sentiment.</td></tr><tr><td align="center" valign="top"><img src="../../.gitbook/assets/image (152).png" alt="View Codebook" data-size="original"></td><td valign="top">Lists previously saved codebooks created with AI Coder. Click the View Codes button to see the codes; click the blue number next to the code to see the associated segments.</td></tr><tr><td align="center" valign="top"><img src="../../.gitbook/assets/image (153).png" alt="Save Codebook" data-size="original"></td><td valign="top">Saves the current codebook and its associated segments to allow for future use. Also creates rules for each code. To see the rules, use the Saved Codebooks option.</td></tr><tr><td align="center" valign="top"><img src="../../.gitbook/assets/image (148).png" alt="Export to HTML" data-size="original"></td><td valign="top">Exports an HTML image of codebook. Use CTRL/HTML button to get an image of the codebook with the responses underneath the codes; the segment which received the code displays in blue.</td></tr><tr><td align="center" valign="top"><img src="../../.gitbook/assets/image (147).png" alt="Export to Excel" data-size="original"></td><td valign="top">Must have the Charts license for this option to appear. Exports the analyzed data to Excel.</td></tr><tr><td align="center" valign="top"><img src="../../.gitbook/assets/image (146).png" alt="Export Data to Coder" data-size="original"></td><td valign="top"><p>Allows you to export the codebook to Ascribe Coder, with the option to code the responses or not.</p><p> </p><ul><li><strong>If no codebook exists in Ascribe Coder</strong>, a new codebook is created. You have the option to export the codebook only (and not code the responses.)</li></ul><p> </p><ul><li><strong>If a codebook exists in Ascribe Coder</strong>, you can choose to update the codebook, append the AI Coder codebook to the existing codebook or overwrite the existing codebook. Update and append put the codes at the top of the codebook.</li></ul><p> </p><ul><li><strong>If no codebook exists in Ascribe Coder and the questions are shared but not all questions were analyzed</strong>, a new codebook is created and the share is maintained.</li></ul><p> </p><ul><li><strong>If a codebook exists in Ascribe Coder and the questions are shared but not all questions were analyzed</strong>, you have the choice to sever the share or maintain the share.  </li></ul></td></tr><tr><td align="center" valign="top"><img src="../../.gitbook/assets/image (170).png" alt="" data-size="original"></td><td valign="top">Navigates back to Ascribe Coder without exporting the codebook, and does not code the responses. If you do that, you can return to AI Coder and export the codebook and code the responses later.</td></tr></tbody></table>

</details>

<details>

<summary>Secondary (gray) tollbar options</summary>



<figure><img src="../../.gitbook/assets/image (336).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="184" align="center" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td align="center" valign="top">Search</td><td valign="top"><p>There is a search text box above both the Segments pane and the Codebook pane.</p><p>When you use the search above the Segments pane, both the segment and the associated code display.</p><p>When you use the search above the Codebook pane, it only searches that pane.</p></td></tr><tr><td align="center" valign="top">Keywords</td><td valign="top">The drop-down list contains the most frequently mentioned words associated with the search criteria. Click a keyword to add it to the search criteria.</td></tr><tr><td align="center" valign="top"><p>Sort</p><p><img src="https://static.goascribe.com/Help/change_sort_direction.jpg" alt="" data-size="original"></p></td><td valign="top"><p>Sort the Segment pane by confidence score, text, length, frequency or sentiment. When you sort by sentiment, the sentiment displays next to the segment. You can click the sentiment and get an option to change the sentiment.</p><p></p><p><strong>Sort by Segment Type</strong>: This option sorts the uncoded segments to the top (to impact the % coded).</p><p> </p><p>The Segment pane also has the Sort Direction button to change the sort order.</p><p> </p><p>Sort the Codebook pane by frequency, text, length or codebook (codebook is useful when a saved codebook was used during the analysis).</p><p> </p></td></tr><tr><td align="center" valign="top">Coded Segments</td><td valign="top">Displays segments that were to assigned to each code with the highest confidence. These segments were assigned during the main clustering algorithm and display in bold. Segments that were assigned during the consolidation phase of the clustering algorithm, but also have a high confidence, display in normal font.</td></tr><tr><td align="center" valign="top"><img src="https://static.goascribe.com/Help/scroll_bar_for_segments.jpg" alt="" data-size="original"></td><td valign="top">When a code has more than 1000 segments, a scroll bar displays. Use it to scroll through all the segments.</td></tr><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/Refresh.jpg" alt="" data-size="original"></p><p>Refresh</p></td><td valign="top">Refreshes the screen.</td></tr><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/undo_01.jpg" alt=""> <img src="https://static.goascribe.com/Help/redo_01.jpg" alt=""></p><p>Undo/Redo</p></td><td valign="top">Actions can be undone and redone (renaming a code, adding nets, merging codes, etc.)</td></tr><tr><td align="center" valign="top"><img src="https://static.goascribe.com/Help/net_codes.jpg" alt="" data-size="original"></td><td valign="top">Automatically groups the codes into nets. Choose 1 for top level codes or 2 for sub-nets. Entering a zero removes the nets.</td></tr><tr><td align="center" valign="top"><img src="https://static.goascribe.com/Help/new_net.jpg" alt="" data-size="original"></td><td valign="top">Lets you add a net manually. If you have selected multiple codes by using the checkbox at the end of the codes' rows, these codes will automatically placed in the new net.</td></tr><tr><td align="center" valign="top"><img src="https://static.goascribe.com/Help/new_code.jpg" alt="" data-size="original"></td><td valign="top">To manually add a code, select a segment or segments and click the New Code button. The segments are then associated with the code.</td></tr><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/fewer_codes_01.jpg" alt="" data-size="original"></p><p><img src="https://static.goascribe.com/Help/more_codes_01.jpg" alt="" data-size="original"></p></td><td valign="top"><p>Use these buttons to create fewer codes or more codes.</p><p> </p><p>When using the Fewer Codes option, you are actually raising the minimum segment frequency needed to create a code. For example, the default maybe be 3 segments needed before a code can be created. When using the Fewer Codes button, that frequency requirement becomes a 5. The system would need to group 5 segments together before it creates a new code. You may see a (slight) drop in coded percentage as more segments are being left ungrouped.</p><p> </p><p>In general, using the More Codes option, you would have more segments coded; however, you could end up creating a code for each unique segment with a lot of overlap across the codes created.</p></td></tr></tbody></table>

</details>

## Panes

<figure><img src="../../.gitbook/assets/image (338).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="103.06671142578125">Region</th><th valign="top">Description</th></tr></thead><tbody><tr><td>A</td><td valign="top">The Segments or Responses pane on the left</td></tr><tr><td>B</td><td valign="top">The Codebook pane on the right</td></tr></tbody></table>

### Codebook pane <a href="#minitocbookmark7" id="minitocbookmark7"></a>

The Codebook pane on the right contains the codes generated by AI Coder.

<figure><img src="../../.gitbook/assets/image (348).png" alt=""><figcaption></figcaption></figure>

The number of codes generated is list at the top of the pane, followed by the percentage of responses that would be coded. The numbers after the percentage (N/N) represent the number of responses that would be coded out of the total number of responses. The number of responses coded do not include responses that would receive the Others code.

* **The blue number next to the code** is the number of segments that make up the code. To view these segments, click the code.&#x20;
* When you click on a code it highlights the segments associated with it in the responses list.

At the end of the codelist is a code called Uncoded Segments. It contains all segments not assigned to any code. Here are the options associated with Others:

<table><thead><tr><th width="292.6666259765625" align="center" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/Include_uncoded_segments_from_uncoded_responses.jpg" alt="" data-size="original"></p><p>Include Uncoded Segments From Uncoded Responses</p></td><td valign="top">Select this checkbox if you want to display segments which are not coded from responses that have not received any codes. These segments display in black in the Segment pane.</td></tr><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/Cluster_segments_of_the_code.jpg" alt="" data-size="original"></p><p>Cluster Segments of That Code</p></td><td valign="top">This option allows the system to try and add codes automatically in a net called Codes Created from Others.</td></tr><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/Help_Code_Others.jpg" alt="" data-size="original"></p><p>Help Code Others</p></td><td valign="top"><p>This option displays a dialog with coding suggestions. A code is listed in bold with uncoded segments underneath. Select the segments which should be coded with that code and click OK.</p><p> </p><p>This symbol is also available for every segment in the Segment pane and allows you to code the segment with a suggested code.</p></td></tr></tbody></table>

#### Codebook pane actions <a href="#minitocbookmark8" id="minitocbookmark8"></a>

<details>

<summary>Edit Codes</summary>

You can change/edit the codes with the following options:

<figure><img src="../../.gitbook/assets/image (349).png" alt="" width="563"><figcaption></figcaption></figure>

<table><thead><tr><th width="219.99993896484375" align="center" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/pencil_icon.jpg" alt="" data-size="original"></p><p>Rename Code</p></td><td valign="top">Click the pencil icon to rename the code. A Rename Code dialog displays where you can edit the code.</td></tr><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/Cluster_segments_of_the_code.jpg" alt="" data-size="original"></p><p>Cluster Segments of That Code</p></td><td valign="top"><p>Sometimes a code may cover more than one idea; in that case, a split symbol displays at the end of the code's row. Click the symbol to split the code into multiple new codes and select the maximum number in the popup dialog. If a zero is entered, the system will use AI logic to determine the appropriate number of codes.<br></p><p>The new codes display in blue. To accept the new codes and turn them black, click the check mark in that code's row.</p><p> </p><p>If you do not like the additional codes, you can click Undo to return the segments to the original code. Or you can manually drag and drop the new codes on the original code.</p><p> </p><p>If you delete the new codes, those segments are put into uncoded segments.  </p></td></tr><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/delete_code.jpg" alt="" data-size="original"></p><p>Delete Code</p></td><td valign="top">To delete a code, click the X at the end of the row. The segments associated with the code are moved to the Others code.</td></tr><tr><td align="center" valign="top">Merge Codes</td><td valign="top"><p>To merge codes, select a code and drag it onto another code. The target code receives all the segments from the merged code. The drag-and-drop method only works on one code at a time.</p><p> </p><p>To merge multiple codes, it can be easier to search for similar segments and then move all the segments to a target code. (Use Ctrl/Click or Shift/Click to select multiple segments.)</p></td></tr></tbody></table>

</details>

<details>

<summary>Create Nets</summary>

To automatically create nets, click the **Net Codes** button. You can move the codes by dragging them and dropping them onto another net.

<figure><img src="../../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

To manually create a net, select a code and click the **New Net** button. To create a net from multiple codes, click the checkbox at the end of each code's row and then click the Add Net button.&#x20;

<figure><img src="../../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

To add codes to an existing net, click the checkbox at the end of each code's row and click on the net.

* Edit a net name by clicking  clicking the pencil icon. A Rename Net dialog displays.
* Delete a net by clicking the X at the end of the net's row.
* You can create a sub-net by dropping one net on another.

Any net or sub-net that has at least five codes has a sub-net button on the right. Click it to create sub-nets within that net.

</details>

### Segments / Responses Pane <a href="#minitocbookmark10" id="minitocbookmark10"></a>

The Segments/Responses tabs on the left populate when you click on a code in the Codebook pane or when you search for a segment/response.

<figure><img src="../../.gitbook/assets/image (350).png" alt=""><figcaption></figcaption></figure>

**Tabs:**

<figure><img src="../../.gitbook/assets/image (347).png" alt="" width="563"><figcaption></figcaption></figure>

{% tabs %}
{% tab title="Segments" %}
Click the Segments tab to access the Segments view.

<figure><img src="../../.gitbook/assets/image (340).png" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
#### What is a Segment

A segment can stand alone as a complete response or can be a component of a larger response.
{% endhint %}

**The red number** next to each segment indicates the number of times this segment was found. Click the number to see the source response(s) where the segment was found.&#x20;

<figure><img src="../../.gitbook/assets/image (36).png" alt=""><figcaption><p>Responses dialog</p></figcaption></figure>

* The respondent ID of the response displays below the segment.
* Click the Export to Excel button (<img src="../../.gitbook/assets/image (37).png" alt="" data-size="line">) to export the questions to a .csv file&#x20;

#### Colors on the Source Responses Pane <a href="#minitocbookmark11" id="minitocbookmark11"></a>

To see the source response of a segment, click the red number next to the segment in the Segments pane. The response displays with these colors:

<table><thead><tr><th width="209.333251953125" valign="top">Color</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Dark Blue</td><td valign="top">The color indicates that this segment is the one you selected. Hover over it to display the idea and applied code (if segment is coded) displays.</td></tr><tr><td valign="top">Light Blue</td><td valign="top">The color indicates that this segment is coded. Hover over it to display the idea and applied code.</td></tr><tr><td valign="top">Dark Black</td><td valign="top">The color indicates that an idea was found in the segment but it is not coded. Hover over it to display the idea.</td></tr><tr><td valign="top">Light Black</td><td valign="top">The color indicates no idea was found in the segment.</td></tr></tbody></table>

#### Uncoded Segments colors <a href="#minitocbookmark12" id="minitocbookmark12"></a>

To view uncoded segments, click the Uncoded Segments code in the Codebook pane. The segments display in the Segment pane with different colors.

<table><thead><tr><th width="212" valign="top">Color</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Dark Blue</td><td valign="top">The color indicates that this segment is the only piece of a response that is not coded.</td></tr><tr><td valign="top">Light Blue</td><td valign="top">The color indicates that this segment is one of several segments in a response that are not coded.</td></tr></tbody></table>

You can also view uncoded segments from uncoded responses by clicking the checkbox next to the Uncoded Segments code. When you do that, segments may display in these colors:

<table><thead><tr><th width="214" valign="top">Color</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Bold Black</td><td valign="top">The color indicates that there are multiple segments in the response and no part of the response is coded.</td></tr><tr><td valign="top">Light Black</td><td valign="top">The color indicates that there is only one segment in the response and it is uncoded.</td></tr></tbody></table>

#### Manipulating Segments <a href="#minitocbookmark13" id="minitocbookmark13"></a>

To remove a segment from a code, click the X at the end of the segment's row or drag it to the Others code at the end of the codelist.

To set the segment as the code's title, click the forward arrow at the end of the segment's row.

When Uncoded Segments is selected, those segments display in italics which indicates they are not part of the code. Click the up arrow at the end of the segment row to add them to the code.&#x20;

Segments can be moved to other codes; select the segment and drag it to a different code.&#x20;

Use Ctrl/Click or Shift/Click to select multiple segments and then perform the desired function (add, delete, move).

#### Allow a Segment to be in Multiple Codes <a href="#minitocbookmark14" id="minitocbookmark14"></a>

Normally, a segment can only be in one code. However, you can copy a segment and assign it to more than one code.

To copy a segment, use CTRL/Drag to move the segment into an additional code.

#### Create New Codes from Segments <a href="#minitocbookmark15" id="minitocbookmark15"></a>

To create a new code from segments, select the segment(s) and then click the New Code button. Enter a title for the code, and click OK.

#### AI Coder Projects and Study Save and Restore <a href="#minitocbookmark16" id="minitocbookmark16"></a>

When a study is saved, the related AI Coder project is also saved. When you restore the study, the AI Coder project is also restored.
{% endtab %}

{% tab title="Responses" %}
Click the Responses tab to access the Responses view.

<figure><img src="../../.gitbook/assets/image (341).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
#### Tip

When you click on a code on the Codes list its corresponding segments will be highlighted in blue in every responses in the list.
{% endhint %}

#### Views

<figure><img src="../../.gitbook/assets/image (343).png" alt=""><figcaption><p>Click the <em>View all codes</em> toggle to change the view.</p></figcaption></figure>

**Responses** (Default): Displays an interactive list of responses.

* Hover the mouse over groups of words to see their coding information.&#x20;
* Click on a coded segment to view the Edit Code window.
* Highlighting text with the mouse in this mode does not do anything.

<figure><img src="../../.gitbook/assets/image (345).png" alt="" width="563"><figcaption><p><em>Responses</em> view - the highlighted .</p></figcaption></figure>

{% hint style="success" %}
#### Usage

* When you click a code on the Codes / Nets list on the right side the corresponding segments will be highlighted in the Responses list.
* Hover the mouse over a an highlighted segment to see which code it's associated with.
* Click the segment to open the Edit Code dialog, that allows you to&#x20;
{% endhint %}

**View all codes**: Display the interactive list of responses with their associated codes.

* Hover the mouse over groups of word to see their coding information.
* Click on a coded segment to view the Edit Code window.
* Highlight uncoded text with the mouse to assign a code to it.

<figure><img src="../../.gitbook/assets/image (346).png" alt="" width="563"><figcaption><p><em>View all codes</em> view.</p></figcaption></figure>

{% hint style="success" %}
#### Hint

You can click the Uncoded Segment link (the red box) to assign a code to it.
{% endhint %}

#### Edit Code

Click on a segment or code in the list of responses to bring up the Edit Code window you can use it to:

* Assign a new or different code to it.

<figure><img src="../../.gitbook/assets/image (342).png" alt="" width="381"><figcaption></figcaption></figure>



#### Response Details

The Response Details dialog shows the full response alongside relevant coding information.

<figure><img src="../../.gitbook/assets/image (352).png" alt="" width="563"><figcaption></figcaption></figure>

Click the "i" button beside the question to view the Response Details dialog.

<figure><img src="../../.gitbook/assets/image (351).png" alt="" width="563"><figcaption></figcaption></figure>

**Fields**:

<table><thead><tr><th width="181.79998779296875" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top"><strong>Response</strong></td><td valign="top">Complete response text.</td></tr><tr><td valign="top"><strong>Applied Codes</strong></td><td valign="top">List of codes applied to the response.</td></tr><tr><td valign="top"><strong>Closed Ends</strong></td><td valign="top">List associated questions with predefined answer choices.</td></tr><tr><td valign="top"><strong>Response ID</strong></td><td valign="top">Unique numeral identifier for the response.</td></tr><tr><td valign="top"><img src="../../.gitbook/assets/image (353).png" alt="" data-size="original"><br><strong>Download</strong></td><td valign="top">Download a spreadsheet (.csv) version of the data on the Response Details dialog.</td></tr></tbody></table>
{% endtab %}
{% endtabs %}
