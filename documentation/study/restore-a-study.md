---
description: Restore a saved study backup into Ascribe.
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/study/restore-a-study
---

# Restore a Study

The save and restore features under Supervisor/Studies enable you to save and restore entire studies or their components to your hard drive or network.

This feature allows users to keep a "master" study or study templates in a central location and restore or merge them at any time to have a similar study. Users generally save and restore the last version of a tracker or wave study to decrease the amount of time spent to set up the studies.

To restore a study, you first must save the study. The restore operation returns the study to Ascribe.

## Restore Types <a href="#minitocbookmark2" id="minitocbookmark2"></a>

There are several types of study restore operations.

<table><thead><tr><th width="182.33331298828125" valign="top">Restore Type</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Original</td><td valign="top"><p>This option restores the study completely. The intention of this restore type is to allow you to save a study, delete it from Ascribe, and later restore it exactly as it was when you saved it.</p><p>Because this restore type is intended to restore a deleted study to its original condition, it causes an error if the study is still present in Ascribe. The study must be deleted from Ascribe before you can use this restore type.</p></td></tr><tr><td valign="top">Setup</td><td valign="top"><ul><li>This restore type is available only when you send a saved study file to Ascribe via the loader FTP site. It creates a new study in Ascribe and loads all of the information from the saved study. The restore operation will fail if there is a study in Ascribe with the same study ID as the one being restored.</li><li>This restore type differs from the Original restore type only in the way Ascribe checks whether the study already exists. With the Original restore type, Ascribe checks an internal identifier for the study (the StudyGuid). If a study exists in Ascribe with the same StudyGuid as the study being "restored as Original," the restore operation fails.</li><li>With the Setup restore type, Ascribe checks the study ID (the StudyIDClient tag in the XML document). If a study exists in Ascribe with the same study ID as the study being restored as Setup, the restore operation fails.</li></ul></td></tr><tr><td valign="top">Questions, Codebooks, Responses, Codes Applied</td><td valign="top"><p>This restore type, and the next ones listed in this table, create a new study in Ascribe. With these restore types, you must provide a study ID and a study name. The study ID you provide may be changed by Ascribe if a study already exists with this study ID.</p><p>This restore type loads all of the information from the saved study, with these exceptions:</p><ul><li>The study ID and study name are set to the values you provide;</li><li>The start date of the study is set to the current date;</li><li>The status of the study is set to under construction.</li></ul></td></tr><tr><td valign="top">Questions, Codebooks, Responses</td><td valign="top">This restore type is identical to the <em>Questions, Codebooks, Responses, Codes applied</em> restore type, except that the codes applied are not loaded. All responses in the restored study have the coding removed.</td></tr><tr><td valign="top">Questions, Codebooks</td><td valign="top">This restore type is identical to the <em>Questions, Codebooks, Responses</em> restore type, except that the responses are not loaded. This restore type is useful when you want to use a saved study as a template for a new study.</td></tr><tr><td valign="top">Questions</td><td valign="top">This restore type is identical to the <em>Questions, Codebooks</em> restore type, except that codebooks are not restored. Each question is restored with an empty codebook.</td></tr></tbody></table>

## Restore Shared Codebooks <a href="#minitocbookmark3" id="minitocbookmark3"></a>

When you restore a study, shared codebooks may or may not remain shared. Codebooks that are shared within a study remain shared. Codebooks that were shared across studies do not remain shared with those studies. For example, Q1 of Study A shares a codebook with Q1 of Study B. If we save Study A and then restore it as Study C, we find that Q1 of Study C no longer shares a codebook with Study B. The codebook is restored, but the shared connection is broken.

It is possible to restore shared connection of codebooks across studies using a [merge](merge-study.md) instead of a restore.

## How to Restore a Study <a href="#minitocbookmark4" id="minitocbookmark4"></a>

_Navigate: Supervisor/Studies/Click Restore Study_

After you select to restore a study, a screen displays with these fields:

<table><thead><tr><th width="212.33331298828125" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Study File</td><td valign="top"><p>Enter the name of the file to restore, or click Browse... to locate the file. You can use either the original zip file that was saved, or the XML file that you extracted from the zip file.</p><p>Use of the original zip file is recommended because it is much smaller than the XML file and takes less time to transfer.</p></td></tr><tr><td valign="top">New Study ID</td><td valign="top">This entry is available only if you have not selected the <strong>Restore as original</strong> option. Type the study ID for the new study.</td></tr><tr><td valign="top">New Study Name</td><td valign="top">This entry is available only if you have not selected the <strong>Restore as original</strong> option. Type the study name for the new study.</td></tr><tr><td valign="top">Restore as Original</td><td valign="top"><p>This option uses the study ID and study name from the saved study. Use this option if you want to restore a deleted study with the same study ID and name as the saved study. The restore operation will fail if the original study has not been deleted.</p><p>Prior to 01/29/2010, Ascribe did not restore the name of the coder who applied a code to a response. After that date, the coder name is restored. The load information is not restored in either case.</p><p>Account codebook designations are not restored. Codebook IDs are restored if the codebook ID is unique to the site.</p></td></tr><tr><td valign="top">Restore as New Study</td><td valign="top">Questions, Codebooks, Responses, Codes Applied: This option restores all information in the saved study, creating a new study.<br><br>Questions, Codebooks, Responses: This option creates a new study, but does not include any codes applied from the saved study.<br><br>Questions, Codebooks: This option creates a new study, but does not restore the responses and codes applied from the saved study.</td></tr></tbody></table>

After you enter the information, click OK to submit the job. When it finishes, the [Jobs page](../data-management/manage-jobs.md) displays.
