Rough guideline
- Setup WSL
	- Basically follow windows guide https://docs.microsoft.com/en-us/windows/wsl/install-win10
	- Update Windows
	- Install WSL
	- Make sure to check trouble shoot section in case the installation is not working
- GitHub
	- Create an account
	- Setup SSH connection (follow github guide: https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/connecting-to-github-with-ssh)
	- Trick to copy SSH public key "$ cat id_rsa.pub" to show key in terminal and then copy paste it
- Pyenv
	- $ curl https://pyenv.run | bash
	- Add to bashrc:
		export PATH="~/.pyenv/bin:$PATH"
		eval "$(pyenv init -)"
		eval "$(pyenv virtualenv-init -)"
	- Reboot shell via "$ source ~/.bashrc"
- Install a Python version
	- "$ pyenv install -- list" to show available versions and choose one
	- Install via "$ pyenv install 3.8.6"
	- Create venv: "$ pyenv virtualenv 3.8.6 <name>
- Install VSCode
	- Open within WSL 2 via "$ code ."
