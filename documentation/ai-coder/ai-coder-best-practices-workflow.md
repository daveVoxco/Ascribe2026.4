---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/ai-coder/ai-coder-best-practices-workflow
---

# AI Coder Best Practices Workflow

## Phase One: Review Initial Analysis

Once analysis is complete, review the results to decide if you have a good starting point or need to re-analyze.

**Key metrics to check:**

* Percent coded - Is coverage appropriate for your data?
* Number of codes - Does this align with your expected scope?
* Nets - Do the high-level groupings make sense?

**Review the codebook quality.** Read through a portion of the codebook to verify:

* Code names and descriptions meet your expectations
* Terminology aligns with your research objectives
* Code descriptions are clear and actionable

**Validate segments:** Check two or three of the most frequently used codes to ensure AI Coder is creating segment that understand and reflect your data accurately.

## Phase Two: Re-Analyze (if needed)

Identify Issues before you re-analyze.

**Common issues and solutions:**

* AI Coder misunderstanding data - Add or edit context information ("the data is about...")
* Specific codes missing - Use Codebook Builder prompt to instruct AI Coder to create these codes
* Need more context - Use  contextual closed-end questions (like rating questions)
* Codebook too large/small - Adjust max codes setting or granularity drop-down

## Phase Three: Cleaning and Upcoding

**Refine the codebook by working through it systematically:**

* Combine similar codes/ideas that represent the same concept
* Use Cluster option to break out codes that may house multiple ideas or are too inclusive/broad
* Review unclear or overly general code names - examine segments and rename codes to better reflect captured ideas

**Look closely at key codes:**

* Most frequently used codes
* General or ambiguous codes
* Codes that don't seem to fit well

**Look closely at segments:**

* Review segments using segment confidence sort
* Use keyword drop-down list for targeted review
* Move segments to better-fitting codes or create new codes as needed

**Review uncoded segments:**

* Enable both types of uncoded segments using the ‘show uncoded segments’ checkbox
* Change segment sort to Frequency to quickly find segments representing multiple responses
* Use keyword drop-down list to identify frequently mentioned words/ideas (more than a handful of times)
* Move recurring ideas to existing codes or create new codes as needed

**Final uncoded cleanup if too many uncoded segments remain:**

* Use Cluster Uncoded Segments button to have AI Coder group remaining uncoded segments into new codes
* These new codes will act like "Other" type codes ready for review
* Keep, delete, or clean these codes as you would any regular code
