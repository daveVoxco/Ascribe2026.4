---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/data-management/study-archive-save-and-restore-xml-specification
---

# Study Archive (Save and Restore) XML Specification

Ascribe uses XML to save and restore studies. This section describes the contents of the XML files. It will help you create software that will read and write Ascribe studies, so that you can integrate Ascribe with other software components in your company.

## Structure

The XML schema used by Ascribe is "tag-centric", meaning that tags are generally used for data elements, as opposed to attributes. This results in XML files that are lengthy but highly compressible. Normally the XML document is stored in a zip file to reduce storage space and network transfer times. The use of a zip file is optional unless media files accompany the XML document.

This section does not contain a full example of an Ascribe XML file. You may easily obtain examples by saving one or more studies in Ascribe and inspecting the resulting XML file.

Ascribe does check the syntax of the XML document when restoring a study, but does not perform extensive semantic checks. For example, it is possible to create codebooks with scrambled indentation levels. You must ensure that the documents you generate are semantically correct.

## XML Document Outline

This section describes the general form of the XML document, listing those tags that serve as containers for other tags.

Each document begins with the tag:

\<?XML version="1.0" encoding="utf-8" standalone="yes" ?>

This indicates that the document uses XML version 1.0, and utf-8 encoding. You may also use utf-16 encoding. If you plan to support multiple languages, we recommend that you write your files in utf-16 encoding.

The following tags serve as containers for other tags, and define the overall structure of the XML document:

<table><thead><tr><th width="286" valign="top">Tag</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">&#x3C;Studies></td><td valign="top">Container for &#x3C;Study> tags</td></tr><tr><td valign="top">&#x3C;Study></td><td valign="top">Defines a study</td></tr><tr><td valign="top">&#x3C; CodeBooks></td><td valign="top">Container for &#x3C; CodeBook> tags</td></tr><tr><td valign="top">&#x3C; CodeBook></td><td valign="top">Defines a codebook</td></tr><tr><td valign="top">&#x3C; CodeBookCode></td><td valign="top">Defines a code in a codebook</td></tr><tr><td valign="top">&#x3C;Questions></td><td valign="top">Container for &#x3C;Question> tags</td></tr><tr><td valign="top">&#x3C;Question></td><td valign="top">Defines a question</td></tr><tr><td valign="top">&#x3C;Responses></td><td valign="top">Container for &#x3C;Response> tags</td></tr><tr><td valign="top">&#x3C;Response></td><td valign="top">Defines a response</td></tr><tr><td valign="top">&#x3C; ResponseCodes></td><td valign="top">Container for &#x3C; ResponseCode> tags</td></tr><tr><td valign="top">&#x3C; ResponseCode></td><td valign="top">Defines a code applied to a response</td></tr><tr><td valign="top">&#x3C; ResponseQualityCodes></td><td valign="top">Container for &#x3C; ResponseQualityCode> tags</td></tr><tr><td valign="top">&#x3C; ResponseQualityCode></td><td valign="top">Defines a quality code applied to a response</td></tr><tr><td valign="top">&#x3C; QuestionRelationships></td><td valign="top">Container for &#x3C; QuestionRelationship> tags</td></tr><tr><td valign="top">&#x3C; QuestionRelationship></td><td valign="top">Defines a relationship between two questions</td></tr></tbody></table>

## Tag Descriptions

The table below lists each of the tags required for reading and writing Ascribe studies. For the Text data type, a maximum length in characters may be specified in parentheses. Textual data must of course conform to standard XML representations (e.g. & quot; for a double quotation character). Integer data types allow values for 32 bit signed integers. Remember that XML tag names are case sensitive.

