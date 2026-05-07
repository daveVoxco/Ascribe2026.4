---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/frequently-asked-questions/load-and-download-data-questions
---

# Load and Download Data Questions

**My question was automatically marked as the wrong question type when data was loaded; how do I resolve this?**

The Ascribe logic for assigning a question type upon data load is as follows:

<table><thead><tr><th width="286.6666259765625" valign="top">Question Type</th><th valign="top">If the first response for the question is...</th></tr></thead><tbody><tr><td valign="top">Open End</td><td valign="top">…textual and greater than 15 characters</td></tr><tr><td valign="top">Closed End</td><td valign="top">…numeric and less than 15 characters</td></tr><tr><td valign="top">Other Specify</td><td valign="top">…textual and less than 15 characters</td></tr></tbody></table>



**No code values appear in the data file; how do I resolve this?**

Usually, the codebook has not been numbered, or the code values are in the code description with the code text. This happens when codebooks have been pasted in from another source and there was not a tab between the code value and the code text.

&#x20;

**When I am running User Defined using \[ RVerbatim: qid] I get the following error message: "\[ RVerbatim: qid] references a question that does not exist in the study." How do I resolve this?**

The substitution value \[ RVerbatim: qid] is case sensitive. If the qid is Q32, then make sure the substitution value is \[ RVerbatim:Q32]. Likewise if it is q4, then the substitution value should be \[ RVerbatim:q4].
