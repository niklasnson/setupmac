# setupmac.markdown

## Intro
Please start with a new installed mac.

##### First of all you need to install 

+ Xcode 

Best is often to download from https://developer.apple.com/downloads/ 


##### Setup git 
```
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
$ git config --global core.editor vim
$ git config --global core.excludesfile '~/.gitignore_global'
```

##### Setup Terminal enviroment 
I love the terminal, this will set it up just like i love it

###### Oh-My-Zsh
```
$ sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

###### Homebrew 
```
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Recomended: 

+ brew install wget 
+ brew install imagemagick
+ brew install rbenv ruby-build
+ brew install ssh-copy-id
+ brew install pyenv-virtualenv
+ brew install gcc --with-all-languages [this can/will take some time]

```
# make brew happy, in most cases xcode-select --install
$ brew doctor
```

###### Homebrew Cask
```
$ brew install caskroom/cask/brew-cask
```

Recomended: 

+ brew cask install alfred
+ brew cask install dropbox
+ brew cask install google-chrome
+ brew cask install iterm 
+ brew cask install mactex 
+ brew cask install macvim 
+ brew cask install slack
+ brew cask install vlc

```
# you might need to run the following command to get icons to show up.
mv ~/L*/Application\ Support/Dock/*.db ~/Desktop; killall Dock; exit
```

####### Set up SSH keys 
```
# generate key and follow instructions 
$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

# start the ssh-agent in the background
$ eval "$(ssh-agent -s)"
Agent pid 59566

# Add your SSH key to the ssh-agent
$ ssh-add ~/.ssh/id_rsa

# Copy the key to the clipboard 
$ pbcopy < ~/.ssh/id_rsa.pub
  > Paste the keys into github, gitlab! 


# Use ssh-copy-id to manage remote servers eg: 
$ ssh-copy-id (user-id)@remote-und.ida.liu.se

```


##### User Dropbox/Documents as the Documents folder
```
$ sudo rm -rf ~/Documents
```

```
$ ln -s ~/Dropbox/Documents ~/Documents
```

####### Get my .vim files and some config files

```
git clone git@github.com:niklasnson/.vim.git
git clone https://github.com/gmarik/Vundle.vim.git ~/.vim/bundle/Vundle.vim
cd .vim
# if you trust me:
./restore.sh
# else:
cp vimrc ~/.vimrc
cp gvimrc ~/.gvimrc
cp zshrc ~/.zshrc
cp gitignore_global ~/.gitigonore_global
# endif
vim +BundleInstall +qall
```

####### Restart terminal!
```
# Yes restart terminal to get some commands from the .zshrc that we need!
```

####### Install Ruby
```
# list all versions 
$ rbenv install -l

# install the latest version 
$ $ rbenv install 2.2.3

# set the that verison to the global 
$ rbenv global 2.2.3
```

####### Install bundler and rails 

```
# install bundler 
$ gem install bundler

# install rbenv-bundler 
$ brew install rbenv-bundler

# install rails 
$ gem install rails
```


####### Install Python
```
# download and compile latest stable python release
$ pyenv install 3.5.0

# set it all up 
$ pyenv virtualenv 3.5.0 virtual-env-3.5.0

# set this version to global 
$ pyenv global 3.5.0

$ pyenv rehash
$ python --version
Python 3.5.0
```

####### Install Flask 
```
# install Flask 
$ pip install Flask

```


####### Install Postgresql
```
# Will install the latest version
$ brew install postgresql

# Start Postgresql at login 
$ ln -sfv /usr/local/opt/postgresql/*.plist ~/Library/LaunchAgents

# Start it right now 
$ launchctl load ~/Library/LaunchAgents/homebrew.mxcl.postgresql.plist

# If you want to manual start 
$ postgres -D /usr/local/var/postgres

```


