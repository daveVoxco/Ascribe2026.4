---
description: >-
  The AI Coder Analyze window is used to evaluate and interpret text responses,
  applying various coding techniques to categorize data effectively.
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/ai-coder/ai-coder-analyze
---

# AI Coder Analyze

This tool assists analysts in processing and managing large datasets by automating the coding process and allowing for precise adjustments through customizable coding options.

<figure><img src="../../.gitbook/assets/Ascribe 20264 Analyze window.png" alt="" width="540"><figcaption></figcaption></figure>

**Location:**

<details>

<summary>New project</summary>

1. Click the **Studies** button under Coder on the Home page
2. **Load Your Data**: Begin by uploading or loading the dataset you wish to analyze.
3.  Open the **questions** list for the selected study

    <figure><img src="../../.gitbook/assets/image (120).png" alt="" width="563"><figcaption></figcaption></figure>


4.  &#x20;Click the **AI Coder icon** for the desired question

    <figure><img src="../../.gitbook/assets/image (121).png" alt="" width="563"><figcaption></figcaption></figure>



The Analyze dialog will be displayed if no clustering analysis was run on this data before.

</details>

<details>

<summary>Existing project</summary>

Click the **Analyze** button in the top toolbar to launch the AI Coder Analyze.

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

The Analyze dialog will display a different set of options when it is used on an existing AI Coder analysis:

<figure><img src="../../.gitbook/assets/image (110).png" alt=""><figcaption></figcaption></figure>

</details>

## Options

<table><thead><tr><th width="255.5111083984375" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">New Responses<br><strong>This option is only visible when loading additional data into an existing analysis.</strong></td><td valign="top"><p>When additional data is loaded to a question, this section displays and indicates how many new responses were found.</p><p>Click the checkbox to add new/unanalyzed responses to the existing project using the project's current options. This option retains the current analysis and adds results to the analysis. It is helpful if you want to keep the results in AI Coder and use the visuals or Excel export to report on all the data.</p></td></tr><tr><td valign="top">Codebook</td><td valign="top"><ul><li><strong>New Codebook:</strong> analyzes the responses and creates a new AI Codebook</li><li><strong>Select a saved or trained codebook</strong> from the drop-down list if you want to use a previously-created codebook. Use the <a href="ai-coder-analyze.md#minitocbookmark2">View Codebook</a> button to display the codebook and select how the codebook is applied.</li></ul><p><strong>When using a saved or trained codebook</strong>, you can suggest new codes. These codes display in a net called Suggested New Codes.</p><p></p><p><strong>Options </strong><em><strong>only</strong></em><strong> available with an existing analysis:</strong></p><ul><li><strong>Use Current Codebook:</strong> this option displays when an AI Coder codebook was created for the question and more data has been added to the question; the option will keep the codes that were exported from AI Coder to Ascribe Coder synchronized, which allows for using AI Coder to analyze projects with multiple loads. When using this option, the codebook is automatically saved and rules are created. This option creates a new analysis using the new and uncoded responses. Therefore, the totals only reflect the current data. This option is useful when you are exporting interim loads to Ascribe Coder.</li><li><strong>Train Ascribe Codebook:</strong> If the question has coded data with this codebook, the system analyzes the coded responses and creates an AI Codebook using the same codes and nets. If the codebook has not been used for coding, the system creates an AI Codebook using the code descriptions and then applies the codes to the responses. Rules for each code are created when you save the codebook. You can view the rules from the Saved Codebooks option.</li></ul><p></p></td></tr><tr><td valign="top">Generate Segments</td><td valign="top"><p><strong>When working with an existing analysis:</strong> you have the option to not re-segment the data.</p><p> </p><p>Generating segments takes more time than clustering existing segments; therefore, if you don't select Generate Segments, you can change the proximity settings without going through the segmenting process again.</p></td></tr><tr><td valign="top">Generative AI Segmenting</td><td valign="top"><p>Select this option if you want to use Generative AI.</p><ul><li><strong>Context:</strong> Enter information about the data.</li><li><strong>Codebook Language:</strong> The codes will display in the language you select.</li><li><strong>Translate responses to English for analysis:</strong> This option translates the responses to English to improve AI analysis accuracy. It is helpful for Hebrew and other double-byte languages. When selected, the segments will display in English.</li></ul><p>See <a href="ai-coder-analyze.md#minitocbookmark4">AI Coder and Languages When Using Generative AI</a> for more information.</p></td></tr><tr><td valign="top"><p>Split Characters</p><p>Split Words<br></p></td><td valign="top"><p><strong>These options are only available when Generative AI Segmenting is disabled.</strong></p><p></p><p>Non-generative AI Coder uses the split characters and split words to parse responses into segments.</p><p></p><p><strong>Defaults</strong>:</p><ul><li><strong>Split Characters</strong>: <code>,.!?|;\&#x26;/{-</code> </li><li><strong>Split Words</strong>: but, however, nevertheless, nonetheless, yet, although, and, so, with, at, then, that, this, of, for, when, while.</li></ul></td></tr><tr><td valign="top">Words To Ignore</td><td valign="top"><p>Enter any words that should be skipped during analysis. Words and groups of words can be separated by a space, a comma or semicolon. </p><p>i.e.: great, works well, excellent product</p></td></tr><tr><td valign="top"><p>Responses Are In English</p><p>(Non-Generative AI)</p></td><td valign="top">If checked, the system uses an all-English model, and if not, a multi-lingual model is used. Only used in non-generative AI.</td></tr><tr><td valign="top"><p>All responses (Coded and Uncoded)</p><p>or</p><p>Uncoded Only</p></td><td valign="top"><p>Choose to analyze coded and uncoded responses or uncoded only.</p><p> </p><p><strong>Coded Only</strong> is the only option when Train Ascribe Codebook is selected in the Codebook menu; when active the system will only look at coded responses when training.</p></td></tr></tbody></table>

