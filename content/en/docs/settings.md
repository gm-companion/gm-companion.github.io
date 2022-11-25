---
title: Settings
weight: 5
---

## General

### Language and UI Style

These settings should be self-explanatory.  
The following languages are currently available:
 - English
 - German

### Updates

If you enable "Automatically check for updates" you will be notified at prgram start when an update is available.  
By default this setting is disabled, as I recommend to use a package manager to install the program.

### Spotify

See the instructions [here](/docs/tools/audio#spotify).

## Paths

Many tools use file paths that can be changed here.  
I recommend to store stuff like audio project files, maps, character sheets, notes, etc. in a cloud storage and sync them between computers.

## Cloud Storage

It is possible to stream some files from a cloud service. (Currently only Google Drive)  

1. Open the [Google developer console](https://console.developers.google.com)
2. Create a new project
3. Add the Google Drive API (under the G Suite category)
4. Click "Create Credentials"
5. Select the Google Drive API, Choose "Other UI" abd select "User Data"
6. Set up an OAuth consent screen. The only field you need to fill out is the application name. Enter _GM-Companion_.
7. Go back to the credentials page and "Create an OAuth 2.0 client ID"
8. Click on your newly created ID name. A page should open where you can copy a "Client ID" and a "Client Secret".
9. In the GM-Companion settings open the _Cloud Storage_ tab and under _Select File Storage_ select "Google Drive"
10. Enter the Client ID and Secret into their respective textfields in the GM-Companion.

You can now enter the folder ids similar to the normal paths.  
Note that all Google Drive folders used in the GM-Companion need their sharing setting set to "Anyone with the link can view".  
To find the id of a folder open it in a web browser. The URL should be something like `https://drive.google.com/drive/folders/###` where `###` represents the folder id.

## Addons

Here you can enable / disable addons. For more information see [_addons_](/docs/addons).
