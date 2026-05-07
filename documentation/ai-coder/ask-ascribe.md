---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/ai-coder/ask-ascribe
---

# Ask Ascribe

Ask Ascribe allows users to ask questions of a dataset and immediately receive relevant answers and a summary report based on the analysis of the data. Whether it’s identifying key themes, exploring customer emotions, or determining areas for improvement, Ask Ascribe offers AI-powered insights and reports instantly.

<figure><img src="../../.gitbook/assets/image (321).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
#### Segmentation limits

* The segment limit for Large Language Model processing is 25,000 segments.
* **If the limit of 25 000 is exceeded**: The system utilizes a representative sampling method (prioritizing code representation over random selection), dynamically adjusting the number of codes downward until the 25,000 total limit is met.
{% endhint %}

{% hint style="success" %}
#### Tips

**Click hyperlinked terms** (bold) within the _Results_ (e.g., specific phrases like "excellent service") to view the underlying representative segments in the [#comments-window](ask-ascribe.md#comments-window "mention").
{% endhint %}

**Location**: The Ask Ascribe feature can be accessed from either the Edit or Visualize page in AI Coder (if the license is activated).&#x20;

**Fields**

<table><thead><tr><th width="276" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Explain what the data is about</td><td valign="top">If you entered a context when analyzing the data, that information will be displayed here. If not, then you can enter the context.</td></tr><tr><td valign="top">Select or type your query below</td><td valign="top">Select a question from the drop-down list or enter your own question in the text box.</td></tr><tr><td valign="top">Specify Results Format</td><td valign="top">Choose from bullet lists (short descriptions), bullet lists with details (description with more explanation) or paragraphs (longer text summary).</td></tr><tr><td valign="top">Break Down Results By</td><td valign="top">Choose a closed-end from the drop-down list. Choosing a closed-end will apply your query to each variable and will provide specify results to each variable group in your data.</td></tr><tr><td valign="top">Apply Filter to Data</td><td valign="top">Enter text to filter the results if you want to see answers to a specific topic or word.</td></tr><tr><td valign="top">Results</td><td valign="top"><p>After you click the Launch Query button, results display in the Results text box. You can download the results to your clipboard or HTML using the buttons at lower right.</p><p>Ask saves the last answer from session to session. If you want to ask the same question to see if the system provides a better answer, you must clear the results first.</p></td></tr></tbody></table>

**Bottom toolbar**

<figure><img src="../../.gitbook/assets/image (359).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="211.199951171875" align="center" valign="top">Button</th><th valign="top">Description</th></tr></thead><tbody><tr><td align="center" valign="top"><img src="../../.gitbook/assets/image (322).png" alt="" data-size="original"><br>Download as Word</td><td valign="top">Download a word (.doc) version of the results.</td></tr><tr><td align="center" valign="top"><img src="../../.gitbook/assets/image (323).png" alt=""><br>Download Results</td><td valign="top">Downloads the results to HTML.</td></tr><tr><td align="center" valign="top"><img src="../../.gitbook/assets/image (324).png" alt=""><br>Copy to Clipboard</td><td valign="top">Copy the result to your clipboard.</td></tr><tr><td align="center" valign="top"><img src="../../.gitbook/assets/image (326).png" alt=""><br>Clear Results    </td><td valign="top">Clears the results. Ask saves the last answer from session to session. If you want to ask the same question to see if the system provides a better answer, you must clear the results first.</td></tr></tbody></table>

## Comments window

**Click hyperlinked terms** (bold) within the _Results_ (e.g., specific phrases like "excellent service") to view the underlying representative segments.

<figure><img src="../../.gitbook/assets/image (375).png" alt=""><figcaption></figcaption></figure>

**Comments window tabs**

{% tabs %}
{% tab title="Responses" %}
Click on the _Responses_ tab to see the responses that were used as a source for the Ask report.&#x20;

* Click on a response to see the related respondent info.
* Click the <img src="../../.gitbook/assets/image (360).png" alt="" data-size="line"> to extract a csv version of the data.

<figure><img src="../../.gitbook/assets/image (372).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Top Quotes" %}
Click on the _Top Quotes_ tab to see an AI generated list the most representative and interesting quotes extracted directly from responses given by the respondents.&#x20;

* Click on a quote to see it in its full context.
* Click the <img src="../../.gitbook/assets/image (360).png" alt="" data-size="line"> to extract a csv version of the data.
* Check the Weigh % on sample size to change Closed Ends graph calculation to their weight relative to the sample size.

<figure><img src="../../.gitbook/assets/image (374).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Closed Ends" %}
Click on the _Closed Ends_ tab to see the report based on choice answers.

* Click on a graph to generate a visualization for it.
* Click the <img src="../../.gitbook/assets/image (360).png" alt="" data-size="line"> to extract a csv version of the data.
* Check the Weigh % on sample size to change Closed Ends graph calculation to their weight relative to the sample size.

<figure><img src="../../.gitbook/assets/image (373).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}