<table><thead><tr><th width="200" valign="top">Tag</th><th width="147" valign="top">Parent Tag</th><th width="164.6666259765625" valign="top">Data Type</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Studies</td><td valign="top">None</td><td valign="top">Container tag</td><td valign="top">Required. This is the root tag of the document.</td></tr><tr><td valign="top">Study</td><td valign="top">Studies</td><td valign="top">Container tag</td><td valign="top">Required. The Study tag defines a study. Exactly one Study tag must be present in the document. The schema is designed to allow multiple Study tags, but this usage is not presently supported by Ascribe.</td></tr><tr><td valign="top">StudyIDClient</td><td valign="top">Study</td><td valign="top">Text(20)</td><td valign="top"><p>Required. This is the requested short identifier for the study. This text appears in Ascribe as the Study ID.</p><p>When an XML document is sent to Ascribe via the FTP site a study restore will be performed if a study with this ID does not exist. If a study with this ID does exist, the file sent will be merged with the existing study.</p><p>When restoring or merging a study via the Ascribe web site, this tag is ignored except when the study is restored as Original. In other cases the user provides the desired Study ID when submitting the file.</p></td></tr><tr><td valign="top">StudyName</td><td valign="top">Study</td><td valign="top">Text(50)</td><td valign="top">Optional. The name of the study.</td></tr><tr><td valign="top">StudyDescription</td><td valign="top">Study</td><td valign="top">Text</td><td valign="top">Optional. A description of the study.</td></tr><tr><td valign="top">StudyCreateDate</td><td valign="top">Study</td><td valign="top">DateTime</td><td valign="top">Optional. The date and time that the study was created.</td></tr><tr><td valign="top">StudyHelp</td><td valign="top">Study</td><td valign="top">Text</td><td valign="top">Optional. Help text to provide to coders of this study.</td></tr><tr><td valign="top">StudyFileFormat</td><td valign="top">Study</td><td valign="top">Integer</td><td valign="top"><p>Optional. Specifies the file format for column binary output of the file. If present, must be one of the following values:</p><p>1: Binary<br>2: ASCII</p></td></tr><tr><td valign="top">StudyFileEncoding</td><td valign="top">Study</td><td valign="top">Integer</td><td valign="top"><p>Optional. Specifies the internal encoding used in column binary output. Corresponds to the Layout setting in the Ascribe study. If present, must be one of the following values:</p><p>1: Punch<br>2: Numeric<br>3: Use question setting<br>4: Punch using question column offset</p></td></tr><tr><td valign="top">StudyCardColumns</td><td valign="top">Study</td><td valign="top">Integer</td><td valign="top">Optional. Specifies the number of columns used in column binary output.</td></tr><tr><td valign="top">StudyCardNumberColumn</td><td valign="top">Study</td><td valign="top">Integer</td><td valign="top">Optional. Specifies the column where the card number starts in column binary output.</td></tr><tr><td valign="top">StudyCardNumberColumns</td><td valign="top">Study</td><td valign="top">Integer</td><td valign="top">Optional. Specifies the number of columns occupied by the card number in column binary output.</td></tr><tr><td valign="top">StudyRespondentIDColumn</td><td valign="top">Study</td><td valign="top">Integer</td><td valign="top">Optional. Specifies the column where the respondent ID starts in column binary output.</td></tr><tr><td valign="top">StudyRespondentIDColumns</td><td valign="top">Study</td><td valign="top">Integer</td><td valign="top">Optional. Specifies the number of columns occupied by the respondent ID in column binary output.</td></tr><tr><td valign="top">CodeBooks</td><td valign="top">Study</td><td valign="top">Container tag</td><td valign="top">Required. Container for codebooks for the enclosing study.</td></tr><tr><td valign="top">CodeBook</td><td valign="top">CodeBooks</td><td valign="top">Container tag</td><td valign="top">The CodeBook tag defines a codebook for the study. One CodeBook tag must be present for each distinct codebook in the study. Codebooks may be shared among questions, so the total number of codebooks may be less than the number of questions.</td></tr><tr><td valign="top">CodeBookKey</td><td valign="top">CodeBook</td><td valign="top">Integer</td><td valign="top">Required. The value contained by this tag is used within a Question tag to reference the codebook for the question. The value of the integer is arbitrary, but it must be unique among all codebooks in the XML document. Note that there is no requirement for the value to be unique across XML documents. The simplest scheme for generating CodeBookKey values is to use a counter starting at 1 and incrementing for each codebook.</td></tr><tr><td valign="top">CodeBookDescription</td><td valign="top">CodeBook</td><td valign="top">Text(200)</td><td valign="top">Optional. A description of the codebook.</td></tr><tr><td valign="top">CodeBookNoDuplicates</td><td valign="top">CodeBook</td><td valign="top">Boolean</td><td valign="top"><p>Optional. Specifies the setting of the No Duplicate OutputID's value for the codebook. If present, the value must be one of the following:</p><p>True: The No Duplicate OutputID's option is set<br>False: The No Duplicate OutputID's option is not set</p><p>If omitted, the default value is False.</p></td></tr><tr><td valign="top">CodeBookIncrement</td><td valign="top">CodeBook</td><td valign="top">Integer</td><td valign="top">Optional. Specifies the value of the Increment setting for the codebook. This setting is used to generate suggested OutputID values when a new code is added to the codebook.</td></tr><tr><td valign="top">CodeBookGuid</td><td valign="top">CodeBook</td><td valign="top">GUID</td><td valign="top"><p>Optional for study restore operations. Required for study merge operations. This GUID uniquely identifies the codebook.</p><p>This is a critical value if you are creating XML files that you want to use for study merge operations. Understand that codebooks in Ascribe are not owned by specific studies. Codebooks can be shared across studies. This GUID provides a way for you to specify a codebook in a study on which you intend to perform later merge operations.</p><p>The value of this GUID must be the same for a given codebook in each file you submit for a study merge.</p></td></tr><tr><td valign="top">CodeBookCodes</td><td valign="top">CodeBook</td><td valign="top">Container tag</td><td valign="top">Optional. Contains the codes in the codebook. While each question must have a codebook, the codebook need not contain any codes.</td></tr><tr><td valign="top">CodeBookCode</td><td valign="top">CodeBookCodes</td><td valign="top">Container tag</td><td valign="top">Optional. Defines a code in the codebook.</td></tr><tr><td valign="top">CBCKey</td><td valign="top">CodeBookCode</td><td valign="top">Integer</td><td valign="top">Required. The value contained by this tag is used within a ResponseCode tag to reference the code applied to the response. The value of the integer is arbitrary, but it must be unique among all CodeBookCode tags in the XML document (not just among codes in the containing codebook). Note that there is no requirement for the value to be unique across XML documents. The simplest scheme for generating CBCKey values is to use a counter starting at 1 and incrementing for each code.</td></tr><tr><td valign="top">CBCOrdinal</td><td valign="top">CodeBookCode</td><td valign="top">Integer</td><td valign="top">Required. The ordinal number of the code, which defines its sort order in the codebook. You should use the value 1 for the first code in the codebook, and increment this value for each successive code. Note that the order of codes in the codebook is determined by this value, not by the location of the CodeBookCode tag in the XML document.</td></tr><tr><td valign="top">CBCDepth</td><td valign="top">CodeBookCode</td><td valign="top">Integer</td><td valign="top">Required. The indentation depth of the code. This value should be 1 for a top level code, 2 for a net, 3 for a sub-net, and so on.</td></tr><tr><td valign="top">CBCChildren</td><td valign="top">CodeBookCode</td><td valign="top">Integer</td><td valign="top"><p>Required. The number of direct children of this code or net. The value should be 0 for codes, and non-zero for nets. Note that this is the number of direct children of the net, not the total number of descendents, i.e. children, but not grandchildren.</p><p>It is very important that all nets have a non-zero value for CBCChildren, and that all leaf codes have a zero value.</p></td></tr><tr><td valign="top">CBCOutputID</td><td valign="top">CodeBookCode</td><td valign="top">Text(24)</td><td valign="top">Optional. The output value of the code. This is the value that should be written to a data file for this code when downloading coding results.</td></tr><tr><td valign="top">CBCInputID</td><td valign="top">CodeBookCode</td><td valign="top">Text(24)</td><td valign="top">Optional. The input value of this code. This is the value used for this code when uploading responses to Ascribe. It is typically used only for closed end data.</td></tr><tr><td valign="top">CBCDescription</td><td valign="top">CodeBookCode</td><td valign="top">Text(1000)</td><td valign="top">Required. The description of the code. This is the text that appears for the code in the codebook.</td></tr><tr><td valign="top">CBCRegExp</td><td valign="top">CodeBookCode</td><td valign="top">Text(800)</td><td valign="top">Optional. The regular expression used for pattern matching during coding.</td></tr><tr><td valign="top">CBCHover</td><td valign="top">CodeBookCode</td><td valign="top">Text(400)</td><td valign="top">Optional. Help to display to coder when hovering over the code with the mouse.</td></tr><tr><td valign="top">CBCHelp</td><td valign="top">CodeBookCode</td><td valign="top">Text(1000)</td><td valign="top">Optional. Help to display to coder in popup window.</td></tr><tr><td valign="top">CBCTextColor</td><td valign="top">CodeBookCode</td><td valign="top">Text(7)</td><td valign="top">Optional. Foreground text color of the code to display to coders. This string is of the form:<br>#RRGGBB<br>where RR, GG, and BB are hex values for the red, green, and blue values to display. If not present, the default is #000000 (black).</td></tr><tr><td valign="top">Questions</td><td valign="top">Study</td><td valign="top">Container tag</td><td valign="top">Optional. Container for the questions in the study.</td></tr><tr><td valign="top">Question</td><td valign="top">Questions</td><td valign="top">Container tag</td><td valign="top">Defines a question.</td></tr><tr><td valign="top">QuestionKey</td><td valign="top">Question</td><td valign="top">Integer</td><td valign="top">Required. The value contained by this tag is used within &#x3C;QuestionRelationshipFrom> and &#x3C;QuestionRelationshipTo> tags to reference the question. The value of the integer is arbitrary, but it must be unique among all Question tags in the XML document. Note that there is no requirement for the value to be unique across XML documents. The simplest scheme for generating QuestionKey values is to use a counter starting at 1 and incrementing for each question.</td></tr><tr><td valign="top">QuestionID</td><td valign="top">Question</td><td valign="top">Text(50)</td><td valign="top">Optional. The short identifier for the question, typically the question number.</td></tr><tr><td valign="top">QuestionText</td><td valign="top">Question</td><td valign="top">Text</td><td valign="top">Required. The text of the question.</td></tr><tr><td valign="top">QuestionHelp</td><td valign="top">Question</td><td valign="top">Text</td><td valign="top">Optional. Help about this question to display to coders.</td></tr><tr><td valign="top">QuestionCard</td><td valign="top">Question</td><td valign="top">Integer</td><td valign="top">Optional. The card number of the question. Used for column binary output.</td></tr><tr><td valign="top">QuestionColumn</td><td valign="top">Question</td><td valign="top">Integer</td><td valign="top">Optional. The starting column position for codes. Used for column binary output.</td></tr><tr><td valign="top">QuestionColumns</td><td valign="top">Question</td><td valign="top">Integer</td><td valign="top">Optional. The number of columns used for each code written in column binary output when using Numeric format ( StudyFileEncoding = 2).</td></tr><tr><td valign="top">QuestionLabel</td><td valign="top">Question</td><td valign="top">Text(25)</td><td valign="top">Optional. Short identifier for question, used to identify the question in reports.</td></tr><tr><td valign="top">QuestionType</td><td valign="top">Question</td><td valign="top">Integer</td><td valign="top"><p>Optional. Specifies the type of the question. When present, must be one of the following values:</p><p>0: Open<br>1: Closed<br>2: Other specify<br>3: Value</p></td></tr><tr><td valign="top">QuestionCodeBookKey</td><td valign="top">Question</td><td valign="top">Integer</td><td valign="top"><p>Required. Specifies the codebook for this question. Must match one of the values of a CodeBookKey tag in the document.</p><p>More than one question may reference the same codebook. This indicates that the codebook is shared by these questions.</p></td></tr><tr><td valign="top">QuestionFileEncoding</td><td valign="top">Question</td><td valign="top">Integer</td><td valign="top"><p>Optional. Specifies the internal encoding used in column binary output. Corresponds to the Layout setting in the Ascribe study. If present, must be one of the following values (note that the value 3 is illegal):</p><p>1: Punch<br>2: Numeric<br>4: Punch using column offset</p></td></tr><tr><td valign="top">QuestionMaxCodes</td><td valign="top">Question</td><td valign="top">Integer</td><td valign="top">Optional. Specifies the maximum number of codes to be output in result files for this question. If not present, or if the value is 0, the number of codes is unlimited.</td></tr><tr><td valign="top">QuestionCodingSource</td><td valign="top">Question</td><td valign="top">Integer</td><td valign="top"><p>Optional. Specifies the text used in coding operations. This is the text that coders look at to code. Allowed values are:</p><p>0: Verbatim (default if not present)<br>1: Transcription<br>2: Translation</p></td></tr><tr><td valign="top">QuestionOrdinal</td><td valign="top">Question</td><td valign="top">Integer</td><td valign="top">Optional. Used for sorting questions when displayed to the user in a list. Questions in lists are sorted first by this value, then by the QuestionID. If not present the default value is zero.</td></tr><tr><td valign="top">QuestionCode</td><td valign="top">Question</td><td valign="top">Boolean</td><td valign="top">Optional. Specifies whether this question is to be coded. If false, this question will not be present in lists of questions to code presented to coders. If not present the default value is true.</td></tr><tr><td valign="top">QuestionTranscribe</td><td valign="top">Question</td><td valign="top">Boolean</td><td valign="top">Optional. Specifies whether this question is to be transcribed. If false, this question will not be present in lists of questions to be transcribed, nor will it be present in lists of responses to transcribe for the question. If not present the default value is false.</td></tr><tr><td valign="top">QuestionTranslate</td><td valign="top">Question</td><td valign="top">Boolean</td><td valign="top">Optional. Specifies whether this question is to be translated. If false, this question will not be present in lists of questions to be translated, nor will it be present in lists of responses to translate for the question. If not present the default value is false.</td></tr><tr><td valign="top">QuestionCrosstab</td><td valign="top">Question</td><td valign="top">Boolean</td><td valign="top">Optional. Specifies whether this question should appear in the crosstab report. If not present the default value is false.</td></tr><tr><td valign="top">Responses</td><td valign="top">Question</td><td valign="top">Container tag</td><td valign="top">Optional. Container for responses to this question.</td></tr><tr><td valign="top">Response</td><td valign="top">Responses</td><td valign="top">Container tag</td><td valign="top">Optional. Defines a response.</td></tr><tr><td valign="top">DROVerbatim</td><td valign="top">Response</td><td valign="top">Text(3000)</td><td valign="top">Required. The verbatim text.</td></tr><tr><td valign="top">DRORespondent</td><td valign="top">Response</td><td valign="top">Text(20)</td><td valign="top">Required. The identifier for this respondent. Must be unique among responses for the containing Question.</td></tr><tr><td valign="top">DROTranscription</td><td valign="top">Response</td><td valign="top">Text</td><td valign="top">Optional. A transcription of the verbatim text.</td></tr><tr><td valign="top">DROTranslation</td><td valign="top">Response</td><td valign="top">Text</td><td valign="top">Optional. A translation of the verbatim or transcription text.</td></tr><tr><td valign="top">DRONotes</td><td valign="top">Response</td><td valign="top">Text</td><td valign="top">Optional. Notes for this response.</td></tr><tr><td valign="top">DROMedia</td><td valign="top">Response</td><td valign="top">Integer</td><td valign="top">Optional. Specifies the media type of the response. See Media types below.</td></tr><tr><td valign="top">ResponseCodes</td><td valign="top">Response</td><td valign="top">Container tag</td><td valign="top">Optional. Container for the codes applied to this response.</td></tr><tr><td valign="top">ResponseCode</td><td valign="top">ResponseCodes</td><td valign="top">Container tag</td><td valign="top">Optional. Defines a code applied to the containing Response.</td></tr><tr><td valign="top">DCCBCKey</td><td valign="top">ResponseCode</td><td valign="top">Integer</td><td valign="top">Required. Specifies the code applied. Must match one of the values of a CBCKey tag in the document.</td></tr><tr><td valign="top">ResponseQualityCodes</td><td valign="top">Response</td><td valign="top">Container tag</td><td valign="top">Optional. Container for the quality codes applied to this response.</td></tr><tr><td valign="top">ResponseQualityCode</td><td valign="top">ResponseQualityCodes</td><td valign="top">Container tag</td><td valign="top">Optional. Defines a quality code applied to the containing Response.</td></tr><tr><td valign="top">DQCCBCKey</td><td valign="top">ResponseQualityCode</td><td valign="top">Integer</td><td valign="top">Required. Specifies the quality code applied. Must match one of the values of a CBCKey tag in the document. The referenced code must be in the codebook for this question.</td></tr><tr><td valign="top">QuestionRelationships</td><td valign="top">Study</td><td valign="top">Container tag</td><td valign="top">Optional. Container for relationships between questions.</td></tr><tr><td valign="top">QuestionRelationship</td><td valign="top">QuestionRelationships</td><td valign="top">Container tag</td><td valign="top">Optional. Defines a relationship between questions.</td></tr><tr><td valign="top">QuestionRelationshipFrom</td><td valign="top">QuestionRelationship</td><td valign="top">Integer</td><td valign="top"><p>Required. References question A in the relationship "Question A is related to Question B".</p><p>Must match one of the values of a QuestionKey tag in the document.</p></td></tr><tr><td valign="top">QuestionRelationshipTo</td><td valign="top">QuestionRelationship</td><td valign="top">Integer</td><td valign="top"><p>Required. References question B in the relationship "Question A is related to Question B".</p><p>Must match one of the values of a QuestionKey tag in the document.</p></td></tr></tbody></table>

