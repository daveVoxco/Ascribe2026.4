---
description: AI Coder is Ascribe’s codebook builder and theme extractor.
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/ai-coder/get-started-with-ai-coder
---

# Get Started With AI Coder

It extracts ideas (segments) from responses and groups them into codes. You can either export the results into Ascribe Coder or use the Visualize and ASK modules available within AI Coder.

<figure><img src="../../.gitbook/assets/image (66).png" alt=""><figcaption></figcaption></figure>

## Generative or Non-Generative AI Segmentation?

Generative AI summarizes the main idea(s) from each response into segments to create a codebook, whereas non-Generative AI uses split characters and split words to manually segment the responses prior to grouping into codes.

As a rule, Generative AI is most useful when analyzing Open End responses, while Non-Generative AI is best used for brand/single response/keyword coding.

<table><thead><tr><th valign="top">Generative AI Segment</th><th valign="top">Response</th><th valign="top">Non-Generative AI Segment</th></tr></thead><tbody><tr><td valign="top"><ul><li>in-store pick-up option for online purchases</li><li>reduce shipping costs</li><li>missed sale due to high shipping costs</li></ul></td><td valign="top"><em>Allow on-line items to be delivered to store without paying shipping. The shipping is about 1/3 of the price of the item and caused me not to purchase the item from your store.</em></td><td valign="top"><ul><li>allow on-line items to be delivered to store without paying shipping</li><li>the shipping is about 1/3 of the price of the item</li><li>caused me not to purchase the item from your store</li></ul></td></tr><tr><td valign="top"><ul><li>poor customer service</li><li>lack of politeness</li></ul></td><td valign="top"><em>at the conclusion of my purchase the cashier put my change in my hand and said nothing i said thank you and got no response, no have a good night, thanks for shopping here nothing</em></td><td valign="top"><ul><li>at the conclusion of my purchase the cashier put my change in my hand</li><li>said nothing i said thank you</li><li>got no response, no have a good night, thanks for shopping here nothing</li></ul></td></tr><tr><td valign="top"><ul><li>healthier bakery items</li></ul></td><td valign="top"><em>better low fat and no sugar bakery items</em></td><td valign="top"><ul><li>better low fat</li><li>no sugar bakery items</li></ul></td></tr></tbody></table>

## Theme Extractor for Codebook Building/Coding or Clustering AI Codebook Building/Coding?

Theme Extractor is the default and simplest option when running your analysis. It leverages generative AI built on top of Ascribe’s algorithms and rule sets to provide results.  Theme Extractor will provide the largest coded percentage as well as a shorter codebook.

Turning Theme Extractor off allows the user to control all parts of the analysis on the individual level. This option is recommended for users who are already familiar with AI Coder functionality.

## Running AI Coder

{% stepper %}
{% step %}
Login and open **Ascribe Coder**.

<figure><img src="../../.gitbook/assets/image (154).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
Click **the Lock** icon the codebook in the toolbar.

<figure><img src="../../.gitbook/assets/image (67).png" alt="" width="357"><figcaption></figcaption></figure>
{% endstep %}

{% step %}
Click the **AI Coder** icon in the toolbar.

<figure><img src="../../.gitbook/assets/image (68).png" alt="" width="375"><figcaption></figcaption></figure>
{% endstep %}

{% step %}
Choose to keep the **Generative AI Segmenting** option or not in the Analyze window

**Basic Generative AI Segmenting configuration:**

<figure><img src="../../.gitbook/assets/image (69).png" alt="" width="563"><figcaption></figcaption></figure>
{% endstep %}

{% step %}
Click on the **Go** button to start the analysis process.

<figure><img src="../../.gitbook/assets/image (70).png" alt="" width="563"><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

## Working with AI Coder

Review the percentage coded and number of codes created once the analysis is done.&#x20;

* Do you need more codes? You might experiment with the Analysis settings and re-analyze to get more data coded.&#x20;
* Use the **Analyze** button to bring up the analysis options.&#x20;
* Edit the data context to control the idea extraction and codebook building. Alternatively use the Initial Codes Min. Proximity value to control the initial coding.&#x20;
* Raising the Initial Codes Min. Proximity value will code less data but will create more concise codes. Lowering the Initial Codes Min. Proximity value will code a larger portion of the data and create somewhat more general codes.

### AI coder main interface

<figure><img src="../../.gitbook/assets/image (64).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="52.59100341796875"> </th><th width="153.0001220703125" valign="top">Element</th><th>Description</th></tr></thead><tbody><tr><td>A</td><td valign="top">Analyze</td><td>Click this button to configure and run the analysis.</td></tr><tr><td>B</td><td valign="top">Codes and Nets</td><td>Indicate how many codes and nets are in the project</td></tr><tr><td>C</td><td valign="top">Coding progress</td><td>Indicates the percentage of responses coded and the relative absolute progress numbers.</td></tr></tbody></table>

### Analyse window on re-analysis

<figure><img src="../../.gitbook/assets/image (56).png" alt="" width="563"><figcaption></figcaption></figure>

