---
description: Use shared, account-level codebooks across multiple projects.
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/ascribe-coder/codebooks/account-codebooks
---

# Account Codebooks

_Navigate: Supervisor/Account Codebooks_

The Account Codebooks page displays a list of codebooks that have been designated as account codebooks. The purpose of account codebooks is to reuse them for sharing or copying to the other questions.

The codebooks will not be deleted if even no question references them.

You can designate a codebook as an account codebook by accessing the Codebook Properties dialog from Ascribe Coder or the Copy/Share Manager. The codebook must have an ID in order to be designated as an account codebook. Each codebook ID must be unique.

If you no longer want a codebook to be an account codebook, right-click the codebook and select Edit to open the Codebook Properties dialog. Click the check box next to Account Codebook to change the designation. You can also access the Codebook Properties dialog from Ascribe Coder or the Copy/Share Manager to change the designation.

When you restore a study that had an account codebook, the account codebook designation is not restored.

The Account Codebooks page has these columns (you can choose the columns displayed by selecting [Choose Columns](../../get-started/customization-features/choose-columns.md) from the right-click menu):

<table><thead><tr><th width="247.33331298828125" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">ID</td><td valign="top">The codebook ID.</td></tr><tr><td valign="top">Description</td><td valign="top">An optional description of the codebook.</td></tr><tr><td valign="top">Notes</td><td valign="top">An optional field which lists additional information about the codebook.</td></tr><tr><td valign="top">Length</td><td valign="top">The number of codes and nets in the codebook.</td></tr><tr><td valign="top">Shared Questions</td><td valign="top">The number of questions that share this codebook.</td></tr><tr><td valign="top">No Duplicate OutputID's</td><td valign="top">If there is a dot in this column, duplicate outputID's are not allowed in the codebook. If this column is empty, duplicate outputID's are allowed. For more information, see No Duplicate OutputID's on the Codebook Properties dialog.</td></tr><tr><td valign="top">Master Codebook</td><td valign="top">Indicates if the codebook is a <a href="account-codebooks.md#minitocbookmark2">Master Codebook</a>.</td></tr><tr><td valign="top">Spread Between Codes</td><td valign="top">This field displays the value entered in the Spread Between Codes field on the Codebook Properties dialog.</td></tr></tbody></table>

The right-click menu options for this page are:

<table><thead><tr><th width="198.66668701171875" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Properties</td><td valign="top">Opens the Codebook Properties dialog so you can edit the fields. If you no longer want a codebook to be an account codebook, click the check box next to Account Codebook to change the designation.</td></tr><tr><td valign="top">New</td><td valign="top">Opens the Codebook Properties dialog so you can create a new account codebook.</td></tr><tr><td valign="top">Unshare</td><td valign="top">Unshares the account codebook from other questions.</td></tr></tbody></table>

{% hint style="info" %}
#### Note

**Drop-Down Boxes**

Several columns on this screen display drop-down boxes when left-clicked. A hand icon displays when you hover over these fields. The drop-down boxes can open with a single click or a double click. Choose the method you prefer in [User Options](../../get-started/customization-features/user-options.md).

To close the drop-down box, click Close, left-click twice in the box, or click once anywhere on the other columns.
{% endhint %}

### Master Codebooks <a href="#minitocbookmark2" id="minitocbookmark2"></a>

Master codebooks are intended to assist in administration of codebooks as resources to be used across multiple projects. A master codebook can be used to propagate changes to the codes contained in it to other codebooks. It is intended to assist companies that have administrative rules for the construction of codebooks, and for the properties of the codes.

Master codebooks may contain only codes. No nets are permitted in master codebooks.

A codebook can be designated as a master codebook by editing its properties. A master codebook is automatically an account codebook, meaning it will appear in the list of account codebooks and will not be deleted even if it is not used by any question.

A master codebook can be edited in Ascribe in the same fashion as any other codebook.

The Account Codebooks page has a column for indicating whether the account codebook is a master codebook.

If a codebook contains any nets, or any linked codes (see below), it cannot be converted to a master codebook.

If a master codebook contains any codes that are referenced by linked codes, it cannot be changed back to a normal codebook. In other words, the master codebook property of a codebook cannot be set to false if it contains any codes that are referenced by linked codes.

Typically a master codebook will be used to create and maintain account codebooks. These account codebooks can then be used in individual projects.

If the account codebook containing linked codes is shared with a question in a project, the linkages are maintained, and updates to the Master codes will propagate to the codebooks in the project.

If the account codebook is copied to a question in a project, the linkages are removed. Changes to the master codebook will not affect the codes in the project.

While changes to master codes will always propagate to any codes linked to them, only Ascribe Coder and Dual Codebooks are designed to properly handle the editing of linked codes. You should use only these pages when working with codebooks containing linked codes.

#### Master Codes and Linked Codes <a href="#minitocbookmark3" id="minitocbookmark3"></a>

Codes in a master codebook are called master codes.

A code that is linked to a master code is called a linked code. You create linked codes only through the Dual Codebooks page. Display the master codebook on the left side of the page and the target codebook on the right side. Copy the appropriate master codes to the target codebook.

In Ascribe Coder and Dual Codebooks, a linked code is identified by italic text.

A linked code can be deleted from a codebook, and can be moved within the codebook, but it cannot be edited. Linked codes cannot be modified by editing their properties, nor by operations on selected codes such as renumber, color, or case.

If the properties of a master code are changed, the changes propagate to all linked codes that reference the master code, just as if the user had made the same change in each of the linked codes.

If a linked code is copied to another codebook, the newly created code is NOT linked to the master code.

If a master codebook is copied via the Copy/Share Manager or Copy/Share From, the codes in the newly created codebook are NOT linked to the master codes in the master codebook. Similarly, if a codebook containing linked codes is copied, the codes in the newly created codebook are not linked to the master codes.

#### Linked Codes and the No Duplicate Output ID’s setting <a href="#minitocbookmark4" id="minitocbookmark4"></a>

Because the value of the output ID in a master code will propagate to any number of linked codes in any number of codebooks, the output ID has special treatment.

A codebook may be designated as having no duplicate output ID’s using its No Duplicate Output ID’s property. If the output ID of a master code were to propagate into a linked code in a codebook with No Duplicate Output ID’s, duplicate ID’s may be created in that codebook.

To deal with this problem these rules are followed:

* The output ID of a linked code in a codebook with No Duplicate Output ID’s = true is always null. (The output IDs are blank.)
* The output ID of a linked code in a codebook with No Duplicate Output ID’s = false is the output ID of its master code.
* If the No Duplicate Output ID’s property of a codebook is changed, the output ID’s of all linked codes it contains are updated in accordance with rules 1 and 2 above.

So what to do if the user wants both linked codes and unique output ID's? They must use the No Duplicates = false, and check whether there are duplicates using the codebook tools dialog, renumbering the codebook if necessary. The linked codes will always have the output ID's as assigned in the master codebook. Other codes will be renumbered, skipping the output ID's assigned to the linked codes.

If a user wants complete control over the output ID's, then the user should follow this methodology: Use linked codes only in account codebooks that are then copied to projects as needed. Once copied, the linkage is broken, and the codes can be renumbered as desired (and the No Duplicates = true option set if desired).
