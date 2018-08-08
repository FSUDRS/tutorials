# Git and GitHub

## Introduction

By the end of this tutorial you will set up an account on [DHBox](http://dhbox.org/), understand and be able to use Git as a protocol for version control, and use GitHub to share code, manage projects, and as a form of social media.

Version control or versioning is the management of changes to files and the management of files themselves. While similar to saving, versioning offers several benefits such as creating multiple versions of the saved file and *revision metadata* or descriptions of the changes that were made since the last save. Git is a piece of software and protocol of the same name that allows for versioning of files. GitHub is an open source platform and social media site for sharing code and files \(the GitHub website is built on top of Git\). Other platforms for source code hosting exist (e.g. SourceForge, Bitbucket, GitLab). 

## Getting Started with DHBox

The first step is to sign up for an account at [dhbox.org](http://dhbox.org/). After logging in to DHBox, navigate to the Command Line tab and enter your log in information again. The command to create a new directory \(folder\) is `mkdir directoryname` \(`mkdir test` would create a new directory or folder named "test"\). The command to create a file is `touch filename.ext` \(`touch test.md` creates a new Markdown file named "test"). Be sure to use the proper extension when creating files. Note that there is a space between the command and the name of the directory or file. Spaces, however, are not allowed in directory or file names. Press enter to execute the commands. 


To navigate through directories, there are three useful commands: `cd`, `ls`, and `pwd`. `cd` stands for "change directory" and allows you to move from one directory to another. 

* `cd directoryname` moves you down to the child directory \(a directory within your current directory\), or you can type in the full pathname for the directory you want to navigate to.
* `cd ..` moves you up to the parent directory \(the directory or folder one level up from the one you are currently in\).
* `cd ~` moves you to the root directory \(the highest level directory or folder you can get to\).
* `ls` shows you the contents \(files and folders within a directory\) you can use it by itself to show the contents of the current directory, or write the name of another directory after it to show the contents of that directory.
* `pwd` stands for "print working directory" and shows you the full pathname to your current directory


To begin, let's create a couple of directories. In the root directory, create a new directory called "documents". Inside the "documents directory, create a file called test.txt \(Plaintext file\). Now create a directory called "code-snippets", create a file called "test.py" (Python file) within the "code-snippets" directory. Create a “README.md” file in the “documents” directory. Create another “README.md” file in the “code-snippets” directory. Note that while you cannot have two files of the same name and type within a single directory, there is no problem with having a file with the same name and type (such as “README.md”) within multiple directories.

After completing the exercises above, to check whether or not the directories and files are being created where you want them, you can click the File Manager tab at the top of DHBox and navigate through the directories and files using a GUI (Graphical user interface).

If in the last exercise, you accidentally created a file that you didnt mean to, you can remove it with the command `rm filename.ext`. This works for files, but not directories. If you accidentally created a directory that you didn't mean to, you will need to use `rm -r directoryname` to remove it. 

If you get lost in your directories while in the command line, remember to use the commands `ls` and `pwd` described above to figure out where you are.

## Git in the Command Line

In order to start using Git, you will need to configure it with a user name and a user email \(you only need to do this once\). Enter the following code:


```
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

Next, navigate to the code snippets repository and type `git status`. You will be returned a message that says `not a git repository` \(or something similar\). This means that the directory you're working in does not have any .git information associated with it. To remedy this, type:

`git init`


Type `git status` again. This time you will receive a message that you have 2 unstaged files. Any files that you want to commit, you will first need to add to the repository by using the command `git add filename.ext` \(This allows you to commit one file in a repository, but not the others, or to completely ignore files that you don’t want in the Git ecosystem\). To add all files in the current directory, type:

`git add .`


The `.` in the above code refers to the current directory. 

The next step to the process is committing the files. This allows you to keep a record of what the file looked like at the time of the commit. In the commit, we can add a succinct but detailed message to explain what changes have been made.

To commit, write `git commit -m "your message goes in quotes"`. After committing, you should get a message that describes the *extent* of the changes to the files \(i.e. number of files/lines added/deleted and the total overall change\).

Now let's edit the README.md file in the "code-snippets" directory. The file can be edited within the UNIX Command Line itself by using the "vi text editor". Use the command `vi filename.ext` \(in this case `vi README.md`\) to open the file in the text editor. After opening the file with "vi" add the text "Hello World!". Now, we need to close the text editor and save the file. Press the Esc key on the keyboard to exit "Insert" mode in "vi", type `:x`, and hit the Enter \(Return\) key to exit the program and save the file. Add and commit the README.md file to the repository. Next, try creating a new Markdown file in the "code-snippets" directory called test.md. Add some text to the test.md file in the same way you added text to README.md. Now add and commit the test.md file to the repository.

To look at the histories or the log of files that you have committed try using `git log`.

That’s the basics of using Git in the command line, now we’ll switch gears and explore the GitHub interface both online and in the GitHub for Desktop application.

The tutorial we just went through describes how to commit files locally on your own machine, or in the case of DHBox, on the DHBox cloud. In the next section we will discuss how to share files on GitHub so that they will be accessible from anywhere with internet access.


## GitHub

Now we'll start by going to the GitHub website at [github.com](http://github.com/) and press the "Sign up" button at the top right of the page. You will be led through the process of creating a personal account. After you create your account, you will need to go download [GitHub Desktop](http://desktop.github.com/) and follow the directions to install it to your computer.


## GitHub Desktop

After installing GitHub Desktop, open it. The first time you open it, it will ask you to sign in with the GitHub account that you just created online. Then you’ll see a screen called Configure Git. Click continue to go to the next screen. The next screen asks if you would like to submit anonymized usage data to GitHub, you can leave this checked or uncheck it before pressing finish.

Now that you’re in GitHub desktop, you’ll probably see a screen that says “No repositories found” and gives you the option to “Create a new repository”, “Add a local repository”, or “Clone a repository”. The first thing that we want to do is “Create a new repository”. When you press the “Create a new repository” button, a popup should appear asking you to type in a “Name”, “Description”, and select a “Local Path”. Create a name for the repository without using any spaces and type a brief description of the repository. Then press the "Choose" button next to Local Path and navigate using the interface to select the folder in which you would like to put your new repository. Also check the box that says “Initialize this repository with a README” (this will create a README.md file for us within the directory that contains the repository). If you navigate to the directory you selected in the previous screen, should now see a new directory has been made on your computer with the name you entered in the “Name” field. Remember, the repository will be able to manage only those files and folders within its container directory. Now, navigate to the folder and open README.md. Edit the text in the README.md to say whatever you would like and then save the file. Now, go back to GitHub Desktop; you should see that under the changes tab it says “1 changed file”. If you select the file you can see the changes within the README.md file. Now we want to commit this file just as we did in the Command Line. In the GitHub Desktop application this is as simple as adding a brief summary of the changes made and a longer description of the changes such that it will make sense to us in the future or to others with whom we share the repository. The final step is pressing the "Commit to master" button. To view all of the changes we have made to the file, click the “History” tab in GitHub desktop next to “Changes”. This will show all of the commits that we have made just as the `git log` command did in the Command Line on DHBox. 

To make the repository accessible online, press the “Publish repository” tab at the top of GitHub Desktop. A popup will appear asking again for a name and description. You can leave these the same as they were on the local repository. A checkbox at the bottom of the page says “Keep this code private”. In paid versions of GitHub, you can publish your repositories privately. In the free version, however, this option doesn’t work. After checking the name and description, press the “Publish repository” button. Now, the repository is also available on the GitHub web page on your account.

## GitHub Web Page

On the [GitHub](http://github.com/) web page, log in. You should see your repositories. If you navigate to the "Repositories" page within GitHub, you can see a list of all your repositories, and there is a button with the option for you to create a new repository called "New". Click the "New" button from this page and you should see a page very similar to the popup in GitHub Desktop when you create a new repository. From there, you will be taken to the "Code" tab of the new repository. The "Code" tab gives detailed instructions on how to set up the repository on your local machine. There is also a convenient "Set up in Desktop" button that will open GitHub Desktop and allow you to clone your online repository to your local machine. After setup, if you open one of your repositories on the GitHub web page you'll be presented with several options along the top, including "Create new file", "Upload files", and "Clone or download". In the next step, we'll talk about *cloning* the repository to create a copy on our machines.

Cloning a repository is making a copy of that repository that can sync up between your local machine and your personal GitHub web page. On the GitHub web page open your repository. From there press the "Clone or download" button and then press the "Open in Desktop" button. You'll now be able to say where you want the repository to exist on your local machine.

Using GitHub Desktop is an easy way to manage files locally on your computer. Pushing the files to the GitHub webpage ensures that they are accessible anywhere that you have internet access.