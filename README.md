# ansible-init

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

# upgrade pip
sudo pip3 install --upgrade pip

# install homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# install ansible
brew install ansible

# clone this repo
mkdir Workspace
cd Workspace
git clone git@github.com:manuelserradev/ansible-init.git

# run playbook
ansible-playbook macos.yml --ask-become-pass
```

## wsl

```bash
# install openSUSE
wsl --install openSUSE-Tumbleweed

# enter openSUSE
wsl

# upgrade release
zypper dup

# install mvp
zypper install git ansible

# clone this repo
mkdir ~/workspace
cd ~/workspace
git clone git@github.com:manuelserradev/ansible-init.git

# run playbook
ansible-playbook wsl-opensuse.yml --ask-become-pass
```
