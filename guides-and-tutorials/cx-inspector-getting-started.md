---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/guides-and-tutorials/cx-inspector-getting-started
---

# CX Inspector: Getting Started

## Generative or Non-Generative AI?

Generative AI summarizes the main idea(s) from each response into segments to create a codebook, whereas non-Generative AI uses split characters and split words to manually segment the responses prior to grouping into codes.

<table><thead><tr><th valign="top">Generative AI segment</th><th valign="top">Response</th><th valign="top">Non-Generative AI segment</th></tr></thead><tbody><tr><td valign="top"><p>-in-store pick-up option for online purchases</p><p> </p><p>-reduce shipping costs</p><p> </p><p>-missed sale due to high shipping costs</p></td><td valign="top"><em>Allow on-line items to be delivered to store without paying shipping. The shipping is about 1/3 of the price of the item and caused me not to purchase the item from your store.</em></td><td valign="top"><p>-allow on-line items to be delivered to store without paying shipping</p><p> </p><p>-the shipping is about 1/3 of the price of the item</p><p> </p><p>-caused me not to purchase the item from your store</p></td></tr><tr><td valign="top"><p>-poor customer service</p><p> </p><p>-lack of politeness</p></td><td valign="top"><em>at the conclusion of my purchase the cashier put my change in my hand and said nothing i said thank you and got no response, no have a good night, thanks for shopping here nothing</em></td><td valign="top"><p>-at the conclusion of my purchase the cashier put my change in my hand</p><p> </p><p>-said nothing i said thank you</p><p> </p><p>-got no response, no have a good night, thanks for shopping here nothing</p></td></tr><tr><td valign="top">-healthier bakery items</td><td valign="top"><em>better low fat and no sugar bakery items</em></td><td valign="top"><p>-better low fat</p><p> </p><p>-no sugar bakery items</p></td></tr><tr><td valign="top"><p>-proposal to extend the class schedule</p><p> </p><p>-suggestion to add classes on friday</p></td><td valign="top"><em>after 5:30pm classes. Can we add on for Friday?</em></td><td valign="top"><p>-after 5:30pm classes</p><p> </p><p>-can we add on for Friday</p><p> </p><p></p><p> </p></td></tr></tbody></table>

### Load Data / Create a Project:

1. **Format Data file if necessary.**\
   Note: CX Inspector accepts excel files with or without a respondent id column and/or a header row. Example of excel file:\
   ![](<../.gitbook/assets/image (301).png>)<br>
2.  **Upload and Analyze.**\
    Click the “Upload and Analyze” button to browse to and select the formatted data file. After selecting the data file, the “Excel Import” dialogue box opens.

    <figure><img src="../.gitbook/assets/image (300).png" alt=""><figcaption></figcaption></figure>


3. **Select Variables Analyze and analysis options**
   1. Select text fields to be analyzed. The variables correspond with the column headers from the data file. Ascribe will suggest data fields that contain varied textual comments; only select the fields that need categorized.\
      ![](<../.gitbook/assets/image (298).png>)<br>
   2. Note: All fields listed in the “Closed-end” area will be available for filters, crosstab banners, and creating custom dimensions.\
      ![](<../.gitbook/assets/image (299).png>)

### Generative AI Options

* The data is about -- provide context describing the comments to be analyzed. Example: a mascara product; a fitness club review; a financial institution; an ice cream shop; a dog food survey response
* Codebook language – choose a language for the results. The codebook or categories will be created in the chosen language.\
  ![](<../.gitbook/assets/image (302).png>)

### Overview of “Excel Import” dialog

Select “Analyze” to start the analysis process and create the project. CX Inspector extracts the main ideas from each comment, then groups similar ideas together to create codes. The result is a list of “codes” that can be visualized instantly.

<figure><img src="../.gitbook/assets/image (303).png" alt=""><figcaption></figcaption></figure>

### Visualize Results

<figure><img src="../.gitbook/assets/image (304).png" alt=""><figcaption></figcaption></figure>

## Using the Edit Tool

{% stepper %}
{% step %}
### Review the percentage coded and number of codes created once the analysis is done.

Do you need more codes? You might experiment with the Analysis settings and re-analyze to get more data coded.

1. Use the Analyze button to bring up the analysis options
2. Use the Initial Codes Min. Proximity value to control the initial coding
3. Raising the Initial Codes Min. Proximity value will code less data but will create more concise codes.
4. Lowering the Initial Codes Min. Proximity value will code a larger portion of the data and create somewhat more general codes.
5. If the created codes do not fit your data topic, provide more context about your data by changing the prompt.

<figure><img src="../.gitbook/assets/image (290).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (291).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Check the top five codes, are they named properly? Does the code represent the segments?

Check “Keywords” to see if anything stands out. Move segments as needed, either creating a new code, dragging into an existing code or using the Get Code Suggestions icon.

<figure><img src="../.gitbook/assets/image (292).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (293).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (294).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (295).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Combine redundant or overlapping codes. Use the AI Codebook keywords tool to isolate similar codes and combine as needed.

<figure><img src="../.gitbook/assets/image (297).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Net the codes: use the Netting tool to group codes into similar Nets. Rename the nets as appropriate and combine redundant codes.

<figure><img src="../.gitbook/assets/image (296).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

## Others Code and Uncoded Segments

{% stepper %}
{% step %}
### By default, the Others code displays uncoded segments belonging to partially coded responses.&#x20;

Enable the checkbox toggle on the Others code to display uncoded segments which are part of completely uncoded responses.
{% endstep %}

{% step %}
### Use any of the following tools to review and upcode the Others.

* Use “Keywords” to manually identify segments that fit existing codes or add new codes.
* Click on the Autocode Others icon to automatically generate additional codes from the segments in Others.
* Use the Help Code Others icon to bring up the Coding Suggestions window for the Others.

<figure><img src="../.gitbook/assets/image (288).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (289).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
