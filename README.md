# setupmac

##### First of all you need to install 

+ Mac Os X 
+ iTerm 
+ X code 

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

```
$ brew doctor
```
run the commands to make brew happy, in most cases xcode-select --install


```
$ brew install caskroom/cask/brew-cask
```
Install Brew Cask, now you can install applications with brew. 

