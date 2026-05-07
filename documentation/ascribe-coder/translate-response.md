---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/ascribe-coder/translate-response
---

# Translate Response

The Translate dialog provides a way to translate responses. ([There are also two other ways to translate responses with Ascribe Coder.](translate-response.md#other-ways-to-translate)) In the Translate dialog, you tell Ascribe what you are translating, and you specify the From and To languages. With this method, Ascribe can give you and automatic translation using the New translation button (there is a  transaction cost each time you click the button).  It can also suggest a "Previous translation" (at no cost!) if you have already entered a translation for the From and To languages.  Finally, since it knows what you are translating (Verbatim etc) it can and does automatically apply that translation to all duplicates of that field that have no existing translation.

You can also enter a translation in the New Translation text box; you do not have to use the auto-translate option.

If you are translating more than one response using the Translate dialog, you will want to set the Response Settings as follows: on the Responses tab, check Display in responses/translation AND Edit Translation.  Now when you click in the editable translation field of a response, the dialog updates to show the stuff for that response. You can leave the dialog open and move from one response to another by just clicking in the translation portion of the desired response.

Here are the Translate dialog options:

<table><thead><tr><th width="235.33331298828125" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Translate</td><td valign="top">Select which response field you want to translate. The options are: Verbatim, Transcription and Notes.</td></tr><tr><td valign="top">From</td><td valign="top">This field is used to display the source language of the response. You must select the source language before anything can be translated.</td></tr><tr><td valign="top">To</td><td valign="top">This field is used to display the language of the translation. You must select the target language before anything can be translated. This selection will stick from session to session, so you may only have to select it one time if you always translate to the same language.</td></tr><tr><td valign="top">Translating</td><td valign="top">Displays the text being translated.</td></tr><tr><td valign="top">Previous Translation</td><td valign="top">This field is used in conjunction with the translation library on each account. The translation library stores an entry for each verbatim text and its corresponding translation, Source Language, and Target Language. If the exact verbatim appears again in a question or study, this field displays the translation from the library, and you can decide to use that suggestion by clicking the Apply button.</td></tr><tr><td valign="top">New Translation</td><td valign="top">Clicking this button displays the suggested translation; you can decide to use that suggestion by clicking the Apply button or enter a different translation. (Note: Upon clicking the New Translation button you will be charged transactions according to your account.)</td></tr><tr><td valign="top">Translate Back</td><td valign="top">This field can be used to check the translation in the New Translation field. Clicking this button translates the translation back to the source language. (Note: Upon clicking the Translate Back button, you will be charged transactions according to your account.)</td></tr></tbody></table>

## Other Ways to Translate

Ascribe Coder provides two other ways to translate:

* Right-click response/Edit.  Enter translation.
* Turn on these settings in the Response Settings dialog: in the Responses tab, check Display in responses/translation AND Edit Translation. Type translations directly in responses.

These methods have very different behavior than the Translate dialog. In these methods, Ascribe has no knowledge of the source and target languages. It does not know what field you are translating (Verbatim, Transcription, Notes). It also does not know what languages you are translating to and from. Hence it cannot do anything more than simply store the translation you provide in the response. It does not save the translation as a "Previous translation", nor does it apply the translation to any duplicate responses.
