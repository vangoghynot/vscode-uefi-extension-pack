
# My Visual Studio Code Keyboard Shortcuts
[My VSCode Keyboard Shorcuts - Windows](https://github.com/vangoghynot/vscode-resources/blob/main/doc/my_vscode_win_key_cheatsheet.pdf)


# UEFI Firmware Resources

[List of UEFI Firmware Resources](https://github.com/vangoghynot/FirmwareResources)

<br>
<br>

# Installation Guide

Provide some setup guidance before using the extensions. Visit the extension in market place to get more details of each extension, include setup guidance and function details.

## Gitlab Setup

### Create Personal Access Token

First, follow below guidance to create one personal access token(PAT) with the scopes "api" and "read user"
https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html

Note: Remember to backup your token after you create it. You won't be able to access the token after revisit the web page.

### VSCode Extension Setup

Once the PAT is created properly, in VSCode,

-launch the command palette (Press F1)<br>
-Execute command "GitLab: Set GitLab Personal Access Token"<br>
-Input Gitlab server URL (For example: https://gitlab.com)
-Input PAT

### Modify VSCode setting "gitlab.InstanceUrl"

If the official gitlab server gitlab.com is not consumed, the VSCode setting "gitlab.InstanceUrl" should be set to match the target gitlab server.

-Launch the command palette (Press F1)<br>
-Execute command "Preferences: Open Settings (UI)"<br>
-Type "instanceurl" to locate the key "Gitlab: Instance Url".<br>
-Click "Edit in settings.json", modify like below<br>
"gitlab.instanceUrl": "https://your-gitlab.com",

## Git Client Setup
The Git client should be properly configured for the VSCode source control functionality.
### For Windows User

-Visit "Windows Credentials" in Windows "Credential Manager"

[Click to see how to access the credential Manager](https://support.microsoft.com/en-us/windows/accessing-credential-manager-1b5c916a-6a16-889f-8581-fc16e8165ac0)

-Click "Add a windows credential"

assume the target gitlab server address is https://your-gitlab.com

Fill-in below information:<br>

<pre>
Internet address: git:https://oauth2@your-gitlab.com

User name: oauth2
password: [Your PAT]

</pre>


## Project Manager Setup

It's recommended to add the folder path for "Project Manager" extension to enumerate the available projects for switching between projects easily.

For Git projects, VSCode setting "projectManager.git.baseFolders" specify the folders to search available projects.


-Launch the command palette (Press F1)<br>
-Execute command "Preferences: Open Settings (UI)"<br>
-Type "git:base" to locate the key "Project Manager>Git: Base Folders".<br>
-Click "Add Item" to add the folder to be scanned.<br>

<br>
<br>

Hopefully this Quick Guidance Help. Enjoy !!!


# v0.1.5

Add "Installation Guide".
# v0.1.4

Add changelog.md for history


