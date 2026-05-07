---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/data-management/ascribe-study-shipping
---

# Ascribe Study Shipping

Ascribe can ship archived studies automatically to your company’s FTP site. Those studies are automatically deleted from Ascribe after they are shipped. (The studies are deleted from the site when the next weekly maintenance runs.) This feature improves the usability of Ascribe by removing studies that are no longer active. It also automates your data archiving procedures.

The Study Shipping feature of Ascribe operates only after specific configuration as described in this document. Until the feature is configured, your studies will not be automatically shipped and deleted, and archived studies will remain in the archived state until you delete them.

## Study Shipping Features

Study shipping can help in these ways:

* Weekly shipments - Study shipping occurs every Saturday. Any studies with archived status are shipped at that time and then deleted from Ascribe.
* Automatic save to zip file - Every study to be shipped is saved to a compressed (zip) file. This operation is identical to the interactive Save operation for a study from the Ascribe website. The entire study is always saved (questions, codebooks, codes applied.)
* Optional encryption password - If desired, the zip file can be compressed with an encryption password of your choosing.
* Automatic FTP transfer of the compressed study file - Each compressed study (one study per compressed file) is transferred to your FTP site.
* Automatic deletion of shipped studies - Upon successful completion of the save and transfer operations, the study is deleted from Ascribe.
* Automatic failure recovery - If any part of the shipping process fails for a given study, it is not deleted from the Ascribe website.

## Shipped Studies Page

Navigate: Supervisor/Shipped Studies

You can view a list of shipped studies for your account from the Shipped Studies page. The page defaults to show studies shipped within the last week. However, you can change the default date to view a range of dates.

The Shipped Studies page has this format:

<table><thead><tr><th width="202.6666259765625" align="center" valign="top">Top of the Page</th><th valign="top">Description</th></tr></thead><tbody><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/Excel_export_shipped_studies.jpg" alt=""></p><p>Excel Export</p></td><td valign="top">Click the icon to export the data to Excel</td></tr><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/Refresh_july2025.jpg" alt=""></p></td><td valign="top">Refreshes the page</td></tr><tr><td align="center" valign="top">Date Range</td><td valign="top"><p>There are two ways to select dates. You can use the drop-down list next to the Use local time box to select today, this week, this month, this year, last week, last month, or last year. When you select one of these options, the dates change to reflect your selection, and the report displays.</p><p> </p><p>Another way to select dates is to click Custom Range. A calendar displays. Use the arrows next to the calendar heading to scroll through the months. Or click the heading to see a list of months. Click the heading a second time to see a list of years. Use the arrows to scroll through the months or years.</p></td></tr><tr><td align="center" valign="top">Use Local Time</td><td valign="top">Time tracking uses your local time rather than UTC time.</td></tr><tr><td align="center" valign="top">Search</td><td valign="top">Use the Search field to filter the page.</td></tr></tbody></table>

<table><thead><tr><th width="242" align="center" valign="top">Grid</th><th valign="top">Description</th></tr></thead><tbody><tr><td align="center" valign="top"><p><img src="https://static.goascribe.com/Help/Table_manager_icon.png" alt=""></p><p>Table Manager</p></td><td valign="top">The Table Manager allows you to customize the page, by choosing columns and row options. It opens when you click the hamburger icon. It closes when you move the mouse outside of it.</td></tr><tr><td align="center" valign="top">Ship Date</td><td valign="top">The date the study was shipped</td></tr><tr><td align="center" valign="top">Created</td><td valign="top">The date the study was created</td></tr><tr><td align="center" valign="top">Study ID</td><td valign="top">The ID of the study</td></tr><tr><td align="center" valign="top">Study Name</td><td valign="top">The name of the study</td></tr><tr><td align="center" valign="top">File Name</td><td valign="top">The <a href="ascribe-study-shipping.md#file-management">file name</a> of the shipped study</td></tr><tr><td align="center" valign="top">Supervisor</td><td valign="top">The supervisor of the study</td></tr><tr><td align="center" valign="top">Client</td><td valign="top">The client of the study</td></tr><tr><td align="center" valign="top">End Customer</td><td valign="top">The end customer of the study</td></tr><tr><td align="center" valign="top">Study Description</td><td valign="top">The description of the study</td></tr></tbody></table>

## Configure Study Shipping

To configure study shipping, you need to provide this information to Ascribe Support:

