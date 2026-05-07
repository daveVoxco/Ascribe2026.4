---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/user-administration/contacts
---

# Contacts

An account can restrict users to certain studies through the use of companies and contacts. A company can be an end-client or customer. Once a company is added, then you can add contacts for the company. Contacts can only view the studies assigned to the company. You assign studies to a company in the [Studies Details dialog](https://static.goascribe.com/Help/Study_Details_Dialog.htm#Client). &#x20;

## Toolbar <a href="#minitocbookmark2" id="minitocbookmark2"></a>

The Contacts page is organized with a toolbar and a grid, which lists the contacts. Here are the options on the toolbar:

<table><thead><tr><th width="231.3333740234375" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top"><p><img src="https://static.goascribe.com/Help/add_contact.jpg" alt=""></p><p>Add Contact</p></td><td valign="top">Add a new contact; see <a href="contacts.md#minitocbookmark4">Add New Contact</a> for more information.</td></tr><tr><td valign="top"><p><img src="https://static.goascribe.com/Help/deleted_users.jpg" alt=""></p><p>Deleted Contacts</p></td><td valign="top">Displays a list of deleted users. Right-click a user to restore the user.</td></tr><tr><td valign="top"><p><img src="https://static.goascribe.com/Help/companies.jpg" alt=""></p><p>Add or Edit Companies</p></td><td valign="top">Displays a dialog where you can <a href="contacts.md#minitocbookmark4">add or edit a company</a>.</td></tr></tbody></table>

## Grid <a href="#minitocbookmark3" id="minitocbookmark3"></a>

The [Table Manager](https://static.goascribe.com/Help/Table_Manager.htm) controls what fields are displayed. Options are:

<table><thead><tr><th width="261.3333740234375" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">Company</td><td valign="top">The company is always displayed.</td></tr><tr><td valign="top">User Name</td><td valign="top">ID used for logging in and tracking of activity, if the associate does not have <a href="../get-started/single-sign-on-overview.md">single sign-on</a> (SSO) authentication. If  user has SSO, then the user name is only used for tracking activity.</td></tr><tr><td valign="top">SSO</td><td valign="top">SSO stands for <a href="../get-started/single-sign-on-overview.md">single sign-on</a>. If a user has SSO, then a dot displays in this column.</td></tr><tr><td valign="top">MFA</td><td valign="top">MFA stands for multi-factor authentication.</td></tr><tr><td valign="top">External IDP</td><td valign="top">Displays the external identify provider used with SAML technology; please contact Ascribe Support for more information.</td></tr><tr><td valign="top">Last Name</td><td valign="top">The last name of the associate; this field is not editable if the user has single sign-on credentials.</td></tr><tr><td valign="top">First Name</td><td valign="top">The first name of the associate; this field is not editable if the user has single sign-on credentials.</td></tr><tr><td valign="top">Email Address</td><td valign="top">Used for password reset requests by the user and used for <a href="../get-started/single-sign-on-overview.md">SSO</a> logins. This field is not editable if the user has single sign-on credentials.</td></tr><tr><td valign="top">Last Activity</td><td valign="top">Date of last activity in Ascribe</td></tr><tr><td valign="top">Privilege</td><td valign="top">The privileges assigned to this associate. You can change this by editing the associate.</td></tr></tbody></table>

## Add or Edit New Contact <a href="#minitocbookmark4" id="minitocbookmark4"></a>

On the Contacts page, click the Add button.&#x20;

To modify a contact, right-click a contact and select Edit.

The Properties dialog has these fields:

<table><thead><tr><th width="232" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">User Name</td><td valign="top">The user ID used for login and tracking, if the user does not have <a href="../get-started/single-sign-on-overview.md">single sign-on</a> credentials. If the user has single sign-on credentials, it is used for tracking, and their login is their email address.</td></tr><tr><td valign="top">First Name</td><td valign="top">Self-explanatory</td></tr><tr><td valign="top">Last Name</td><td valign="top">Self-explanatory</td></tr><tr><td valign="top">Email Address</td><td valign="top">Ascribe uses email addresses for password resets and <a href="../get-started/single-sign-on-overview.md">single sign-on</a> identities. If a user has single sign-on credentials, only the user can edit the email address on the User Options page.</td></tr><tr><td valign="top">Company</td><td valign="top">The company to which this contact belongs. You can change the company for a contact by selecting a value in this list. A contact can belong to only one company. Contacts are able to view only those studies that are assigned to the contact's company.</td></tr><tr><td valign="top">Ascribe Coder</td><td valign="top"><p>The privilege level for the contact. If all check boxes are clear, the contact cannot log in.</p><p><strong>Client -</strong> The contact has access to the client area of Ascribe.</p><p><strong>Coder -</strong> The contact only has access to Ascribe Coder and can code verbatims. The contact cannot enter transcriptions or edit or add verbatims.</p><p><strong>Transcriber -</strong> The contact can use <a href="../verbatims/edit-verbatims/edit-responses-ii.md">Edit Responses</a> to add notes, translations, and transcriptions. The contact can edit verbatims, but cannot add or delete responses. The contact can use the <a href="../verbatims/edit-verbatims/edit-respondent-window.md">Edit Respondent Window</a> to add notes, translations, and transcriptions. The contact can edit verbatims, but cannot delete respondents.</p></td></tr><tr><td valign="top">Product</td><td valign="top">Select the privilege Ascribe Illustrator as appropriate.</td></tr></tbody></table>

To delete a contact, right-click the contact and select Delete.&#x20;

You can disable access by a contact without deleting the contact. To do this, right-click the contact, select Edit, and remove any privileges.

## Companies <a href="#minitocbookmark5" id="minitocbookmark5"></a>

To add a company, click the Companies button and then click the Add a New Company button in the dialog. Enter a name in the Properties box and click OK.&#x20;

The action buttons allow you to edit the company name or delete the company. The contacts have to be deleted before you can delete the company.