### Data Types

The following data types are used in the Ascribe study archive document:

<table><thead><tr><th width="233.3333740234375" valign="top">Data Type</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Container Tag</td><td valign="top">This is not actually a data type, but rather a type of tag used in the document. A container tag contains other tags, and do not themselves contain values.</td></tr><tr><td valign="top">Integer</td><td valign="top">A 32 bit signed integer value. The value in the document is a text representation of the integer in base 10. The range of this data type is -2147483648 to 2147483647, although some fields restrict the allowed value to certain ranges.</td></tr><tr><td valign="top">Text(max characters)</td><td valign="top">A field containing UNICODE characters, up to max characters in length. Zero length strings are permitted unless otherwise specified. Omitting the tag is equivalent to specifying a zero length string value. The value must conform to XML requirements for text values (i.e. XML escaping of reserved characters is required).</td></tr><tr><td valign="top">Text</td><td valign="top">A field containing UNICODE characters. Any number of characters may be specified. The value must conform to XML requirements for text values (i.e. XML escaping of reserved characters is required).</td></tr><tr><td valign="top">Boolean</td><td valign="top">The text True or False</td></tr><tr><td valign="top">DateTime</td><td valign="top"><p>A datetime string conforming to the XML standard:</p><p>YYYY-MM-DDTHH:MM:SS</p><p>The length of the string must be exactly 19 characters.</p><p>YYYY: year (e.g. 2004)<br>MM: month (e.g. 02 = February)<br>DD: day<br>HH: hour (24 hour clock, 02 = 2AM, 18 = 6PM)<br>MM: minute<br>SS: second</p><p>Example:</p><p>2004-05-14T03:09:45</p></td></tr></tbody></table>

