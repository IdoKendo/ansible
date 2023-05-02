# Ansible
Ansible playbooks for setting up my environment

# What to do?!
Create a file called pass with the vault password and then run:
```
sudo apt-get update
sudo apt-get upgrade -y
sudo apt-get install -y software-properties-common
sudo apt-add-repository -y ppa:ansible/ansible
sudo apt-get update
sudo apt-get install -y sudo curl git git-lfs g++ ansible build-essential
sudo apt-get clean autoclean
sudo apt-get autoremove --yes
ansible-pull -U https://github.com/IdoKendo/ansible.git --ask-become-pass --vault-password-file pass
source .bashrc
nvm install 18.5.0 && nvm alias default 18.5.0
pyenv install 3.11.3 && pyenv global 3.11.3
```
Don't forget to delete the pass file afterwards!  
To set up the nvim plugins run `nvim ~/.config/nvim/lua/idos/packer.lua` and then inside nvim run:
```
:so
:PackerSync
```
To install the TMUX plugins run tmux and click `prefix + I`
