---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/ascribe-illustrator/weighting-results
---

# Weighting Results

In order to weight the results in Illustrator, you must have a Data question in the study, which contains the respondent IDs and their corresponding weights.

Here is an example:

| Respondent ID | Weight |
| ------------- | ------ |
| 848100        | 1.1    |
| 848110        | 0.75   |
| 845000        | 1.25   |
| 842000        | 1      |

When an illustration is created for that study, the weighting data question(s) display in the [Illustration Tools](tools.md#options).

By default, no weighting question is selected (blank choice). In that case, ALL the results will be un-weighted meaning that each respondent gets assigned a weight of 1.

Once the users select a weighting question, absolutely ALL visualizations (bar charts, cross-tabs, co-occurrence, etc.) take the weights into account.

For example, if all females have a weight of 1.1 and Illustrator counts 100 females in a cell, that cell will display 110.

If a respondent has a weight of 0, that respondent will be ignored.

### **What if some respondents are omitted from the weighting Question?**

In that case, they get the “[Default Weight](tools.md#options)” set in Illustration Tools, which can be either 1 or 0.

### **How to use a weighting question to “Ignore” some respondents?**

There are two ways to do this:

The users load a weighting question that contains the respondents to be ignored by making sure that their weights is set to 0 and that the “Default Weight” is set to 1.

| Respondent ID | Weight |
| ------------- | ------ |
| 92100         | 0      |
| 92101         | 0      |
| 92102         | 0      |

In this example, respondents 92100, 92101, 92102 will be ignored.

The users load a weighting question that contains ONLY the respondents they want to take into account by making sure that their weights is set to 1 (or something else that is not 0) and that the “Default Weight” is set to 0.

| Respondent ID | Weight |
| ------------- | ------ |
| 92100         | 1      |
| 92101         | 1      |
| 92102         | 1      |

In this example, respondents 92100, 92101, 92102 will be the only ones taken into account.
