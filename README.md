# Iceberg Test
Testing Pharo's Iceberg git tool
## Preamble
Git and Github is my preferred way of sharing my software, and Smalltalk is one of my favorite programming languages. However, I have found Pharo's native git client Iceberg to be confusing, poorly documented, and a chore to use.
This repository is my attempt to understand Iceberg and document git workflows.
## Iceberg
Iceberg is Pharo's native git client. To open it select it from the world menu, or use the hotkey `ctrl + O + I` for Windows and Linux, or `cmd + O + I` for MacOS.
## Worklows
All workflows assume the Iceberg client is open and displaying the Iceberg repositories table. I have tried to match the workflows to the corresponding commands you would use for the Git command line interface.
### Git init
There are several ways of initializing a git repository in Iceberg, some of them use an already existing repository.
#### Adding a git repository on your local computer
This is for when you already have an existing git repository on your computer and you want to add it to the repositories tracked by Iceberg.
1. In the top right corner click `Add local repository`. The dialog box `Import local repository into Iceberg` will open.
2. In the `Local directory` text field enter the file path of the existing git repository root directory, or use the file icon on the right of the text field to navigate to the root director with a file explorer.
3. Optionally in the `Code subdirectory` text field enter the name of the directory that the source code of the repository is located in. Note that this directory **must** exist or Iceberg will throw an error.
4. Click the `Create repository` button. The repository will now be listed in Icebergs table of repositories.
### Git add and git commit
To track changes Iceberg must track one or more Pharo packages in the repository. You will see in the repositories table, in the `Loaded version` field, the text "No package loaded" if Iceberg is not tracking any packages in your repository.
#### Tracking Pharo packages
1. Select the `Packages` tab below the Repositories table. This will display all the packages being tracked in the repository.
2. On the far right click the `Add package` button. This will display the `Choose` dialog showing all the packages in the Pharo image.
3. Select the package containing the code you want to commit to the repository. Dirty packages i.e. packages with their name prefixed by '\*' will be displayed first on the left. You can also use the text field at the bottom to search for your package, which will highlight the matches. Clicking on the package name will close the dialog. The package will be in the `Packages` table with "Uncommitted changes" in the `Status` field.
4.
#### Adding changes
1. Right click on the repository in the table of repositories and select `Synchronize repository...`. The `Synchronizing` dialog will open.
2. Select the `Commit your changes` tab. The `Local changes` pane will show the code changes in a tree of packages, classes, and methods as nodes. When a node with code changes is selected the code diffs will be displayed in the bottom left and right panes.
3. Enter a commit message in the `Commit changes` pane on the top right. Click the `Commit onto master` button to commit the changes. Note that "master" on the button label will likely be different if you are checked out on a different branch.
