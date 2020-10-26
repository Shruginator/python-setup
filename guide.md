# How to set up a Python development environment on Windows 10

This guide is a quick reference on how to set up a Python development environment on Windows 10 using the Windows Subsystem for Linux (**WSL**).
Further we will use Pyenv for managing different Python versions.

In addition, we will show how to connect to GitHub in order to start our own development project and how Windows allows us to use VS Code on Windows while remotely connecting to WSL.

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

Pyenv is a simple tool for managing Python versions on your system, which is highly recommended if you are going to develop and work on several projects at the same time that require different versions of Python.
Check out the official [Pyenv repository](https://github.com/pyenv/pyenv) for a deeper understanding.

If you want to find out more about the WSL or Pyenv check out the web.
There is plenty of content itnroducing you to them and explaining why they are good for you.😎

## Step 1: Install Windows Subsystem for Linux

First let's make sure that your Windows 10 is up-to-date. Type "winver" in the Windows search bar and excecute the command by pressing enter. The opening window tell us our current Windows version. In order to install WSL 2 correctly we should have version 2004 or higher. If that is not the case update your system by going to "Settings" and then "Update & Security". Once the download has finished we need to perform the update which might take a bit of time.

If our system up-to-date we can simply follow the official [guide](https://docs.microsoft.com/en-us/windows/wsl/install-win10) provided by Windows for installing WSL 2. The guide covers all necessary steps and provides a lovely troubleshoot section. Feel free to checkout the additional information and tutorials provided by Windows.

## Step 2: Install Pyenv

The official [Pyenv repository](https://github.com/pyenv/pyenv) has an installation guide.
Exemplary we will go through the installation procedure for Ubuntu.
If you are using a different Linux distribution, please make sure to check out the official guide.

On Ubuntu we start by opening the WSL console and running
```
  $ curl https://pyenv.run | bash
```
which pulls ??? How did we get the Python version?

Next we add the following commands to our `.bashrc` file, which can be found under `$ ~/home/user/`:
```
  export PATH="~/.pyenv/bin:$PATH"
  eval "$(pyenv init -)"
  eval "$(pyenv virtualenv-init -)"
```
Afterwards we activate the changes via the command `$ source ~/.bashrc`, which reloads the bash with our new configurations.

Install Python build dependencies????
I do believe via
```
  $ sudo apt-get install -y build-essential libssl-dev zlib1g-dev libbz2-dev \
  libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev \
  xz-utils tk-dev libffi-dev liblzma-dev python-openssl git
```

Having Pyenv set up, we can install a specific Python version via
```
  $ pyenv install 3.8.6
```
where we can substitute 3.8.6 for the desired version.
A list of all available versions can be shown via
```
  $ pyenv install --list ?????????
```

## (Optional) Step 3: GitHub Setup

GitHub is a version control system that not only allows you to store your project in the cloud but also makes sharing and collaborating easy.
If you do not have an account yet feel free to head over to [GitHub](https://github.com/) to register.

Once we have our account we can set up our user information used across all local repositories on our machine.
In order to set a name associated with our contributions we can type
```
  $ git config --global user.name "[firstname lastname]"
```
Furthermore,
```
  $ git config --global user.email "[valid-email]"
```
will set an email address that will link our contributions to our account.

Now we can either download an existing repository from the internet via
```
  $ git clone [url]
```
or initialize an existing local directory as a Git repository by executing the following command within the respective directory:
```
  $ git init
```

As a quick reference for the most common GitHub commands we recommend to check out the [Git cheat sheet](https://education.github.com/git-cheat-sheet-education.pdf).

### SSH Setup

Whenever you connect to GitHub from your machine you will be asked for your login credentials.
In order to skip this authentification we can use Secure Shell (**SSH**), which is a network protocol particularly for connecting and authenticating to remote servers and services.

Simply said, SSH works with key pairs, consisting of a public and a private key.
As the names imply, the public key is intended for sharing while the private key should be only known to its owner.
Now the idea is that with the receiver's public key any person can encrypt a message, but that encrypted message can only be decrypted with the receiver's private key.
This concept is called public-key crypthography or asymmetric cryptography and in fact cryptographical algorithms are used to generate the key pair in the first place.

The SSH setup for GitHub is simple thanks to the official [GitHub guide](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/connecting-to-github-with-ssh).
However, we will go through the most important steps for quick reference.
For additional information or troubleshooting please refer to the GitHub guide.



set user profile
generate key "keygen ..."
print key (below)
add key to github profile
clone or create project

For new Linux users it can be bit tricky to extract the public key and enter it to GitHub.
A possible way is to simply print your public key via the command
```
  $ cat id_rsa.pub
```

## (Optional) Step ???: Install VS Code

Download Visual Studio Code (**VS Code**) from the official website, which can be found [here](https://code.visualstudio.com/) or simply google it.

Once we open VS Code for the first time it will detect that WSL installed on our system and thus, ask us we would like to install its remote extensions.
YES!
The remote extensions will allow us to use VS Code on Windows while actually running the code remotely on WSL - a true Linux environment.

There are several ways to connect VS Code to WSL, but the one I find the easiest is to browse within the WSL to the folder of the project I want to open and typing
```
  $ code .
 ```
This will open VS Code on Windows within our WSL project folder, which means that all our files are already within the file explorer.

That's it!
Now we are set up to develop with Python on Windows.

Happy coding!