<table><thead><tr><th width="248.66668701171875" valign="top">Data</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">FTP IP address</td><td valign="top"><p>The IP address of the FTP site to which studies are shipped. May be in dot notation or a name that can be resolved to an IP address by DNS.</p><p>If no value is specified, study shipping is disabled.</p><p> </p><p>Examples:</p><p>homeworkforce.net</p><p>216.68.104.125</p></td></tr><tr><td valign="top">FTP port</td><td valign="top">The port number of the FTP site. The default value is 21.</td></tr><tr><td valign="top">FTP ship folder</td><td valign="top"><p>The name of the folder to which study files should be shipped. Must be relative to the root folder of the FTP site. The string provided here is submitted to the CD command of the FTP client used to ship the study.</p><p>It is best to include no blank spaces anywhere in the string.</p><p>Examples:</p><p>ShippedStudies</p><p>ShippedStudies/ FilesIn</p></td></tr><tr><td valign="top">FTP username</td><td valign="top"><p>The username used by the FTP client to log in to your FTP site. If none is provided, the username ‘anonymous’ is used.</p><p>May not have leading or trailing blanks.</p></td></tr><tr><td valign="top">FTP password</td><td valign="top"><p>The password used by the FTP client to log in to your FTP site. If none is provided, the password ‘ LanguageLogic’ is used.</p><p>May not have leading or trailing blanks.</p></td></tr><tr><td valign="top">Encryption password</td><td valign="top"><p>The password used to encrypt the zipped study file. If none is provided, the study file will not be encrypted.</p><p>May not have leading or trailing blanks.</p><p>Example:</p><p>$56hgBG#</p></td></tr></tbody></table>

## Set Up Your FTP Site

Your FTP site should be configured according to your own best practices. The following suggestions may help you in this configuration. These suggestions are intended to help prevent malicious use of your FTP site.

### Required Permissions

The user account for Study Shipping must have read and write privileges in the folder specified by the ‘FTP ship folder’ configuration setting. The account must also have permission to execute the CD command from the root folder to the FTP ship folder.

Study Shipping does not create folders on your FTP site, and does not need permission to do so. The folder specified by the FTP ship folder setting must exist.

### Suggested Settings

We suggest you restrict access to your FTP site by IP address, allowing only the IP address specified by the DNS name media.languagelogic.net

In addition, you may wish to restrict permissions at the file system level for the account used for study shipping. Study Shipping requires only read and write access and the ability to list folder contents. Removal of the ability to create folders can prevent many common hacker attacks

## Maintain Your FTP Site

You must move the shipped files on a regular basis to a secure location (not on the FTP site). This improves security and performance of Study Shipping. Study Shipping will eventually fail if the FTP folder contains too many files (caused by timeouts on a request of folder contents). We recommend that you move the shipped files by a scheduled task running on Sunday.

## Use Encryption

The encryption feature is actually separate from Study Shipping. It applies to all studies saved or restored on the Ascribe web site. If no encryption password is provided, Ascribe will not encrypt the study files it creates, and will accept only unencrypted files for restoring. If an encryption password is provided, Ascribe will encrypt all study files it creates (using the provided password). It will accept either encrypted or unencrypted files for restoring. If you elect to use an encryption password, you will want to give some thought to how widely you disseminate knowledge of the password. Most users of Ascribe should have no need for the password. The password is needed only if the XML contents of the file need to be used.

Changing the password is possible, but studies submitted to Ascribe for later restore operations will need to be either unencrypted, or encrypted with the new password.

We recommend that you keep knowledge of the encryption password to a small group, and that you do not plan to change it.

It is Ascribe policy not to provide the encryption password to anyone by phone. Please make a careful record of your encryption password.

## File Management

Shipped studies are placed in compressed files, and can be decompressed using a standard "zip" program such as WinZip™. The WinZip program is available at http:// www.winzip.com. If you wish to create an automated system for management of study files, you may want a programmable utility to work with zip files. Ascribe uses the Xceed Zip compression library, available at http:// www.xceedzip.com.

File names are constructed for shipped studies as follows:

\<Study ID>\_\<Study name>\<version>.zip

The fields in this name are described in the following table:

<table><thead><tr><th width="222.6666259765625" valign="top">Field</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">&#x3C;Study ID></td><td valign="top">The Study ID, as assigned to the study in Ascribe. The length of this field varies, and is a zero length string if no Study ID is assigned.</td></tr><tr><td valign="top">&#x3C;Study name></td><td valign="top">The Study name, as assigned to the study in Ascribe. The length of this field varies, and is a zero length string if no Study name is assigned.</td></tr><tr><td valign="top">&#x3C;version></td><td valign="top"><p>A zero length string, unless the file name as constructed above already exists in the FTP site. In that case a &#x3C;version> string is constructed by creating a suffix as:</p><p>_N</p><p>where N is an integer that is incremented until the resulting file name does not exist on the FTP site.</p></td></tr></tbody></table>
