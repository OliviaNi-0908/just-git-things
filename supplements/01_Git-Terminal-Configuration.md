# Installing Git
Git is actually installed on MacOS, but we'll be reinstalling it so that we'll have the newest version:

1. go to https://git-scm.com/downloads
2. download the software for Mac
3. install Git choosing all of the default options

Once everything is installed, you should be able to run `git` on the command line. If it displays the usage information, then you're good to go!


# Configuring Mac's Terminal
We're about to configure the Terminal to display helpful information when in a directory that's under version control. This is an optional step! You do not need to re-configure your terminal for Git to work. You can complete the entire course without reconfiguring it. However, reconfiguring the Terminal makes it significantly easier to use.

## Configuration Steps
To configure the terminal, we'll perform the following steps:

1. download and move the directory `udacity-terminal-config` to your home directory and name it `.udacity-terminal-config` (there's a dot at the front, now!)
2. move the `bash_profile` file to your home directory and name it `.bash_profile` (there's a dot at the front, now!)
   * if you already have a `.bash_profile` file in your home directory, transfer the content from the downloaded `bash_profile` to your existing `.bash_profile`

## First Time Git Configuration
Before you can start using Git, you need to configure it. Run each of the following lines on the command line to make sure everything is set up.

~~~sh
# sets up Git with your name
git config --global user.name "<Your-Full-Name>"

# sets up Git with your email
git config --global user.email "<your-email-address>"

# makes sure that Git output is colored
git config --global color.ui auto

# displays the original state in a conflict
git config --global merge.conflictstyle diff3

# sets up Git with your code editor
git config --global core.editor /usr/bin/vim

git config --list
~~~
