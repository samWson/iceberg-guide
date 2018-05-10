# Iceberg Test
Testing Pharo's Iceberg git tool
## Preamble
Git and Github is my preferred way of sharing my software, and Smalltalk is one of my favorite programming languages. However, I have found Pharo's native git client Iceberg to be confusing, poorly documented, and a chore to use.
This repository is my attempt to understand Iceberg and document git workflows.
## Iceberg
Iceberg is Pharo's native git client. To open it select it from the world menu, or use the hotkey `ctrl + O + I` for Windows and Linux, or `cmd + O + I` for MacOS.
## Worklows
All workflows assume the Iceberg client is open and displaying the Iceberg repositories table.
### Adding a git repository on your local computer
This is for when you already have an existing git repository on your computer and you want to add it to the repositories tracked by Iceberg.
1. In the top right corner click `Add local repository`. The dialog box `Import local repository into Iceberg` will open.
2. In the `Local directory` text field enter the file path of the existing git repository root directory, or use the file icon on the right of the text field to navigate to the root director with a file explorer.
3. Optionally in the `Code subdirectory` text field enter the name of the directory that the source code of the repository is located in. Note that this directory **must** exist or Iceberg will throw an error.
4. Click the `Create repository` button. The repository will now be listed in Icebergs table of repositories.
