---
description: Understand how SSO works in Ascribe and what users need to sign in.
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/get-started/single-sign-on-overview
---

# Single Sign-On Overview

Single sign-on (SSO) allows users to switch between accessible accounts without re-entering their user name and password. During SSO creation process, your email address becomes your login ID.

**All associates created after March 26, 2025 are created as SSO users. No additional action required. After March 26, 2025, administrators have the option to select associates and make them SSO users via the Associates page. Simply select an association, and the option Convert to SSO displays. The user will receive email instructions.**

If user has more than one user ID on an account, please see [Single Sign-On Plus Addressing](single-sign-on-plus-addressing.md); these users need an additional step before creating a single sign-on identity. (A user might have multiple user IDs on an account depending on their function; for example, coding or quality checking or translating.)

Here are the steps for creating a single sign-on identify:

* Login to an Ascribe account. Click the Account drop-down arrow in the black header and select Switch to Single Sign-On.
* An email verification code is sent to your email. Copy/paste the code into the dialog that displays.
* The Create SSO ID dialog displays. Verify your name and enter a new password and click OK.
* You are logged out. Your email address is now your login ID for that account.
* You have to establish SSO on every account you want to access.
* Your legacy user name becomes a 'nickname' that is still used for tracking purposes (Open Sessions, Associates page, applying codes, etc.)
* Once you have established SSO on multiple accounts, you can switch accounts by clicking the Account drop-down.
* If you change your password, you do not need to change it on every SSO account.

See[ How to Become an SSO User](single-sign-on-overview.md#minitocbookmark3) for more detailed instructions.

## Types of Users <a href="#minitocbookmark2" id="minitocbookmark2"></a>

We have three types of users:

* Legacy - your user name/login ID and password are stored in the account database; you have to enter your user name and password every time you access an account. When a password change is required, you have to change it on every account.
* SSO - your login ID is your email address, and your email address and password are stored in an identity provider (IdP). Ascribe uses Amazon Cognitio as the default IdP. No two users may share the same email address. Note that you retain your legacy user name for tracking purposes (who applied a code or translated a response, etc.) The two IDs are linked through the email address on the User Options page. Administrators can see who has SSO IDs on the Associates page.
* SSO with SAML - your company may provide an external identity provider that conforms to the Security Assertion Markup Language (SAML). Your user name is your email address, and you may not need a password at every login time. Please contact Ascribe Support for more information on establishing SAML users for your company.

## How to Become an SSO User <a href="#minitocbookmark3" id="minitocbookmark3"></a>

A legacy user can become an SSO user. The SSO user name will be your email address, which must be unique on the account.

Here are the steps to become an SSO user:

* Log into an Ascribe account with your user name and password. Many Ascribe pages have been recently updated and feature a black header. On the right side of the header are the current account name, followed by the user name. See an example below:

![](https://static.goascribe.com/Help/account_name_position_on_black_header.jpg)

* A legacy user can switch to SSO on any of the new pages. Click the account name and click Switch to Single Sign-On as shown below.

![](https://static.goascribe.com/Help/switch_to_single_siign-on.jpg)

* When you click Switch to Single Sign-On, Ascribe checks whether the user can switch to SSO for this account. The user can switch to SSO if:
* the user has an email address on the User Options page, and
* the email address is well formed,
* and no SSO user on this account has this email address.
* If these conditions are not met, a dialog displays explaining why the user cannot switch to SSO on this account. Otherwise, the user sees this dialog:

![](https://static.goascribe.com/Help/enter_email_verification_code_march18.jpg)

* The verification code is a six-digit number and is sent to the user in an email like this:

![](https://static.goascribe.com/Help/email_address_verification_march_18.jpg)

* The user must type or paste the verification code into the dialog in Ascribe. After entering the correct verification code, a dialog like this is displayed:

![](https://static.goascribe.com/Help/sso_01.jpg)

* The above dialog displays if there is not yet an SSO user on any Ascribe account with this email address. If there were already an SSO user with this email address, a different dialog would display. The user must now enter a password for the new SSO identity. If the first name and last name fields are blank, you must enter that information.
* After the user has entered an acceptable password, they are logged out. The log out screen displays the information below, which notes that the SSO user name is your email address. You must use the email address to access this account.

![](https://static.goascribe.com/Help/new_sso_credentials_march_18.jpg)

When you log in to that account again, the user name displayed in the black bar is the legacy user name. A small icon (<img src="https://static.goascribe.com/Help/single_sign_on_icon.jpg" alt="" data-size="line">) next to the user name indicates the user has single sign-on ability. Here is an example:

![](https://static.goascribe.com/Help/single_sign_on_user.jpg)

The legacy user name is used in Open Sessions, Associates page, and tracking (transactions, who applied codes or translated, etc.)

### Switch to SSO on Other Accounts <a href="#minitocbookmark4" id="minitocbookmark4"></a>

If you have other accounts that you can access, you can switch to SSO on those accounts. Here are the steps to set up SSO on other accounts (you must do this for every account that you want to access using SSO):

* Log into a different account with your legacy user ID, not your SSO email address.
* Go to the User Options page and check that the email address listed is the same address you used as your SSO identity. If it is not, change it to the email used for SSO.
* On one of the Ascribe pages with the black border, click the account drop-down and select Switch to Single Sign-On.

![](https://static.goascribe.com/Help/switch_to_single_sign-on_02.jpg)

* A dialog displays with a message that an email with a verification code has been sent to your email address. Enter or paste the code into the text box:

![](https://static.goascribe.com/Help/enter_email_verification_code_01.jpg)

* Next, a dialog asks you to confirm your SSO password. Enter it into the Password text box:

![](https://static.goascribe.com/Help/confirm_sso_password.jpg)

* You are logged out, and this message displays:

![](https://static.goascribe.com/Help/new_sso_credentials_02.jpg)

**You must go through this process on every account where you want to use single sign-on.**

## How to Access Other Accounts Using Single Sign-On <a href="#minitocbookmark5" id="minitocbookmark5"></a>

Log into an account where you use single sign-on. (Remember that you have to establish SSO on each account that you want to access.) When you want to switch accounts, click the Account drop-down in the black border:

![](https://static.goascribe.com/Help/account_drop-down.jpg)

Any account where you've established single sign-on is listed. Click the account you'd like to visit.

You are then logged out, and the Log Out screen displays the transactions incurred for your work on that account. Click the green button to proceed to the next account.

![](https://static.goascribe.com/Help/log_out_sso.jpg)

The next account opens without the need to enter the SSO password.

You can continue to switch to accounts using the account drop-down.

Note that when you switch accounts, your display settings and privileges are unique to each account. For example, you may display certain columns on one account and different columns on another account. Those settings do not change even though you're using the same email address to log in.

## User Options and Password Reset for Single Sign-On <a href="#minitocbookmark6" id="minitocbookmark6"></a>

Once you have single sign-on credentials, only you can change your name fields, email address, address, and phone number. You can change these fields on the User Options page. Also, you can change your password on the User Options page or request a new password from the Log In page. An administrator cannot reset your password.
