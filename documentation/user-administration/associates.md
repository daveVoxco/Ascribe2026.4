---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/user-administration/associates
---

# Associates

_Navigate: Administrator/Associates_

An associate is a person who works for your company and can log in to Ascribe. Your license agreement allows you to create associate entries only for employees and contractors of your company.

When you create an associate, you assign privileges to the user. These privilege settings grant or deny access by the person to various features of Ascribe.

{% hint style="info" %}
#### Note

An associate with only client privilege is **not** the same as a [contact](contacts.md) with client privilege. An associate with client privilege is able to access the client functions for **all studies**. A contact with client privilege is able to access only those studies for which the client company or the end customer company is the same as the contact company.
{% endhint %}

## Toolbar <a href="#minitocbookmark2" id="minitocbookmark2"></a>

The toolbar has these fields:

<table><thead><tr><th width="234" align="center" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/add_new_associate.jpg" alt="" data-size="original"></p><p>Add New Associate</p></td><td valign="top">Displays Properties dialog. Required fields are user name and email address.</td></tr><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/deleted_users.jpg" alt="" data-size="original"></p><p>Delete Users</p></td><td valign="top">Displays a list of deleted users. Right-click a user to restore the user.</td></tr><tr><td align="center" valign="top">Row Groups</td><td valign="top">Drag a column header to this control to group rows by that column.</td></tr><tr><td align="center" valign="top">Search</td><td valign="top">Search for rows containing the search text. The search text may appear anywhere in the rows. The search is 'sticky', meaning it stays until the field is cleared. You can use some regular expression operators such as | or angle brackets. See <a href="../ascribe-coder/codebooks/regular-expressions.md">Regular Expressions</a> for more information.</td></tr></tbody></table>

## Columns <a href="#minitocbookmark3" id="minitocbookmark3"></a>

You customize the Associates page by using the [Table Manager/Columns](../study/table-manager-columns.md) option.&#x20;

Here are the available columns:

| Field         | Description                                                                                                                                                                                                                                                                                                                                    |
| ------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| User Name     | ID used for logging in and tracking of activity, if the associate does not have [single sign-on](../get-started/single-sign-on-overview.md) (SSO) authentication. If  user has SSO, then the user name is only used for tracking activity.                                                                                                     |
| SSO           | SSO stands for [single sign-on](../get-started/single-sign-on-overview.md). If a user has SSO, then a dot displays in this column.                                                                                                                                                                                                             |
| MFA           | MFA stands for multi-factor authentication.                                                                                                                                                                                                                                                                                                    |
| External IDP  | Displays the external identify provider used with SAML technology; please contact Ascribe Support for more information.                                                                                                                                                                                                                        |
| First Name    | The first name of the associate; this field is not editable if the user has single sign-on credentials.                                                                                                                                                                                                                                        |
| Last Name     | The last name of the associate; this field is not editable if the user has single sign-on credentials.                                                                                                                                                                                                                                         |
| Full Name     | Full name of the associate; this field is not editable if the user has single sign-on credentials.                                                                                                                                                                                                                                             |
| Hourly Rate   | Used to calculate job cost in the [time accounting](../client-access-to-data/time-accounting/time-accounting-reports/) reports                                                                                                                                                                                                                 |
| Email Address | Used for password reset requests by the user and used for [SSO](../get-started/single-sign-on-overview.md) logins. This field is not editable if the user has single sign-on credentials.                                                                                                                                                      |
| SSO Email     | The email address in this column identifies the SSO identity for the user. This field is most helpful when using [email plus addressing](../get-started/single-sign-on-plus-addressing.md).                                                                                                                                                    |
| Address       | Informational only, not currently used by Ascribe; this field is not editable if the user has single sign-on credentials.                                                                                                                                                                                                                      |
| Phone Number  | The phone number validation defaults to US phone numbers. If you enter anything that could be interpreted as a US phone number, it will be saved with the country code +1. For phone numbers from any other country, enter the country coded with a + at the beginning. This field is not editable if the user has single sign-on credentials. |
| Last Activity | Date of last activity in Ascribe                                                                                                                                                                                                                                                                                                               |
| Privilege     | The privileges assigned to this associate. You can change this by editing the associate. When you add an associate, some privileges may already be set through the [Default Associate Privilege](../site-administration/site-configuration.md) option.                                                                                         |

