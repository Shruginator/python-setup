# How to set up a Python development environment on Windows 10

In this guide we will use the Windows Subsystem for Linux (**WSL**) to set up a Python development environment. Further we will use Pyenv for managing different Python versions.

## Step 1: Install Windows Subsystem for Linux

First let's make sure that your Windows 10 is up-to-date. Type "winver" in the Windows search bar and excecute the command by pressing enter. The opening window tell us our current Windows version. In order to install WSL 2 correctly we should have version 2004 or higher. If that is not the case update your system by going to "Settings" and then "Update & Security". Once the download has finished we need to perform the update which might take a bit of time.

If our system up-to-date we can simply follow the official [guide](https://docs.microsoft.com/en-us/windows/wsl/install-win10) provided by Windows for installing WSL 2. The guide covers all necessary steps and provides a lovely troubleshoot section. Feel free to checkout the additional information and tutorials provided by Windows.

## Step 2: Install Pyenv

Opening the WSL console we run `$ curl https://pyenv.run | bash` which pulls ??? How did we get the Python verson?

Next we add the following commands