## Media Types

The < DROMedia> tag specifies the media type of the response, for example image or sound. The allowed values are:

<table><thead><tr><th width="188" valign="top">DROMedia Value</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">0</td><td valign="top">Numeric text - The contents of the DROVerbatim tag is the response, containing only the digits 0-9, hyphen (-), space, and vertical bar (|) characters.</td></tr><tr><td valign="top">1 (default)</td><td valign="top">Text - The contents of the DROVerbatim tag is the response, containing any text characters.</td></tr><tr><td valign="top">2</td><td valign="top">Image - The contents of the DROVerbatim tag is a file path, relative to the Media folder in the zip file containing the XML document. When rendered in Ascribe, the file will be displayed in an &#x3C; IMG> tag.</td></tr><tr><td valign="top">3</td><td valign="top">Sound - The contents of the DROVerbatim tag is a file path, relative to the Media folder in the zip file containing the XML document. When rendered in Ascribe, the file will played using Windows Media Player.</td></tr></tbody></table>

When constructing XML documents, you need not make a distinction between DROMedia types 0 and 1. When either of these values is supplied, Ascribe inspects the contents of DROVerbatim and assigns a value of 0 or 1 based on the verbatim text. If your verbatims are all text, you can simply omit the DROMedia tag.

When media files accompany the XML document, there are several additional requirements:

