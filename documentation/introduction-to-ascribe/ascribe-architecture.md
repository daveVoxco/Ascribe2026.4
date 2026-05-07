---
description: Understand how Ascribe is structured and how data moves through the system.
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/introduction-to-ascribe/ascribe-architecture
---

# Ascribe Architecture

Ascribe is a web application, hosted on our secure servers and provides several advantages to you:

* Global accessibility - Ascribe is available from any location on the Internet.
* No installation required - Ascribe requires no installation on your network.
* Low IT costs - Ascribe manages the servers.
* Multi-lingual - Ascribe supports any character set and is Unicode compliant.

## Data Security <a href="#minitocbookmark2" id="minitocbookmark2"></a>

Ascribe provides a comprehensive security framework and strategy. All data is protected by a system of interlocking technologies that ensure maximum protection.

Ascribe is built around SQL Server databases, housed on servers at Amazon Web Services (AWS) in Northern Virginia for our US environment and Frankfurt, Germany for the EU environment. AWS provides 24x7 support for server and infrastructure failures. Ascribe provides multiple levels of security against data loss.

### **Active Data Stores**

Ascribe AI Coder, CXI Inspector and Illustrator data are stored in Amazon Web Services' Simple Storage Service (S3).

All Ascribe Coder data is stored in SQL Server, except for media files which represent responses that are voice or image files, which are also stored in S3.

### SQL Server Data Store

The Ascribe application utilizes multiple, clustered instances of Microsoft SQL Server, version 2019. SQL Server is configured for the Full Recovery model. The SQL data files and active transaction logs are stored on a storage area network (SAN), connected to the clustered database server using a redundant optical fiber network. All data is encrypted at rest.

### S3 Data Store

Data stored in S3 is encrypted and replicated across multiple availability zones to ensure protection from data loss. All files (and versions of files) are saved for 14 days before being wiped.

### Backup Data Stores

The Ascribe SQL Server writes transaction log backups every 30 minutes. Full or differential backups of the active SQL Server data stores and file systems are written to S3 daily and saved for 14 days before being wiped.

## Additional Backup Provisions

In addition to the provided levels of security against data loss, other options are available.

### Repository

The Repository will save current studies in your Ascribe database on a nightly basis to a separate server. Each study is saved in the standard XML file format used for saving and restoring studies to Ascribe.

Each night a backup copy is made of each study, if that study has been modified during the past 24 hours. Backup copies of the study are deleted after 30 days, except for the most recent backup. The most recent backup is retained indefinitely.

### Study Shipping

Study shipping is a standard feature of Ascribe, available to any account. When the study shipping feature is used, Ascribe automatically saves each study in the Archived state to a file, and sends the file via FTP to a location designated by the client. Upon successful transfer, the study is deleted from Ascribe. This feature allows convenient long-term storage of past work.

## Security from Loss of Service <a href="#minitocbookmark4" id="minitocbookmark4"></a>

Ascribe provides multiple levels of security against loss of service.

### Redundant Web Servers

Ascribe uses multiple, identically configured web servers. In the case of failure, another server will transparently be used. The web servers store no user information, so no data loss can occur from failure of a web server.

### Multiple Internet Backbone Connections

Amazon Web Services uses multiple network carriers to prevent loss of service resulting from a network failure at a given carrier.

## Security from Server Intrusion <a href="#minitocbookmark5" id="minitocbookmark5"></a>

Ascribe and Amazon Web Services provide multiple levels of security from server intrusion.

## Security from Website Intrusion <a href="#minitocbookmark6" id="minitocbookmark6"></a>

The Ascribe application has been carefully constructed to prevent intrusion to the website. Access to the website is possible only through the login page, where the user must provide credentials consisting of account, username, and password. The Ascribe website is fully logged, and checked routinely for suspicious activity.

The most likely scenario for website intrusion is by access via stolen credentials. As the administrator for your Ascribe site, you must be certain to educate your staff on the importance of keeping this information safe. You should also make certain to disable unused accounts.

Ascribe prompts each user monthly for a new password. Passwords must be eight characters or longer and must contain at least one uppercase letter, at least one lowercase letter, and at least one number.

It is Ascribe policy not to provide passwords to anyone. If a password is forgotten, you as the administrator can reset the user's password.

## Security in Data Transit <a href="#minitocbookmark7" id="minitocbookmark7"></a>

Ascribe provides security for your data across the web.

### HTTPS Protocol

The Ascribe web sites are equipped with a dedicated SSL (Secure Socket Layer) accelerator. This allows your users to use the https protocol with negligible effect on server-side performance.

To use https, your users need only place "https//:" at the front of the URL used to access Ascribe from their browser. If you wish, Ascribe can modify your account so that all users are required to log in using https. Contact Ascribe support if you would like this option enabled for your account.

### Security of Your Data

Within the limits of their privilege level, your users can download information from the Ascribe web site. Once this information has left the Ascribe servers, Ascribe can of course do nothing to prevent unintended use. Again, you should instruct your staff about security of this information.

Ascribe provides a way to download a zipped XML document containing all information in a study (the study save operation). Ascribe support can provide an encryption password for such files. This password does not need to be known by users of Ascribe. We recommend that you use a strong encryption password, and that you keep knowledge of this password very secure.

## Multi-Lingual, Unicode Compliant Application <a href="#minitocbookmark8" id="minitocbookmark8"></a>

Since Ascribe is a multi-lingual, Unicode compliant application, you can translate Ascribe to other languages. When you translate the site, you change the text displayed by Ascribe in menus, buttons, headers, explanatory text, and so on. Translating the site does not translate verbatim.
