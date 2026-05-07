---
description: Analyze response quality issues that can affect coding accuracy.
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/verbatims/edit-verbatims/data-quality-analysis
---

# Data Quality Analysis

The Data Quality Analysis (DQA) allows users to detect, remove, or clean specific criteria from responses, generating a detailed Excel report. It streamlines error checking and management, benefiting you by allowing you to identify and address errors efficiently, leading to more reliable survey results.

<figure><img src="../../../.gitbook/assets/image (136).png" alt="" width="563"><figcaption></figcaption></figure>

## Accessing Data Quality Analysis

Data Quality Analysis can be launched from two locations:

<details>

<summary>Project Level</summary>

**Location**: Supervisor/Right-click study/Click Data Quality Analysis

<figure><img src="../../../.gitbook/assets/image (134).png" alt="" width="563"><figcaption></figcaption></figure>

This launches DQA for all questions in the study, allowing you to select which questions to analyze within the tool.

</details>

<details>

<summary>Question Level</summary>

**Location**: Studies (Questions view) / Select one or more questions / Click Data Quality Analysis...

When questions are selected in the Questions view, the Data Quality Analysis button becomes available in the toolbar. This pre-selects those questions for analysis, allowing you to focus quality checks on specific questions of interest.

</details>

## Permissions and Requirements

Transactions are incurred when an item is detected or cleaned. A transaction is incurred per response flagged; it does not charge per detection item found. In other words, if a response has multiple detections, a transaction is only charged once for the response. If a code is added in Ascribe Coder for a detection category, a text transaction is also incurred.

* _Only_ users with Supervisor or Administrator privilege have access to the Data Quality Analysis.
* **If the license for Generative AI is turned off at the account level**, AI-powered detection options (Names, Safety/Security Issues, Low Effort Responses, Off Base Responses, and AI Bot Responses) will not be available.

## Detection Options

<figure><img src="../../../.gitbook/assets/image (135).png" alt=""><figcaption></figcaption></figure>

### AI-Powered Analysis

<table><thead><tr><th width="231.0667724609375" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Enable AI detection engine</td><td valign="top">Check this option to enable all AI-powered detection capabilities. When disabled, only rule-based detections are available.</td></tr></tbody></table>

### Content Quality

<table><thead><tr><th width="228.933349609375" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Nonsense responses</td><td valign="top">Detects nonsense characters in responses.</td></tr><tr><td valign="top">Safety and security issues<br>(Requires AI)</td><td valign="top">Detects responses indicating safety concerns, harm, adverse events, or threats.</td></tr><tr><td valign="top">Profanity and inappropriate language<br>(English Only)</td><td valign="top"><p>Detects profane or inappropriate language.</p><ul><li><strong>(Detect hidden):</strong> flags responses in the report</li><li><strong>Redact:</strong> replaces flagged content with asterisks in the verbatim (original verbatim preserved in report)</li></ul></td></tr></tbody></table>

### Response Quality

<table><thead><tr><th width="233.9111328125" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Low Effort Responses<br>(Requires AI)</td><td valign="top">Detects responses that are incomplete or minimal answers.</td></tr><tr><td valign="top">Off-Base Responses<br>(Requires AI)</td><td valign="top"><p>Detects responses that don't answer the question asked.</p><ul><li><strong>(Detect hidden)</strong>: flags responses in the report</li><li><strong>Redact:</strong> replaces flagged content with asterisks in the verbatim (original verbatim preserved in report)</li></ul></td></tr><tr><td valign="top">Bot/AI generated responses<br>(Requires AI)</td><td valign="top">Detects responses that appear to be created by AI or automated systems.</td></tr><tr><td valign="top">Duplicate responses</td><td valign="top"><p>Detects duplicate responses with configurable scope:</p><ul><li><strong>Question:</strong> flags duplicated responses within the same question</li><li><strong>Respondent:</strong> flags duplicates from the same respondent across questions</li><li><strong>Response Minimum Length:</strong> responses shorter than this length are not considered for duplicate detection (default: 25 characters)</li></ul></td></tr></tbody></table>

#### Privacy and Personal Data

<table><thead><tr><th width="234.622314453125" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Personally identifiable information</td><td valign="top"><p>Detects phone numbers, social security numbers, and other PII such as addresses.</p><ul><li><strong>(Detect hidden)</strong>: flags responses in the report</li><li><strong>Redact</strong>: replaces detected PII with asterisks in the verbatim (original verbatim preserved in report)</li></ul></td></tr><tr><td valign="top">Personal names<br>(Requires AI)</td><td valign="top"><p>Detects names in responses.</p><ul><li><strong>(Detect hidden)</strong>: flags responses in the report</li><li><strong>Redact</strong>: replaces detected names with asterisks in the verbatim (original verbatim preserved in report)</li></ul></td></tr><tr><td valign="top">Email Addresses</td><td valign="top"><p>Detects email addresses in responses.</p><ul><li><strong>(Detect hidden):</strong> flags responses in the report</li><li><strong>Redact:</strong> replaces detected email addresses with asterisks in the verbatim (original verbatim preserved in report)</li></ul></td></tr></tbody></table>

#### Additional Settings

<table><thead><tr><th width="238.177734375" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Custom flags to detect</td><td valign="top"><p>Create custom lists of terms or phrases to flag in responses. Multiple lists can be created and activated simultaneously. This option replaces both "Additional Matches to Flag" and "Additional Profanity" from the Verbatim Quality Report.<br><br>To create a custom flag list:</p><ol><li>Check <strong>Custom flags to detect</strong></li><li><strong>Click the + icon</strong> to add a new list</li><li><strong>Enter a list name</strong> and add items (one per line)</li><li>Select whether to <strong>Detect </strong><em><strong>or</strong></em><strong> Redact</strong> flagged items</li><li><strong>Repeat</strong> to create additional lists as needed</li></ol></td></tr><tr><td valign="top">Responses To Skip For Analysis</td><td valign="top">Create lists of responses to exclude from analysis. These responses will not be processed or counted.</td></tr><tr><td valign="top">Add codes to detected responses</td><td valign="top">When selected, automatically adds codes to responses that are flagged by the analysis. These codes can be viewed and managed in Ascribe Coder.</td></tr><tr><td valign="top">Include all detection columns in report</td><td valign="top">Shows every available detection column in the Excel report output. Useful when the report is consumed by downstream systems.</td></tr><tr><td valign="top">Put redacted verbatim in a new field</td><td valign="top"><p>When redaction is enabled, copies the redacted version of the verbatim to a specified field. Select from:</p><ul><li>Notes</li><li>Translation</li><li>Transcription</li></ul><p>The original verbatim remains unchanged in the primary verbatim field.</p></td></tr></tbody></table>

### Output and Reporting

An Excel report is generated after the run is complete. The report has details of which responses were flagged for each selected criteria.

* **First tab**: Details of flagged responses with detection reasons
* **Second tab**: Respondents with multiple issues
* **Third tab**: Summary counts of issues found