## Codebook generation methods

### Primary Method Selection

<table><thead><tr><th width="253.11114501953125" valign="top">Generation method</th><th valign="top">Recommendation</th></tr></thead><tbody><tr><td valign="top">Codebook Builder</td><td valign="top"><strong>Recommended for new projects</strong>. Uses the newest AI engine with significantly improved processing speed and classification capabilities.</td></tr><tr><td valign="top">Theme Extractor (Legacy)</td><td valign="top"><strong>Uses the Generation AI analysis method</strong>. Should only be used when matching results from older projects.</td></tr></tbody></table>

#### Codebook Builder

<figure><img src="../../.gitbook/assets/Ascribe 20264 code builder selected.png" alt="" width="518"><figcaption></figcaption></figure>

{% hint style="success" %}
#### Tip

Begin with Medium granularity and 80% strictness, then adjust based on results
{% endhint %}

<table><thead><tr><th width="240.577880859375" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Codebook Creation Method</td><td valign="top"><p><strong>AI-Generated:</strong> Sets the maximum number of codes (LLM may create fewer)</p><ul><li>The LLM analyzes your data and creates the codebook structure</li><li>Dynamically determines the optimal number of codes up to the granularity maximum</li><li>Recommended for <em>most</em> use cases</li></ul><p><br><strong>Data-Driven:</strong> Sets the target number of clusters</p><ul><li>Clusters responses using k-means based on granularity setting, then uses the LLM to generate labels</li><li>Granularity determines the target number of clusters</li><li>Useful when you want clustering to drive the structure</li></ul></td></tr><tr><td valign="top">Codebook Granularity</td><td valign="top"><strong>Options</strong>: Low / <em>Medium (default)</em> / High</td></tr><tr><td valign="top">Classification Strictness</td><td valign="top"><p><strong>Default</strong>: 80%</p><ul><li><strong>Lower values (75-84%)</strong>: More lenient matching - responses are more easily classified</li><li><strong>Higher values (85-95%)</strong>: Stricter matching - responses must closely align with codes</li></ul></td></tr><tr><td valign="top">Minimum Responses per Code</td><td valign="top"><p><strong>Default</strong>: 3 responses</p><ul><li>Sets the threshold for code inclusion in the codebook</li><li>Codes with fewer responses than this will be merged or removed</li></ul></td></tr><tr><td valign="top">Max. Number of Topic-Based Codes</td><td valign="top"><p><strong>Default</strong>: 10 codes</p><ul><li>Sets the maximum number of topic-based codes to generate</li><li>Can be disabled by unchecking the option</li></ul></td></tr></tbody></table>

#### Theme extractor (Legacy)

<figure><img src="../../.gitbook/assets/image (376).png" alt="" width="534"><figcaption></figcaption></figure>

<table><thead><tr><th width="236.31109619140625" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Analyze by closed-end question</td><td valign="top">(Default Closed Ends) Allows you to give the system more context of the data. Select the closed-end from the drop-down list and a dialog opens where you can add information. A codebook is created for each code and then merged into one codebook.</td></tr><tr><td valign="top">Edit codebook builder prompt</td><td valign="top">Allows you to enter your own codebook builder prompt and make specific requests for the codebook.</td></tr><tr><td valign="top">Codebook granularity</td><td valign="top">(Default Low) Select from low (one codebook is created), medium (three codebooks are created and then merged into one) or high (six codebooks are created and then merged into one.) When using medium or high, the results may contain more codes, and the codes may be more specific. This option can be used if you are not analyzing by a closed-end question. If you only have a small number of responses, then low is most appropriate. The other two options are usually for questions that have large amounts of data.</td></tr><tr><td valign="top">Max number of nets</td><td valign="top">(default 10)</td></tr><tr><td valign="top">Max number of codes</td><td valign="top">(default 100)</td></tr></tbody></table>

