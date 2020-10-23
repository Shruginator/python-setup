# How to set up a Python development environment on Windows 10

In this guide we will use the Windows Subsystem for Linux (**WSL**) to set up a Python development environment.
Further we will use Pyenv for managing different Python versions.

## Wait, Windows and development?

That is correct!
Casually spoken the Windows Subsystem for Linux, or short WSL, takes the concept of virtual machines to the next level.
The WSL runs on our main system but it does not take any time to load and it also does not require any management for example regarding resources or version from our side.
However, it enables us to run actual Linux applications on Windows.

The subsystem itself is nothing more than a terminal or rather the bash, if you want to say so, with access to your preferred Linux distribution.
But this is not all, because Windows takes it yet to another level.
By installing VS Code's remote extensions you can actually have VS Code open on your Windows system while actually running the code on the WSL via a remote connection.
This way the WSL, being just the bash, also supports an IDE.

## Ok, got it. But what do we need Pyenv for?

Pyenv is a simple tool for managing Python versions on your system, which is absolutely necessary if you are going to develop and work on several projects at the same time.

If you want to find out more about the WSL or Pyenv check out the web.
There is plenty of content itnroducing you to them and explaining why they are good for you.😎

## Step 1: Install Windows Subsystem for Linux

First let's make sure that your Windows 10 is up-to-date. Type "winver" in the Windows search bar and excecute the command by pressing enter. The opening window tell us our current Windows version. In order to install WSL 2 correctly we should have version 2004 or higher. If that is not the case update your system by going to "Settings" and then "Update & Security". Once the download has finished we need to perform the update which might take a bit of time.

If our system up-to-date we can simply follow the official [guide](https://docs.microsoft.com/en-us/windows/wsl/install-win10) provided by Windows for installing WSL 2. The guide covers all necessary steps and provides a lovely troubleshoot section. Feel free to checkout the additional information and tutorials provided by Windows.

## Step 2: Install Pyenv

Opening the WSL console we run `$ curl https://pyenv.run | bash` which pulls ??? How did we get the Python verson?

Next we add the following commands
