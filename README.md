macInstalls
===========
ruby -e "$(curl -fsSL https://raw.github.com/Homebrew/homebrew/go/install)"

curl -L http://install.ohmyz.sh | sh

#go to here to install xquartz: http://xquartz.macosforge.org/landing/

brew tap homebrew/dupes

brew tap homebrew/science

brew tap caskroom/cask

brew install brew-cask

brew bundle Brewfile

brew install pkg-config

#optional: change scala to scala210
# install intellij IDE and pycharm, downloaded from web

# install sublime, google this


vim ~/.bashrc
#add the following:
export PATH="/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin:/opt/X11/bin"
# Add python libs to PATH
export PATH="/usr/local/share/python:$PATH"
# SBT
export SBT_OPTS="-Xms512M -Xmx12288M -Xss1M -XX:+CMSClassUnloadingEnabled -XX:MaxPermSize=256M"
# Java
export JAVA_HOME=$(/usr/libexec/java_home -v 1.7)

pip install scipy numpy nose ipython pandas scikit-learn nltk matplotlib


#refer to https://help.github.com/articles/generating-ssh-keys
#add your ssh pub key to your github account

# refer to http://www.sourabhbajaj.com/mac-setup/Homebrew/Cask.html

#optional
brew cask install vlc
brew cask install google-chrome
brew update && brew upgrade brew-cask && brew cleanup

#####################
# after install everything, then checkout the code from github



#############################################
### Brewfile
#############################################
# Use latest version of Homebrew
update

# Upgrade existing formulae
upgrade

# Common dependencies
install gcc
install imagemagick
install openssl
link --force openssl

# Useful dev utilities
install git
install grep
install htop-osx
install jq
install phantomjs
install tmux
install vim

# Python stuff
install python

#install r

# Scala stuff
install scala
install sbt

# Remove outdated versions from cellar
cleanup

