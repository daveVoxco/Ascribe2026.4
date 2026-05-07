---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/data-management/how-to-load-data/auto-ftp-setup
---

# Auto FTP Setup

Users can load data files automatically via an SFTP site setup to receive files from a secure location. Once we set up the SFTP site, you will send the files to:

media.languagelogic.net/\<account>, where \<account> is your Ascribe account ID.

A username and password are required for the site. The Ascribe support team will provide users with credentials to access the site.&#x20;

This folder is a write-only folder. Once your file lands here, it is immediately sent to the site for loading.

To successfully transfer files and load them into a project in Ascribe, you must follow the file naming standards. In order to load a data file into a project/study, the file name must contain the Ascribe study ID as the first portion of the file name. The study ID is delimited by a client defined character and may be followed by any additional file details. By default, the defined delimiter is a period "."; however, this can be changed by an account administrator on the "Account Options" page in Ascribe or for specific file types, in the load file type editor (see [Load File Types](load-file-types.md).)

An example file name might be _proj123.12-31-05.txt_ where proj123 is the Ascribe study ID, 12-31-05 is general file info not used by Ascribe, and . txt is the load file type.
