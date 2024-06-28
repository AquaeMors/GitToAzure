# GitToAzure
To access an Azure DevOps repository through git, Git for Windows must be downloaded and initialized first and formost.

Below is the link to the official git webpage. Find the link for **The Lastest Version for Git** on the site and press the blue "Click to Download" link. Make sure it is the correct bit version for your system (example: 64-bit). The latest version as of the 27th of June is Version 2.45.2. 

Link to Git for Windows -> ->     https://git-scm.com/download/win  <- <-


Once Git is downloaded, open up the software and you should have something that looks like this:
![1](/open_git.png?raw=true "Opening Up Git")

Create a new directory for your repository to be stored in by using `mkdir [directory name]` and that Change Directories by using `cd [directory name]`:
![2](/mkdir_cd.png?raw=true "Creating and Changing Dir")

Once you have completed these steps, you will want to open up your companys' Azure DevOps website page. Once on the home page, on the left side of the page, a menu is displayed. Locate the **REPOS** menu option and click on it.
![3](/azure_menu.png?raw=true "Azure Menu")

One of the first boxes in the REPOS sections will say "**Clone to your computer**". A link will be given, make sure to copy this https link. 
Once back at your command terminal, enter `git clone [copied https link from azure]`. This will clone the Azure repository into your new git directory we made earlier. You can check to see if it was successful by typing `ls` into your terminal and see that it has been cloned over to your computer.

Change Directories, `cd [repository name]`, and execute `git fetch` so you will not have to authenticate everytime you reach out to your Azure DevOps site. 

To update to the latest version of the repository, execute `git pull` to pull the updates files from Azure DevOps.