<table><thead><tr><th width="57.7110595703125" align="center"> </th><th width="153.0001220703125" valign="top">Element</th><th valign="top">Description</th></tr></thead><tbody><tr><td align="center">A</td><td valign="top">Segmentation prompt</td><td valign="top">Create a prompt to specify contextual information about the data being analyzed (i.e.; Customer feedback on a hair product).</td></tr><tr><td align="center">B</td><td valign="top">Codebook Granularity</td><td valign="top">Lower or raise the minimal proximity to control the initial coding.</td></tr><tr><td align="center">C</td><td valign="top">Re-Analyze</td><td valign="top">Click this button to proceed with the re-analysis.</td></tr></tbody></table>

### Organize your codes

<figure><img src="../../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="57.7110595703125" align="center"> </th><th width="153.0001220703125" valign="top">Element</th><th valign="top">Description</th></tr></thead><tbody><tr><td align="center">A</td><td valign="top">Codes</td><td valign="top">Are the code names representative of their content (segments)?</td></tr><tr><td align="center">B</td><td valign="top">Segments</td><td valign="top">Does the code represent the segments?</td></tr><tr><td align="center">C</td><td valign="top">Keywords</td><td valign="top">Check the Keywords dropdown menu to see if anything stands out. </td></tr><tr><td align="center">D</td><td valign="top">Code suggestions</td><td valign="top">Click to move segments to a different code.<br>You can also </td></tr><tr><td align="center">E</td><td valign="top">Cluster segments of that code</td><td valign="top"><p>Click <strong>Get Clusters of This Code</strong> button (<img src="https://static.goascribe.com/Help/Get_Started_with_AI_Coder_2025_files/image011.png" alt="">) to break the code into </p><p>multiple more descriptive codes.</p></td></tr></tbody></table>

**Combine redundant or overlapping codes:**

Use the AI Codebook keywords tool to isolate similar codes and combine as needed.

<figure><img src="../../.gitbook/assets/image (157).png" alt=""><figcaption></figcaption></figure>

### Organize your segments

**Move segments to an existing code:**

Move segments as needed, either creating a new code, dragging into an existing code or using the Get Code Suggestions icon.

<figure><img src="../../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

**Move segments to a new code:**

{% stepper %}
{% step %}
**Select** the desired segment(s)

You can select multiple segments by using CTRL + click (non sequential) or Shift + click (select a sequence).

<figure><img src="../../.gitbook/assets/image (59).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
Click the **New Code** button

<figure><img src="../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Enter a new code name** and click OK to complete the operation
{% endstep %}
{% endstepper %}

### Net the codes

If using the Theme Extractor the codebook will be netted (grouped) automatically. Use the Netting tool to remove codes or re-group codes into similar Nets. Rename the nets as appropriate and combine redundant codes.

<figure><img src="../../.gitbook/assets/image (158).png" alt="" width="563"><figcaption></figcaption></figure>

<table><thead><tr><th width="57.7110595703125" align="center"> </th><th width="153.0001220703125" valign="top">Element</th><th valign="top">Description</th></tr></thead><tbody><tr><td align="center">A</td><td valign="top">Group</td><td valign="top">Auto-Group codes into Nets.</td></tr><tr><td align="center">B</td><td valign="top">New Nets</td><td valign="top">Manually create Nets.</td></tr></tbody></table>

### Uncoded Segments

By default, the Uncoded Segments code displays uncoded segments belonging to partially coded responses. Enable the checkbox toggle on the Uncoded Segments code to display uncoded segments which are part of completely uncoded responses.

**Use any of the following tools to review and upcode the Others**

* Use **Keywords** to manually identify segments that fit existing codes or add new codes.
* Use the **Help Code Others** icon to bring up the Coding Suggestions window for the Others.
* Click on the **Autocode Others** icon to automatically generate additional codes from the segments in Others.

<figure><img src="../../.gitbook/assets/image (61).png" alt="" width="563"><figcaption></figcaption></figure>

<table><thead><tr><th width="57.7110595703125" align="center"> </th><th width="153.0001220703125" valign="top">Element</th><th valign="top">Description</th></tr></thead><tbody><tr><td align="center">A</td><td valign="top">Uncoded segments</td><td valign="top">Check to include uncoded segments from uncoded responses.</td></tr><tr><td align="center">B</td><td valign="top">Coding suggestions</td><td valign="top">Help code others.</td></tr><tr><td align="center">C</td><td valign="top">Cluster</td><td valign="top">Cluster segments of that code.</td></tr></tbody></table>

## Coding Suggestions

<figure><img src="../../.gitbook/assets/image (160).png" alt="" width="563"><figcaption><p>Select uncoded segments to move them into suggested codes from the codebook, then click on OK.</p></figcaption></figure>

## Export to Ascribe Coder

<figure><img src="../../.gitbook/assets/image (62).png" alt="" width="563"><figcaption></figcaption></figure>

## Visualize Results

<figure><img src="../../.gitbook/assets/image (63).png" alt="" width="563"><figcaption></figcaption></figure>

<table><thead><tr><th width="57.7110595703125" align="center"> </th><th width="153.0001220703125" valign="top">Element</th><th valign="top">Description</th></tr></thead><tbody><tr><td align="center">A</td><td valign="top">Visualize</td><td valign="top">Data reporting tools to help visualize progress.</td></tr><tr><td align="center">B</td><td valign="top">Ask</td><td valign="top">Ask questions, format the answers, to work with the AI analysis tool to find context.</td></tr></tbody></table>
