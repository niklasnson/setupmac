# setupmac

##### First of all you need to install 

+ Xcode 

Best is often to download from https://developer.apple.com/downloads/ 


##### User Dropbox/Documents as the Documents folder
```
$ sudo rm -rf ~/Documents
```

```
$ ln -s ~/Dropbox/Documents ~/Documents
```

##### Setup Terminal enviroment 
I love the terminal, this will set it up just like i love it

###### oh-my-zsh
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



```
$ brew doctor
```
run the commands to make brew happy, in most cases xcode-select --install


###### Homebrew Cask
```
$ brew install caskroom/cask/brew-cask
```

Recomended: 

+ brew cask install alfred
+ brew cask install iterm 
+ brew cask install macvim 
+ brew cask install slack
+ brew cask install vlc


####### Install a Ruby build version 
```
# list all versions 
$ rbenv install -l

# install the latest version 
$ $ rbenv install 2.2.3

# set the that verison to the global 
$ rbenv global 2.2.3

```

