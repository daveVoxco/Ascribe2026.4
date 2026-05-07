---
description: >-
  Follow the workflow for best results when coding brands using Ascribe's
  non-generative AI Coder.
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/guides-and-tutorials/coding-brands-in-ai-coder
---

# Coding Brands in AI Coder

## Data Formatting

If working with iterated brand lists/questions the first thing to consider is how the data will be loaded into Ascribe.

* Option 1 – Load each iteration as its own question and then share all iterations together
  * Once the questions are shared they can then be analyzed in AI Coder all at once
* Option 2 – Rename all iterations to the same Question ID so that the data is concatenated on load
  * If Option 2 is used, you will need to use the “pipe” symbol as a split character when analyzing the data in AI Coder.

## Analyzing

* The Generative AI option should be turned off when coding brands or other similar responses.
* Split Characters
  * Depending on your data you will want to use either no, or very limited split characters
  * Use the pipe if working with concatenated data
  * A comma as a split character will be useful if the responses look like “Clorox, Store Brand, Puffs”
* Split Words
  * Depending on your data you may want little to no split words
  * Some of the more common split words include “Then, Or, And”
* Minimum codebook creation proximity
  * This value will dictate how precise the initial grouping of segments has to be when creating the codebook during AI Coder’s first pass
  * For branding you will want to start with at least 85 or 90. Move up or down as needed
* Minimum coding proximity
  * The larger this value the more exact the relationship between upcoded segments during AI Coder’s second pass through your data
  * For branding it’s recommended to start at 75 and move up as needed
* It’s possible that you may need to re-analyze the data two or three times until you find the combination of proximity values that work best with your data

<figure><img src="../.gitbook/assets/image (305).png" alt=""><figcaption></figcaption></figure>

## Clean up and Coder Export

* Check the codes, are they named properly? Does the code represent the segments? Check “Keywords” to see if anything stands out. Move segments as needed, either creating a new code or dragging into an existing code
* Combine redundant or overlapping codes. Use the AI Codebook keywords tool to isolate similar codes and combine as needed.
* Check the others code
  * Use The Autocode Others and Help Code Others tools
  * Use “Keywords” to identify segments that might fit existing codes or to add new codes.
* Export to Ascribe Coder
