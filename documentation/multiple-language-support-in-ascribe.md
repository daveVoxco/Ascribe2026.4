---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/multiple-language-support-in-ascribe
---

# Multiple Language Support

This document describes how to use Ascribe in multiple languages. Using Ascribe, you can code and manage verbatim responses in most languages. The sole exceptions are right-to-left languages. Ascribe has not been tested for these languages.

The most important point about multiple language support in Ascribe is that Unicode is used throughout the system. This means that all data loaded to Ascribe, and all data downloaded from Ascribe, will be Unicode.

### Loading Data <a href="#minitocbookmark2" id="minitocbookmark2"></a>

Data files loaded to Ascribe must be in either ANSI or Unicode encoding. We recommend ANSI encoding (which is an 8 bit encoding) only for data files that contain characters below character code 128 decimal. Essentially this is the U.S. character set with standard punctuation. For data files containing Asian characters, or western European characters with diacritical marks, you should use Unicode encoding. When an ANSI file is loaded, it is converted to Unicode automatically, using the U.S. codepage (1252). This conversion can scramble characters written in locales other than the U.S.

### Downloading Data <a href="#minitocbookmark3" id="minitocbookmark3"></a>

When downloading data it is always safe to choose Unicode encoding for the downloaded file. This will cause Ascribe to download the data in 16 bit Unicode encoding. Such files can be used on Windows systems as easily as ANSI files.

If your data contains only standard characters in the U.S. character set, you may also safely download files without Unicode encoding. These files will be written in ANSI encoding.

### Configuring Your Computer For Multiple Language Support and Translating Your Account <a href="#minitocbookmark4" id="minitocbookmark4"></a>

See [Translate the Ascribe Interface](site-administration/translate-the-ascribe-interface.md) for more information.
