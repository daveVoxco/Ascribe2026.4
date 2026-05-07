---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/ascribe-coder/codebooks/use-keyboard-to-edit-codebook
---

# Use Keyboard to Edit Codebook

Ascribe Coder provides the ability to edit the codebook using the keyboard only. This option is activated through the Toggle Focus option in the right-click menus of the Codebook Pane. &#x20;

You can automatically activate Toggle Focus through the Set Focus on First Code setting in the [When Starting tab](../responses-settings.md#when-starting) of Responses Settings or you can right-click a code in the codebook and select Toggle Focus. This code becomes the “focus code.”  Here is how it works:

The focus code is indicated by a green background.  When there is a focus code, it reacts to the up/down arrow keys by moving up or down in the codebook. If there is no focus code, the up/down arrows have their normal browser effect of scrolling the codebook up or down (if you have clicked in the codebook area).

The focus code exists only in the “normal” view of the codebook. There are two other views possible: Codes Only and the codes displayed by the Find All option in the search dialog. There is never a focus code in these views.

You can introduce a focus code a) the option in the When Starting tab of Responses Settings, b) right-click on a code and select Toggle Focus, or c) ctrl-click on a code. If you do this on the current focus code, the focus goes away.  Once you have a focus code, it will generally stay on the display until you toggle it off.

When there is a focus code, these keys have effect:

* **Enter:** opens the Properties dialog for the code.  Clicking the Cancel button in the dialog does not move the focus code.  Clicking the OK button or pressing Enter in the Properties dialog updates the code and moves the focus code down.
* **Insert:** inserts a new code below the current code or into the current net, moves the focus to the new code, and opens the Properties dialog for the new code.
* **Delete:** deletes the focus code (if it is eligible for deletion) and moves the focus to the following code.

The focus code behaves the same way in both locked and unlocked codebooks, and persists across the lock/unlock operation.

Use of the focus code in direct edit mode is not recommended. The problem is the battle for keystroke focus. It will go to the field that contains the edit caret if there is one, or otherwise to the focus code. While that works, you have to be very attentive the presence or absence of the input caret.
