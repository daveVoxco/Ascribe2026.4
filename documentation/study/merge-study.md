---
description: Combine study data so you can work and report from a single study.
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/study/merge-study
---

# Merge Study

_Navigate: Supervisor/Studies/Right-click study/Click Merge Study_

When you merge a study, you take information from a saved study file and add it to an existing study. The merge does not create a new study. An item from the saved study file is added to the existing study if it does not already exist.

**Reasons to merge a study:**

* Maintain codebooks across waves or trackers
* Save time when you set up waves and trackers.

The table below lists the components of an Ascribe study and how they are affected by a merge operation.

<table><thead><tr><th width="209" valign="top">Component</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top"><strong>Study</strong></td><td valign="top">The study setup information (the information entered in the study edit dialog box) is never modified by a merge.</td></tr><tr><td valign="top"><strong>Codebook and Codes</strong></td><td valign="top"><ul><li>If the study has no questions, the questions and the codebooks from the merged study are added. The codes and the nets are added. Ascribe creates a share between the studies.</li><li>If the study has the same question IDs as the merged study, the codebooks are not added, and Ascribe does not create a share between the studies.</li></ul></td></tr><tr><td valign="top"><strong>Question</strong></td><td valign="top">The question is added if there is no question in the existing study with the question ID of the merged question.</td></tr><tr><td valign="top"><strong>Response</strong></td><td valign="top">If you select to add responses, the response is added if there is no existing response with the respondent ID of the merged response.</td></tr><tr><td valign="top"><strong>Codes Applied to a Response</strong></td><td valign="top">Codes applied to responses are never added in a merge operation.</td></tr><tr><td valign="top"><strong>Quality Codes Applied to a Response</strong></td><td valign="top">Quality codes applied to a response are never added in a merge operation.</td></tr><tr><td valign="top"><strong>Question Relationship</strong></td><td valign="top">Question relationships are never added in a merge operation. See <a href="../ascribe-coder/codebooks/copy-share-manager.md#related-questions">Related Questions</a>.</td></tr></tbody></table>

## How to Merge a Study <a href="#minitocbookmark2" id="minitocbookmark2"></a>

_Navigate: Studies/Right-click a study/Select Merge Study_

When you merge a study, you have a master study and a target study. The master study has the information you want to add to the target study. Both the master study and the target study must exist on the Ascribe site. If the master study is not on the site, use the [restore](restore-a-study.md) option to load it to the site. The target study can be a new study or an existing study.

Here are the steps to merge a study:

1. [Save](save-a-study.md) the master study to your computer.
2. Right-click the target study and choose **Merge Study.** The Merge Study page displays.
3. Click the browse box to locate the master study you saved in step 1.
4. Choose **Questions, Codebooks, Responses** or **Questions, Codebooks.**
5. Click **Ok**. The job is submitted. When it is finished, the Jobs page displays to let you know the status.

## Restore and Merge via the FTP Site <a href="#minitocbookmark3" id="minitocbookmark3"></a>

The merge and restore facilities allow you to conveniently develop automated systems for moving studies and response data into Ascribe from the FTP site. You can perform a complete setup of Ascribe studies automatically, and load data incrementally into existing studies.

### Data File Format <a href="#minitocbookmark4" id="minitocbookmark4"></a>

The same file format is used for both the restore and merge operations. The name of the file is of no significance, other than that it must end with the extension .zip, and that the extension must not conflict with any [load file types](../data-management/how-to-load-data/load-file-types.md). The zip file must contain one file with the extension .XML. This file must be an XML file in the Ascribe study archive format. The name of the XML file is also of no significance, other than that it must end with .XML.

The study in Ascribe is identified by the value contained in the StudyIDClient tag of the XML document. If no study exists with this ID, a restore operation is performed. If there is an existing study with this ID, a merge operation is performed.

### Study Restore <a href="#minitocbookmark5" id="minitocbookmark5"></a>

A restore operation creates a new Ascribe study. All of the information in the XML document is restored to the new study.

### Study Merge <a href="#minitocbookmark6" id="minitocbookmark6"></a>

Merge operations allow you to add information from a saved study file to an existing study. The merge operation adds new items found in the saved file, but does not affect any existing items in the study. Do not think of the merge operation as an "update" of the study, except that it adds new information. Existing items in the study are not changed, even if the same item exists in both files.

### Identification of Items to Merge <a href="#minitocbookmark7" id="minitocbookmark7"></a>

To use merge effectively, you need to understand how Ascribe decides to add an item to the existing study. The decision is based on the identifier for each type of item. If there is an existing item in the study with the same identifier, that item is not merged. In this case, the existing item is not affected by the merge operation.

The identifiers used for each item type is listed below:

<table><thead><tr><th valign="top">Item</th><th valign="top">Tag</th><th valign="top">Identifier</th></tr></thead><tbody><tr><td valign="top">Question</td><td valign="top">QuestionID</td><td valign="top">Question ID</td></tr><tr><td valign="top">Codebook</td><td valign="top">CodeBookGuid</td><td valign="top">CodeBookGuid</td></tr><tr><td valign="top">Response</td><td valign="top">DRORespondent</td><td valign="top">Respondent ID</td></tr></tbody></table>

Codes in a codebook are added to the study only if the codebook was itself added. The codebook will be added if there is no codebook in Ascribe with the corresponding CodeBookGuid.
