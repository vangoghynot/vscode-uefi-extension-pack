
# UEFI Firmware Extension Pack <!-- omit in toc -->

This extension pack packages some useful extensions for UEFI Firmware engineer.

Feel Free to share your useful extensions.

**Thank You !!!**

# Table of Content <!-- omit in toc -->
- [My Visual Studio Code Keyboard Shortcuts](#my-visual-studio-code-keyboard-shortcuts)
- [UEFI Firmware Resources](#uefi-firmware-resources)
- [Installation Guide](#installation-guide)
  - [Gitlab Setup](#gitlab-setup)
    - [Create Personal Access Token](#create-personal-access-token)
    - [VSCode Extension Setup](#vscode-extension-setup)
    - [Modify VSCode setting "gitlab.InstanceUrl"](#modify-vscode-setting-gitlabinstanceurl)
  - [Git Client Setup](#git-client-setup)
    - [For Windows User](#for-windows-user)
  - [Project Manager Setup](#project-manager-setup)
  - [Keyboard Shortcuts](#keyboard-shortcuts)

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

## Keyboard Shortcuts

Press **Ctrl+K Ctrl+S** to launch the **Keyboard Shortcuts** table to customize below hotkeys, 

|Command|Hotkey|Command ID|Comment|
|:------|:-----|:-------|:----------|
|||markdown.extension.editing.toggleBold|Remove the extension default hotkey to keep **Ctrl+B** for toggle sidebar visibility|
|Tasks: Run Task|**Ctrl+K Shift+R**|workbench.action.tasks.runTask| Choose and run one task
|Tasks: Run Test Task|**Ctrl+K Shift+T**|workbench.action.tasks.test|Run default test task
|Tasks: Terminate Task|**Ctrl+K Shift+K**|workbench.action.tasks.terminate|Terminate one or all task(s).


Hopefully this Quick Guidance Help. Enjoy !!!

