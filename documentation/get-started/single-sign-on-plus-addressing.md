---
description: Use plus addressing with SSO to route users and manage account access.
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/get-started/single-sign-on-plus-addressing
---

# Single Sign-On Plus Addressing

Some users has multiple user IDs on an account. For example, a user may use different IDs depending on the activity they perform; for example, coding, quality checking or translating. Usually, those IDs share the same email address. However, there are special considerations when creating a single sign-on identity:

* Your login ID becomes your email address.
* No two users can have the same email address, even if the user is the same person.

To get around these constraints, the user must use email plus addressing.

## What is Email Plus Addressing? <a href="#minitocbookmark2" id="minitocbookmark2"></a>

Most email systems allow the user to add a plus sign after their base address. This creates a unique address - but email is still sent to the base address. Everything after the plus sign is ignored by the email provider.

For example, joe.doe@gmail.com is the base address. An email address like joe.doe+french@gmail.com still sends email to joe.doe@gmail.com.

In Ascribe, the base address and the email address with the plus sign are seen as two unique addresses - so that solves one issue.

The plus addressing also allows the identity provider to create one identity for those addresses. It means a user can login with different email addresses, but use the same password for those addresses.

## How to Create Single Sign-On Identity for a User with Multiple IDs on an Account <a href="#minitocbookmark3" id="minitocbookmark3"></a>

The first step is to edit the email addresses of the user and add the plus addressing.

* An administrator can make the change on the Associates page. Right-click the user and select Edit.
* A user can edit their email addresses themselves via the User Options page.

When editing the email address, add a plus sign to the address and some text after the plus sign. It can be helpful to add text that identifies the role of the user. For example, joe.doe+qc@gmail.com, which indicates this login is for quality checking or joe.doe+spanish@gmail.com, which indicates this login is for coding in Spanish.

The email address for each user ID has to be changed, and each email address must have unique text after the plus sign.

## Plus Addressing Rules <a href="#minitocbookmark4" id="minitocbookmark4"></a>

Email addresses must:

* Not contain a space character
* Contain a dot in the domain (the portion following the @ sign)
* Not have a plus sign in the domain
* Not start with a plus sign
* Contain only one plus sign (or no plus sign if using the base address)
* Not have a plus sign as the character before the @ sign.)

## Next Steps <a href="#minitocbookmark5" id="minitocbookmark5"></a>

Follow the steps in [How to Become an SSO User](single-sign-on-overview.md#minitocbookmark3); you have to do these steps for each user ID that you have. If you have multiple user IDs on multiple accounts, you have to follow the steps for each user on each account.

## How to Access Other Accounts Once You have Single Sign-On <a href="#minitocbookmark6" id="minitocbookmark6"></a>

Log into an account where you use single sign-on. (Remember that you have to establish SSO on each account that you want to access.) When you want to switch accounts, click the Account drop-down in the black border:

![](https://static.goascribe.com/Help/Switch_accounts.jpg)

The drop-down displays the account and user IDs available to you. If you have a single sign-on identity on multiple accounts, those accounts and user IDs are also listed.

You are then logged out, and the Log Out screen displays the transactions incurred for your work on that account. Click the green button to proceed to the next account.

The next account opens without the need to enter the SSO password.

You can continue to switch to accounts using the account drop-down.

Note that when you switch accounts, your display settings and privileges are unique to each account. For example, you may display certain columns on one account and different columns on another account. Those settings do not change.

## User Options and Password Reset for Single Sign-On <a href="#minitocbookmark7" id="minitocbookmark7"></a>

Once you have single sign-on credentials, only you can change your name fields, email address, address, and phone number. You can change these fields on the User Options page. Also, you can change your password on the User Options page or request a new password from the Log In page. An administrator cannot reset your password.

## Changing SSO Email Address <a href="#minitocbookmark8" id="minitocbookmark8"></a>

If you change your SSO email address, the change affects all users that share the same SSO identity. You can change your email address on the User Options page.

Let's say you change from joe.doe@gmail.com to joe.doe@yahoo.com. You should retain the plussing for the multiple users. For example. joe.doe+qc@gmail.com should become joe.doe+qc@yahoo.com. Once you make a change for one address, Ascribe will update your other email addresses on all accounts and retain the plussing.
