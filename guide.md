# How to set up a Python development environment on Windows 10

In this guide we will use the Windows Subsystem for Linux (WSL) to set up a Python development environment. Further we will use Pyenv for managing different Python versions.

## Step 1: Install Windows Subsystem for Linux

First let's make sure that your Windows 10 is up-to-date. Searching and executing "winver" will tell us our current Windows version. In order to install WSL 2 correctly we should have version 2004 or higher. If that is not the case update your system by going to "Settings" and then "Update & Security".
Once our system has version 2004 or higher we can simply follow the official [guide|https://docs.microsoft.com/en-us/windows/wsl/install-win10] provided by Windows for installing WSL 2. The guide covers all necessary steps and provides a lovely troubleshoot section.

## Step 2: Install Pyenv