* The XML document must be placed in a zip file. The XML document must be at the root level of the zip file. The zip file must contain a folder named "Media", and that folder must contain the media files referenced in each response.
* The DROVerbatim value in the XML document is a file path name, relative to the Media folder in the zip file. The Media folder may contain sub-folders. In this case, the sub-folder name must be included in DROVerbatim.
* The media files provided must be suitable for direct display in the corresponding rendering format. For image files, the file must render properly in an < IMG> tag. For sound files, the files must be directly playable by Windows Media Player.

## Write XML Documents

Creating XML documents containing Ascribe studies is fairly straightforward. You can test the results of your work by restoring test files to Ascribe. You will find during test efforts that the error messages returned by Ascribe for improperly formed documents are not as informational as you could like. We recommend that you build your documents gradually during testing, starting with very simple documents as shown in the examples that follow, and working up to more complete documents.

The file name you assign to your document files is of no consequence to Ascribe. If you wish to zip your study XML documents, you should place only one XML document in each zip file. You may encrypt the zip file if you wish. You must use the encryption password assigned to your Ascribe account. Ascribe always writes study archive XML documents in utf-8 encoding. You may use utf-16 encoding for your documents if you find it more convenient.

## Parse XML Documents

Reading the XML files created by Ascribe requires the use of an XML parser. Ascribe studies can create very lengthy XML files, causing DOM to require a large amount of memory. If you are working in the Microsoft framework, we highly recommend the use of the SAX parser, as opposed to the DOM object. In the .NET environment, use the XmlTextReader object directly to scan the file.

