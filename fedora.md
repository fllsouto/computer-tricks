## Fedora

### Links

[Fedy](http://folkswithhats.org/)
[EasyLife](https://sourceforge.net/projects/easylife-linux)

### Other Commands

```
# Based on http://www.tecmint.com/things-to-do-after-fedora-24-workstation-installation/
# Updates system
dnf update

# Activate RPMFusion Repository

rpm -ivh http://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-24.noarch.rpm

# Change Hostname

hostnamectl set-hostname <newHostname>

# Install Albert

https://github.com/ManuelSchneid3r/albert/wiki/User-guide

# Things to do after install

https://www.youtube.com/watch?v=JwlWSFAUAnQ
```

## Environment Setup


TODO:
- [ ] Change 2 fedora

```
sudo dnf install xclip

# Creating ~/opt/ folder
mkdir ~/opt

#Installing must have program
sudo dnf install -y vim git curl unrar htop

# Software to configurate dual screen http://askubuntu.com/questions/25339/configuration-tools-for-multiple-monitors-for-x-linux
sudo dnf install arandr

# Installing Sublime Text 3 using Fedy

# Install sublime package installer
# https://packagecontrol.io/installation#st3

# Useful packages
# gitgutter
# git

# Install Ruby on Ubuntu 16.04
# Based on https://gorails.com/setup/ubuntu/16.04

sudo apt-get update
# sudo apt-get install -y git-core curl zlib1g-dev build-essential libssl-dev libreadline-dev libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt1-dev libcurl4-openssl-dev python-software-properties libffi-dev

# sudo dnf install -y git-core openssl-devel readline-devel libxml2-devel

sudo apt-get install -y libgdbm-dev libncurses5-dev automake libtool bison libffi-dev
gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
curl -sSL https://get.rvm.io | bash -s stable
source ~/.rvm/scripts/rvm

# http://www.itzgeek.com/how-tos/linux/centos-how-tos/install-ruby-on-rails-on-ubuntu-centos-fedora-using-rvm.html
rvm requirements #Install Requirements

# Fix problem with openssl https://bugzilla.redhat.com/show_bug.cgi?id=1373810
rvm install 2.3.1 -autolibs=read-only
rvm use 2.3.1 --default
ruby -v

# Install Bundler

gem install bundler

# Install NodeJs

curl --silent --location https://rpm.nodesource.com/setup_6.x | bash -
sudo dnf install -y nodejs

# Install PostgreSQL

sudo sh -c "echo 'deb http://apt.postgresql.org/pub/repos/apt/ xenial-pgdg main' > /etc/apt/sources.list.d/pgdg.list"
wget --quiet -O - http://apt.postgresql.org/pub/repos/apt/ACCC4CF8.asc | sudo apt-key add -
sudo apt-get update
sudo apt-get install postgresql-common
sudo apt-get install postgresql-9.5 libpq-dev

# Install Oracle Java 8 SDK
# Based on http://tecadmin.net/install-oracle-java-8-jdk-8-ubuntu-via-ppa

sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java8-installer

# Check the installation
java -version


# About PATH http://www.linfo.org/path_env_var.html
# About symbolic links http://ubuntuhak.blogspot.com.br/2013/04/symbolic-links-in-ubuntu.html
# About env variables http://www.computerhope.com/issues/ch001647.htm https://help.ubuntu.com/community/EnvironmentVariables

# Install Zsh & Oh-my-Zsh
sudo apt-get install zsh
chsh -s $(which zsh)

# Set correct integration terminal
#https://rvm.io/integration/konsole

# https://github.com/robbyrussell/oh-my-zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

#Install Dropbox

#https://www.dropbox.com/install-linux
wget wget -O 'dropbox_2015.10.28_amd64.deb' - 'https://www.dropbox.com/download?dl=packages/ubuntu/dropbox_2015.10.28_amd64.deb'
sudo dpkg -i dropbox_2015.10.28_amd64.deb
rm dropbox_2015.10.28_amd64.deb
#execute dropbox to finish the instalation

#Install Chrome
# https://www.google.com.br/chrome/browser/desktop/

# Install skype
# https://www.skype.com/en/download-skype/skype-for-linux/

# Install Franz
# meetfranz.com

# Config git
git config --global color.ui true
git config --global user.name "YOUR NAME"
git config --global user.email "YOUR@EMAIL.com"
git config --global core.editor "subl -n -w"


# Generate github key
# https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/
mkdir ~/.ssh
cd ~/.ssh
ssh-keygen -t rsa -b 4096 -C "email@email.com"
ssh-add <private-key>

# ssh -T git@github.com
# ssh -T git@gitlab.com

#copy key to github

# Install Spotify
# https://www.spotify.com/br/download/linux/
# 1. Add the Spotify repository signing key to be able to verify downloaded packages
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys BBEBDCB318AD50EC6865090613B00F1FD2C19886

# 2. Add the Spotify repository
echo deb http://repository.spotify.com stable non-free | sudo tee /etc/apt/sources.list.d/spotify.list

# 3. Update list of available packages
sudo apt-get update

# 4. Install Spotify
sudo apt-get install spotify-client


```
