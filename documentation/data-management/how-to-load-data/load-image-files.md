---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/data-management/how-to-load-data/load-image-files
---

# Load Image Files

When you load image files, Ascribe requires the file to be named in this format: RID\_QID.TIF. Here are two examples:

* 00001\_q23.tif
* 42008\_gender.tif

Next, create a compressed archive of the TIF files to be loaded to Ascribe. Name the archive with this format: StudyID.TIF.ZIP. Here is an example:

* 376029.TIF.ZIP

Create the study in Ascribe so that the study ID matches the study ID of the load file (i.e., 376029.).

Load the compressed archive using the [FTP loader](auto-ftp-setup.md).
