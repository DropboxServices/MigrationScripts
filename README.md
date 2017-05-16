# Dropbox Business Services Migration Scripts

Dropbox’s Custom Solution Development Team has built a repository of scripts to support Deployment & Migration projects. No need to start from scratch. These scripts are open source and available to you to simplify and expedite your projects. Python and Powershell scripts available and the list is growing every day!

Notes:

- Powershell scripts require Powershell 5.0 (included in Windows 10). If your system doesn’t have this version you can easily update it at:

https://www.microsoft.com/en-us/download/details.aspx?id=50395
(Included in Windows Management Framework 5.0 install from link above)


## Bulk Create Groups (Dropbox)
Script Description: Script that lets the user mass create a list of groups from a CSV file into Dropbox

Script Use Case: During migration to Dropbox and you need to create many groups at once, without manually creating them one at a time in the web console.


## Bulk Create Team Folders (Dropbox)
Script Description: Script that lets the user mass create a list of team folders from a CSV file into Dropbox.

Script Use Case: During migration to Dropbox and you need to create many team folders at once, without manually creating them one at a time in the web console.


## Export Groups and all Group Members (Box)
Script Description: Script that lets the user export all groups and group members from Box into a CSV file. This file can then be used in conjunction with the Create Group  and the Create Group member scripts below and be used to import CSV files directly into the DfB Admin Toolkit (or can be used as input for the Bulk Create script) to mass create all groups and group members from Box into Dropbox.

Script Use Case: During a migration from Box to Dropbox, you can run this script and then use the output to run against the Create Group and Create Group Member scripts to easily mass create all groups and group members in Dropbox. Those groups will point to this output file, then create the needed CSV files to import directly into the Admin Toolkit for mass creation.


# Create Group Script for Admin Toolkit Import (Dropbox)
Script Description: Script that lets the user point to the output CSV file of the Export Group and Group Members (Box) script and then creates groups output file that is used to import into the DfB Admin Toolkit to mass create groups.

Script Use Case: The user is familiar with using the Dfb Admin Toolkit and wants to easily mimic and mass create their groups for migration from Box to Dropbox. They can point this script to the output of the Export Group and Group Members (Box) script and produce a CSV file to import easily into the Dfb Admin Toolkit.


## Create Group Member Script for Admin Toolkit Import (Dropbox)
Script Description: Script that lets the user point to the output CSV file of the Export Group and Group Members (Box) script and then creates group member output file that is used to import into the DfB Admin Toolkit to mass create groups. (*Note*: You must run the Create Group Script above first, then this script after that one completes. This script needs to get info from Dropbox once the groups are created first).

Script Use Case: The user is familiar with using the Dfb Admin Toolkit and wants to easily mimic and mass create their group members for migration from Box to Dropbox. They can point this script to the output of the Export Group and Group Members (Box) script and produce a CSV file to import easily into the Dfb Admin Toolkit.


## Export Users (Box) 
Script Description: Script that lets the user export enterprise users from Box into a CSV file that can be used to import for other scripts or for the DfB Admin Toolkit for provisioning new users.

Script Use Case: The user needs to have an exact list of enterprise users from Box with email addresses and names to be able to mass provision during a migration from Box to Dropbox. The output can be used to directly import into the DfB Admin Toolkit (Users tab, Provision new users) or with other scripts.


## Export Users (Dropbox)
Script Description: Script that lets the user export users from Dropbox into a CSV file (includes Email and MemberId).

Script Use Case: The user needs to have an exact list of Dropbox users from Dropbox with email addresses and member Id’s The output can be used for future scripts here.


## Update Users Status (Box)
Script Description: Script that lets the user pull the list of enterprise users from Box and mass update their status to read-only, active, or inactive. Uses an exclusion list to ignore any users for update if needed.

Script Use Case: During a migration from Box to Dropbox you can use this script to mass change the status of all users to read only so no content gets updated during the file migration phase.


## Update Users Status from CSV (Box)
Script Description: Script that lets the user point to a previously downloaded CSV list of enterprise users from Box  (using Export Users (Box) script above) and mass update their status to read-only, active, or inactive. Uses an exclusion list to ignore any users for update if needed.

Script Use Case: During a migration from Box to Dropbox you can use this script to point to a CSV list of enterprise users you have already downloaded to mass change the status to read only so no content gets updated during the file migration phase. Using this script you could possibly carve up a much larger list from CSV into chunks and be able to do this step in phases to avoid doing the entire group at once.


## Export Trashed Items (Box)
Script Description: Script that lets the user export a list of all trashed items in Box to a CSV file for review.

Script Use Case: During a migration the user may need to export trashed items in Box and then possibly select items to be restored (as input into in another future Box restore script).


## Export User Shared Folders (Dropbox)
Script Description: Script that lets the user export a list of all shared folders and access type for all users including external collaborators.

Script Use Case: After a migration the user may need to verify that all shares have been correctly applied to all shared folders. This script allows you to do that, and to verify that access types are correct for each shared folder the user has access to.


## Export All Content To CSV (Dropbox)
Script Description: Script that lets the user export a list of all files and folders for all users on Dropbox Business team.

Script Use Case: For pre and post-migration verification of data. This script allows you to do this, by dumping all content to CSV and lets you sort columns as needed to verify any type of file or folder.


## Export All Content To CSV (Box)
Script Description: Script that lets the user export a list of all files and folders for all users on a Box Enterprise team.

Script Use Case: For pre and post-migration verification of data. This script allows you to do this, by dumping all content (files and folders) to CSV and lets you sort columns as needed to verify any type of file or folder.