## Add/Edit an Associate <a href="#minitocbookmark4" id="minitocbookmark4"></a>

Navigate: Administrator/Associates

From the Associates page, select Add New Associate or right-click and select Edit. A dialog displays with these fields:

<table><thead><tr><th width="236" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">User Name</td><td valign="top">The user ID used for login and tracking, if the user does not have <a href="../get-started/single-sign-on-overview.md">single sign-on</a> credentials. If the user has single sign-on credentials, it is used for tracking, and their login is their email address.</td></tr><tr><td valign="top">First Name</td><td valign="top">Self-explanatory</td></tr><tr><td valign="top">Last Name</td><td valign="top">Self-explanatory</td></tr><tr><td valign="top">Full Name</td><td valign="top">Can automatically be copied from First Name and Last Name fields when you click OK.</td></tr><tr><td valign="top">Email Address</td><td valign="top">Ascribe uses email addresses for password resets and <a href="../get-started/single-sign-on-overview.md">single sign-on</a> identities. If a user has single sign-on credentials, only the user can edit the email address on the User Options page.</td></tr><tr><td valign="top">Phone Number</td><td valign="top">The phone number validation defaults to US phone numbers. If you enter anything that could be interpreted as a US phone number, it will be saved with the country code +1. For phone numbers from any other country, enter the country coded with a + at the beginning.</td></tr><tr><td valign="top">Address</td><td valign="top">Optional</td></tr><tr><td valign="top">Hourly Rate</td><td valign="top">Used to calculate job cost in the <a href="../client-access-to-data/time-accounting/time-accounting-reports/">time accounting</a> reports.</td></tr><tr><td valign="top"><p>Copy User Settings</p><p> </p></td><td valign="top">Use the drop-down list to copy an existing user's settings to a new user. These settings are for anything that 'sticks'; for example, which columns are displayed on the Studies and Questions page and settings for Ascribe Coder.</td></tr><tr><td valign="top">Reset Password and Notify Users by Email</td><td valign="top">This option sends an email to the user and allows them to get a one-time password to login and then change their password. If a user has single sign-on credentials, this option is not available; this user must reset their password from the Log In page or User Options.</td></tr><tr><td valign="top">Ascribe Coder</td><td valign="top">Select the privilege for the associate</td></tr><tr><td valign="top">Product</td><td valign="top">Select the privilege for CX Inspector and/or Ascribe Illustrator as appropriate</td></tr><tr><td valign="top">Account</td><td valign="top">Select Administrator if the associate should have that privilege and Localize if the associate should be able to translate the account.</td></tr></tbody></table>

## Associates and Single Sign-On <a href="#minitocbookmark5" id="minitocbookmark5"></a>

When a user has single sign-on credentials, this identity now applies to all accounts where SSO was set up. Therefore, the first name, last name, full name, email address, phone number and address can only be changed by the user on the User Options page. An administrator cannot change these fields or reset their password. The user must reset their password from the Log In page or User Options.

## Delete an Associate <a href="#minitocbookmark6" id="minitocbookmark6"></a>

From the Associates page, right-click an associate and select Delete.

When you delete an associate, the records of activity by that associate are not removed from the Ascribe database. The username for the associate is changed by the addition of a leading underscore character. Prior activity by this associate will remain in reports such as session records and time accounting.

You also can disable an associate so that he or she cannot log in. This allows you to reactivate the associate in the future if you wish. To do this, clear all access check boxes in the Edit dialog for the associate.
