# GitToAzure
To access an Azure DevOps repository through git, Git for Windows must be downloaded and initialized first and formost.

Below is the link to the official git webpage. Find the link for **The Lastest Version for Git** on the site and press the blue "Click to Download" link. Make sure it is the correct bit version for your system (example: 64-bit). The latest version as of the 27th of June is Version 2.45.2. 

Link to Git for Windows -> ->     https://git-scm.com/download/win  <- <-

Launch the Git Installer and click **Next** past the *GNU General Public License*. Click Next again and when you are prompted with **Choosing the default Editor used by Git**, if VS Code is installed on your host, pick this option, otherwise leave it to default. 

From here on out, unless you want to personalize your Git settings and know what are you doing, go ahead and leave the defaults until you come to the **Install** button. Install Git and launch the software [Git Bash]

Once Git is downloaded, open up the software and you should have something that looks like this:
![1](/open_git.png?raw=true "Opening Up Git")

Create a new directory for your repository to be stored in by using `mkdir [directory name]` and that Change Directories by using `cd [directory name]`:
![2](/mkdir_cd.png?raw=true "Creating and Changing Dir")

Once you have completed these steps, you will want to open up your companys' Azure DevOps website page. Once on the home page, on the left side of the page, a menu is displayed. Locate the **REPOS** menu option and click on it.
![3](/azure_menu.png?raw=true "Azure Menu")

One of the first boxes in the REPOS sections will say "**Clone to your computer**". A link will be given, make sure to copy this https link. 
Once back at your command terminal, enter `git clone [copied https link from azure]`. This will clone the Azure repository into your new git directory we made earlier. You can check to see if it was successful by typing `ls` into your terminal and see that it has been cloned over to your computer.

Change Directories, `cd [repository name]`, and execute `git fetch` so you will not have to authenticate everytime you reach out to your Azure DevOps site. 

To update to the latest version of the repository, execute `git pull` to pull the updated files from Azure DevOps.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Accessing Azure through Visual Studio Code

In order to access the Azure repository, Visual Studio Code must be downloaded on your machine. It can be found through Visual Studio's website: https://code.visualstudio.com/download

Once VS Code is up and running, log into your Azure DevOps account and locate the shared site. Navigate to your **Repos** tab on the website and click the gray *Clone in VS Code* button. Once pressed, the browser will ask you to open VS Code. When VS Code launches, it will prompt you to make a new file. This is where all files pulled and created for the repository will be stored locally.

When this is all done, locate the **Terminal** button (next to the help tab) on the top left of VS Code and open click on New Terminal. 

NOTE: If this is your first time cloning the repository, you will need to configure your username and email. By default, your username and email are the same and you can check what it is by opening your profile in Azure and finding your email.

In the terminal type these commands to configure your user and email:
`git config user.name "JohnSmith@gmail.com"`
`git config user.email "JohnSmith@gmail.com"`

**COMMITING AND PULLING**
Any changes you make through VS Code on the repository will need to be *committed* to the master branch. To do this, save all file and press the Source Control tab on the far left side of your application:
![3](/SourceControl.png?raw=true "Azure Menu")
Hover over your changed/created files and click the "+" button. This Stages the Changes and gets them ready to commit. Add any comments you might need in the Message section above the **✓Commit** button, then press commit.
