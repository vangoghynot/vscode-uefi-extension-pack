
# UEFI Firmware Extension Pack <!-- omit in toc -->

This extension pack packages some useful extensions for UEFI Firmware engineer.

Feel Free to share your useful extensions.

**Thank You !!!**

# Table of Content <!-- omit in toc -->
- [My Visual Studio Code Keyboard Shortcuts](#my-visual-studio-code-keyboard-shortcuts)
- [UEFI Firmware Resources](#uefi-firmware-resources)
- [Installation Guide](#installation-guide)
  - [Gitlab Extension Setup](#gitlab-extension-setup)
    - [Create Personal Access Token (PAT)](#create-personal-access-token-pat)
  - [RST Preview Extension Setup](#rst-preview-extension-setup)
  - [Git Client Setup](#git-client-setup)
    - [For Windows User](#for-windows-user)
  - [Project Manager Setup](#project-manager-setup)
  - [Keyboard Shortcuts](#keyboard-shortcuts)
- [User Guide](#user-guide)
  - [1. Project Manager](#1-project-manager)
  - [2. Markdown File Preview](#2-markdown-file-preview)
  - [3. RST File Preview](#3-rst-file-preview)
  - [4. Git-bash (For Windows)](#4-git-bash-for-windows)

# My Visual Studio Code Keyboard Shortcuts
[My VSCode Keyboard Shorcuts - Windows](https://github.com/vangoghynot/vscode-resources/blob/main/doc/my_vscode_win_key_cheatsheet.pdf)


# UEFI Firmware Resources

[List of UEFI Firmware Resources](https://github.com/vangoghynot/FirmwareResources)


<br>
<br>

# Installation Guide

Provide some setup guidance before using the extensions. Visit the extension in market place to get more details of each extension, include setup guidance and function details.

## Gitlab Extension Setup

In VSCode,

-launch the command palette (Press F1)<br>
-Execute command "GitLab: Authenticate"<br>
-Input Gitlab server URL (For example: https://gitlab.com)<br>
-Choose "Create a token first" or "Enter an existing token"<br>
If you don't have any Gitlab personal access token(PAT) yet,choose "Create a token first", the web broswer will be launched to login into the gitlab server for you to create a new token. (Proceed next section)

If you already have a valid PAT, choose "Enter an existing token" then paste the token.

### Create Personal Access Token (PAT)

First, follow below guidance to create one personal access token(PAT) with the scopes "api" and "read user" right atleast.
https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html

Note: Remember to backup your token after you create it. You won't be able to access the token after revisit the web page.

## RST Preview Extension Setup

Open the VSCode settings UI via command or side bar UI.<br>
-launch the command palette (Press F1)<br>
-Execute command "Preferences: Open Settings (UI)"<br>

Search key "Rst->Preview: Python Path"
Input your python intrepreter path and executable file name. like "c:\python313\python.exe"

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
Password: [Your PAT]
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


# User Guide

## 1. Project Manager

The usage of "Project Manager" extension is available:
https://marketplace.visualstudio.com/items?itemName=alefragnani.project-manager


- Save Project Workspace with Tag
- Switch Project via Tag
- Set Project Root Folders (All Projects under this folder will be listed in treeview.)

## 2. Markdown File Preview

Show preview in right window:<br>
- Open one markdown file in editor<br>
- Press Hotkey Ctrl+K V<br>

Use **Palette** command **Markdown: Open Preview to the side** can achieve the same.

Show preview in tab:<br>
-Open one markdown file in editor<br>
-Press Hotkey Ctrl+Shift V<br>

Use **Palette** command **Markdown: Open Preview** can achieve the same.

## 3. RST File Preview

The .rst file preview can be done through:
- Click the "preview" icon in upper right screen area
- via VSCode command pallete
- Hotkey
<br>
<br>

Show preview in right window:<br>
- Open one RST file in editor<br>
- Press Hotkey Ctrl+K V<br>

Use **Palette** command **RST: Open Preview to the side** can achieve the same.

Show preview in tab:<br>
-Open one RST file in editor<br>
-Press Hotkey Ctrl+Shift V<br>

Use **Palette** command **RST: Open Preview** can achieve the same.


## 4. Git-bash (For Windows)

"Git for Windows" provides Git-bash for Git commands operation in linux terminal type of bash.

Steps to launch Git-bash and set defaule folder in workspace root folder.<br>
- Press F1 to launch command palette
- Select "bash in workspace"