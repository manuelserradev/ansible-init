# workstation-init

Super skinny ansible playbooks to quickly configure dev workstations, with SDKs and tools provided by [asdf](https://asdf-vm.com/).

## fedora

```bash
# install ansible
sudo dnf install ansible

# use ansible-pull for initial ws setup
sudo ansible-pull --url https://github.com/manuelserradev/ansible-init
```

## macos

```bash
# install command line tools
xcode-select --install

# install homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# install task (task runner)
brew install go-task/tap/go-task

# clone this repo
mkdir Workspace
cd Workspace
git clone git@github.com:manuelserradev/ansible-init.git

# run setup
cd ansible-init
task
```

## wsl

```bash
# install openSUSE
wsl --install openSUSE-Tumbleweed

# upgrade release & install mvp
sudo zypper --non-interactive dup && sudo zypper --non-interactive install git ansible

# clone this repo
mkdir ~/workspace && git clone https://github.com/manuelserradev/ansible-init.git ~/workspace/ansible-init

# run playbook
cd ~/workspace/ansible-init && ansible-playbook wsl-opensuse.yml --ask-become-pass
```