Study files written by Ascribe may contain tags that are not described in this document. Your parser should ignore these tags. Also note that additional tags may be added in future releases of Ascribe. Your parser should not be written to assume that it will not encounter unknown tags.

Study files written from Ascribe are always zipped. If you wish to operate directly on the zipped file, you will need to incorporate an unzipping component in your application.

## Example of a Study with No Questions

This first example shows the minimal XML document. It defines a study with no questions.

```xml
<? xml version="1.0" encoding="utf-8" standalone= "yes" ?>

<Studies>

 <Study>

 < StudyIDClient>XML #1</ StudyIDClient>

 <StudyName>XML example</StudyName>

 <StudyDescription>This is an example for study loading from XML files</StudyDescription>

 <StudyCreateDate>2004-06-04T09:32:11</StudyCreateDate>

 <StudyHelp>This example is described in the " Ascribe™ study archive XML specification" document.</StudyHelp>

 <StudyFileFormat>1</StudyFileFormat>

 <StudyFileEncoding>1</StudyFileEncoding>

 <StudyCardColumns>80</StudyCardColumns>

 <StudyCardNumberColumn>6</StudyCardNumberColumn>

 <StudyCardNumberColumns>2</StudyCardNumberColumns>

 <StudyRespondentIDColumn>1</StudyRespondentIDColumn>

 <StudyRespondentIDColumns>5</StudyRespondentIDColumns>

 <CodeBooks />

 <Questions />

 <QuestionRelationships />

 </Study>

</Studies>
```