## Actions

<figure><img src="../../.gitbook/assets/image (107).png" alt="" width="563"><figcaption></figcaption></figure>

<table><thead><tr><th width="233.2001953125">Button</th><th valign="top">Description</th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (129).png" alt="" data-size="original"></td><td valign="top">Close dialog without taking any action.</td></tr><tr><td><img src="../../.gitbook/assets/image (108).png" alt="" data-size="original"></td><td valign="top"><ul><li><strong>Save as Default</strong>: Keep the current configuration as default for future use.</li><li><strong>Restore My Default</strong>: Restore the last saved personal default, can be used after restoring the ascribe default.</li><li><strong>Restore Ascribe Default</strong>: Revert the options to factory defaults on this dialog.</li></ul></td></tr><tr><td><img src="../../.gitbook/assets/image (106).png" alt=""></td><td valign="top">(Only available on initial run) Click the <em>Run Analysis</em> button to start the first analysis on a question. </td></tr><tr><td><img src="../../.gitbook/assets/image (133).png" alt="" data-size="original"></td><td valign="top">(Only available on re-runs) Click the Re-cluster Segments button to re-run the analysis with the current settings.</td></tr></tbody></table>

## View Codebook <a href="#minitocbookmark2" id="minitocbookmark2"></a>

This function is available when the _Apply an existing codebook_ option is selected, it displays the selected codebook prior to analysis. Three configurable options are available at the top of the interface to control how the codebook is applied to the data.

<figure><img src="../../.gitbook/assets/image (109).png" alt="" width="563"><figcaption></figcaption></figure>

## View Codebook options

<figure><img src="../../.gitbook/assets/image (117).png" alt="" width="563"><figcaption></figcaption></figure>

{% hint style="danger" %}
### Important

The options are displayed in the order they will be applied when selected.&#x20;



When all three options are checked, the system first looks at regular expressions, then training examples, and last, the coding rules. You can choose any combination of the three options.
{% endhint %}

<table><thead><tr><th width="230.66668701171875" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Apply Regular Expressions</td><td valign="top"><ul><li>If the codebook has regular expressions, they are displayed below each code.</li><li>If the codebook was created from a codebook in Ascribe Coder, the regular expressions are imported from there.</li><li>You can edit the expressions in this dialog.</li><li>Click the checkbox next to Apply regular expressions if you want the system to first apply the expressions before using other two options.</li></ul></td></tr><tr><td valign="top">Apply Training Examples</td><td valign="top"><ul><li>The training examples are the individual segments that were assigned the code.</li><li>Click the code name to see the segments.</li><li>You can delete segments or cut/paste segments to change their order in the list.</li><li>Click the checkbox next to Apply training examples if you want the system to apply the training examples.</li></ul></td></tr><tr><td valign="top">Apply Coding Rules</td><td valign="top"><ul><li>When a codebook is saved, coding rules are created.</li><li>You can edit the rules in this dialog.</li><li>Click the checkbox next to Apply coding rules if you want the system to apply the rules.</li></ul></td></tr></tbody></table>



## Process Order for Codes <a href="#minitocbookmark3" id="minitocbookmark3"></a>

You can manually assign a process order to the codes in the View Saved Codebook dialog. Next to the regular expression text box for each code is the Codebook Order box. If you want the codes to be applied in a certain order, enter the number in that box. The system will give priority to the numbered codes.

<figure><img src="../../.gitbook/assets/image (116).png" alt="" width="563"><figcaption></figcaption></figure>

## AI Coder and languages when using generative AI <a href="#minitocbookmark4" id="minitocbookmark4"></a>

In the Analysis dialog, you have choices for handling languages:

* Codebook Language drop-down with various languages. The default is English.
* Translate Responses to English: displays the segments and responses in English. If the responses to be analyzed are in English, you don't need to select translate. This option is most helpful for Hebrew and other double-byte languages.

Here's a chart for quick reference:

| Codebook Language | Translate Responses to English | Segments    | ASK Results | ASK Drill-Down |
| ----------------- | ------------------------------ | ----------- | ----------- | -------------- |
| English           | Yes                            | English     | English     | English        |
| Non-English       | Yes                            | English     | Non-English | English        |
| Non-English       | No                             | Non-English | Non-English | Non-English    |
| English           | No                             | English     | English     | English        |

When you use a non-English codebook and translate the responses, the ASK results and drill-down responses may not give the best results.

## Load Closed-Ended Questions <a href="#minitocbookmark5" id="minitocbookmark5"></a>

If you need to load or update closed-ended questions after an analyzing a question, click the Visualize button (you must have a license for AI Coder Charts).&#x20;

<figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

In the section, click the Load Closed-Ends button. The closed ends must be marked as Closed.

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

If the closed-ended question has a codebook, the system will use those values.