## Example of a Study with Three Questions and Coded Responses

This example shows a partially coded study, and also shows the use of quality codes. The Questions Q1 and Q2 share a codebook.

```xml
<?xml version= "1.0" encoding= "utf-8" standalone= "yes"?>

<Studies>

 <Study>

 <StudyGuid>0DE31A2C-54D7-4B6F-8B05-B22DF9C3B6F9</StudyGuid>

 <StudyIDClient>XML #2</StudyIDClient>

 <StudyName>XML example</StudyName>

 <StudyDescription>This is an example for study loading from XML files</StudyDescription>

 <StudyCreateDate>2004-06-04T09:32:11</StudyCreateDate>

 <StudyHelp>This example is described in the "Ascribe™ study archive XML specification" document.</StudyHelp>

 <StudyFileFormat>1</StudyFileFormat>

 <StudyFileEncoding>1</StudyFileEncoding>

 <StudyCardColumns>80</StudyCardColumns>

 <StudyCardNumberColumn>6</StudyCardNumberColumn>

 <StudyCardNumberColumns>2</StudyCardNumberColumns>

 <StudyRespondentIDColumn>1</StudyRespondentIDColumn>

 <StudyRespondentIDColumns>5</StudyRespondentIDColumns>

 <StudyQuestionDateStyle>mdy</StudyQuestionDateStyle>

 <CodeBooks>

 <CodeBook>

 <CodeBookKey>529380</CodeBookKey>

 <CodeBookNoDuplicates>True</CodeBookNoDuplicates>

 <CodeBookIncrement>10</CodeBookIncrement>

 <CodeBookGuid>DDAD0237-9924-46A5-B4C6-62BA83B41D6D</CodeBookGuid>

 <CodeBookCodes>

 <CodeBookCode>

 <CBCKey>42137310</CBCKey>

 <CBCOrdinal>1</CBCOrdinal>

 <CBCDepth>1</CBCDepth>

 <CBCChildren>0</CBCChildren>

 <CBCOutputID>100</CBCOutputID>

 <CBCInputID>10</CBCInputID>

 <CBCDescription>Code1</CBCDescription>

 </CodeBookCode>

 <CodeBookCode>

 <CBCKey>42137311</CBCKey>

 <CBCOrdinal>2</CBCOrdinal>

 <CBCDepth>1</CBCDepth>

 <CBCChildren>2</CBCChildren>

 <CBCOutputID>20</CBCOutputID>

 <CBCInputID>20</CBCInputID>

 <CBCDescription>Net1</CBCDescription>

 </CodeBookCode>

 <CodeBookCode>

 <CBCKey>42137313</CBCKey>

 <CBCOrdinal>3</CBCOrdinal>

 <CBCDepth>2</CBCDepth>

 <CBCChildren>0</CBCChildren>

 <CBCOutputID>110</CBCOutputID>

 <CBCInputID>40</CBCInputID>

 <CBCDescription>SubCode1</CBCDescription>

 </CodeBookCode>

 <CodeBookCode>

 <CBCKey>42137314</CBCKey>

 <CBCOrdinal>4</CBCOrdinal>

 <CBCDepth>2</CBCDepth>

 <CBCChildren>0</CBCChildren>

 <CBCOutputID>120</CBCOutputID>

 <CBCInputID>50</CBCInputID>

 <CBCDescription>SubCode2</CBCDescription>

 </CodeBookCode>

 <CodeBookCode>

 <CBCKey>42137312</CBCKey>

 <CBCOrdinal>5</CBCOrdinal>

 <CBCDepth>1</CBCDepth>

 <CBCChildren>0</CBCChildren>

 <CBCOutputID>130</CBCOutputID>

 <CBCInputID>30</CBCInputID>

 <CBCDescription>Code2</CBCDescription>

 </CodeBookCode>

 </CodeBookCodes>

 </CodeBook>

 <CodeBook>

 <CodeBookKey>529382</CodeBookKey>

 <CodeBookNoDuplicates>True</CodeBookNoDuplicates>

 <CodeBookIncrement>10</CodeBookIncrement>

 <CodeBookGuid>FC563F0F-F5F9-48E9-9D6E-7D4577E68CC6</CodeBookGuid>

 <CodeBookCodes>

 <CodeBookCode>

 <CBCKey>42137315</CBCKey>

 <CBCOrdinal>1</CBCOrdinal>

 <CBCDepth>1</CBCDepth>

 <CBCChildren>0</CBCChildren>

 <CBCOutputID>10</CBCOutputID>

 <CBCInputID>10</CBCInputID>

 <CBCDescription>Code1</CBCDescription>

 </CodeBookCode>

 <CodeBookCode>

 <CBCKey>42137316</CBCKey>

 <CBCOrdinal>2</CBCOrdinal>

 <CBCDepth>1</CBCDepth>

 <CBCChildren>0</CBCChildren>

 <CBCOutputID>20</CBCOutputID>

 <CBCInputID>20</CBCInputID>

 <CBCDescription>Code2</CBCDescription>

 </CodeBookCode>

 </CodeBookCodes>

 </CodeBook>

 </CodeBooks>

 <Questions>

 <Question>

 <QuestionKey>730443</QuestionKey>

 <QuestionID>Q1</QuestionID>

 <QuestionText>This is the question text</QuestionText>

 <QuestionHelp>This is coder help for the question</QuestionHelp>

 <QuestionCard>0</QuestionCard>

 <QuestionColumn>20</QuestionColumn>

 <QuestionColumns>5</QuestionColumns>

 <QuestionLabel>Question1</QuestionLabel>

 <QuestionType>0</QuestionType>

 <QuestionCodeBookKey>529380</QuestionCodeBookKey>

 <QuestionFileEncoding>2</QuestionFileEncoding>

 <QuestionMaxCodes>0</QuestionMaxCodes>

 <Responses>

 <Response>

 <DROVerbatim>Response 1</DROVerbatim>

 <DRORespondent>100</DRORespondent>

 <ResponseCodes>

 <ResponseCode>

 <DCCBCKey>42137310</DCCBCKey>

 </ResponseCode>

 </ResponseCodes>

 </Response>

 <Response>

 <DROVerbatim>Response 2</DROVerbatim>

 <DRORespondent>101</DRORespondent>

 <ResponseCodes>

 <ResponseCode>

 <DCCBCKey>42137314</DCCBCKey>

 </ResponseCode>

 <ResponseCode>

 <DCCBCKey>42137312</DCCBCKey>

 </ResponseCode>

 </ResponseCodes>

 <ResponseQualityCodes>

 <ResponseQualityCode>

 <DQCCBCKey>42137312</DQCCBCKey>

 </ResponseQualityCode>

 <ResponseQualityCode>

 <DQCCBCKey>42137314</DQCCBCKey>

 </ResponseQualityCode>

 </ResponseQualityCodes>

 </Response>

 <Response>

 <DROVerbatim>Response 3</DROVerbatim>

 <DRORespondent>102</DRORespondent>

 <ResponseCodes>

 <ResponseCode>

 <DCCBCKey>42137310</DCCBCKey>

 </ResponseCode>

 </ResponseCodes>

 <ResponseQualityCodes>

 <ResponseQualityCode>

 <DQCCBCKey>42137310</DQCCBCKey>

 </ResponseQualityCode>

 </ResponseQualityCodes>

 </Response>

 </Responses>

 </Question>

 <Question>

 <QuestionKey>730444</QuestionKey>

 <QuestionID>Q2</QuestionID>

 <QuestionText>This is the text for question 2</QuestionText>

 <QuestionHelp>This is help for question 2</QuestionHelp>

 <QuestionCard>0</QuestionCard>

 <QuestionColumn>20</QuestionColumn>

 <QuestionColumns>5</QuestionColumns>

 <QuestionLabel>Question2</QuestionLabel>

 <QuestionType>0</QuestionType>

 <QuestionCodeBookKey>529380</QuestionCodeBookKey>

 <QuestionFileEncoding>2</QuestionFileEncoding>

 <QuestionMaxCodes>0</QuestionMaxCodes>

 <Responses />

 </Question>

 <Question>

 <QuestionKey>730445</QuestionKey>

 <QuestionID>Q3</QuestionID>

 <QuestionText>Text for question 3</QuestionText>

 <QuestionCard>0</QuestionCard>

 <QuestionColumn>20</QuestionColumn>

 <QuestionColumns>5</QuestionColumns>

 <QuestionLabel>Question3</QuestionLabel>

 <QuestionType>0</QuestionType>

 <QuestionCodeBookKey>529382</QuestionCodeBookKey>

 <QuestionFileEncoding>2</QuestionFileEncoding>

 <QuestionMaxCodes>0</QuestionMaxCodes>

 <Responses />

 </Question>

 </Questions>

 <QuestionRelationships>

 <QuestionRelationship>

 <QuestionRelationshipFrom>730444</QuestionRelationshipFrom>

 <QuestionRelationshipTo>730443</QuestionRelationshipTo>

 </QuestionRelationship>

 </QuestionRelationships>

 </Study>

</Studies>
```
