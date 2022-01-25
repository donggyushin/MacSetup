[MacSetup](#MacSetup) | [Install HomeBrew](#Install-HomeBrew) | [Install applications that you want](#Install-applications-that-you-want) | [Iterm2 setup](#Iterm2-setup) | [For M1 users](#For-M1-users)

# MacSetup
My preference mac setup for developers

# Install HomeBrew
Homebrew installs the stuff you need that Apple (or your Linux system) didn’t.
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
Paste that in a macOS Terminal or Linux shell prompt.

After that copy the two command lines at Next Steps section to the shell configuration file(~/.zshrc). 
<div>
<img src="https://user-images.githubusercontent.com/34573243/150907647-bcc099ba-11f0-403b-bd00-9e8d7b3f07b9.png" width=400 />
</div>

# Install applications that you want
In my case
```
brew install --cask firefox visual-studio-code google-chrome brave-browser spotify slack iterm2
brew install python3 go pipenv nvm gh
```
After install them follow the next steps(Edit shell configuration file)

  ## nvm
  See all node versions
  ```
  nvm ls-remote
  ```
  Install the version you want
  ```
  nvm install v17.4.0
  ```
  
  ## gh
  login
  ```
  gh auth login
  ```
  


# Iterm2 setup
```
Iterm2 > Preference > Appearance > General > Theme > Minimal
Iterm2 > Preference > Profiles > Session > Check `status bar enabled` > Configure Status Bar
  Battery Level, CPU Utilization, Memory Utilization, Network throughput
  Auto-Rainbows: Light Colors
```
  ## My Preference scheme
  [github dark](https://raw.githubusercontent.com/mbadolato/iTerm2-Color-Schemes/master/schemes/GitHub%20Dark.itermcolors)
  ```
  You can select your scheme at Iterm2 > Preference > Profiles > Colors
  ```
  ### How to import itermcolors.txt file
  Delete `.txt` extension from `itermcolors.txt` file like following image
  
  <div>
  <img width="250" alt="스크린샷 2022-01-25 오후 4 58 08" src="https://user-images.githubusercontent.com/34573243/150935352-496b55ec-b927-4ab7-ba62-bef1f6ea38d8.png">
  </div>
  
  And import itermcolors file from Iterm by double click `.itermcolors.txt` file 
  
  ## Oh-my-zsh
  Install
  ```
  sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
  ```
  
  ## Powerlevel10k
  clone the repository
  ```
  git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
  ```
  
  edit ~/.zshrc
  ```
  ZSH_THEME="powerlevel10k/powerlevel10k"
  ```
  
  then restart your terminal
  
  # For M1 users
  Install of Rosetta<br />
  If you want to use M1 Mac without issues related with M1 chip by following the next command.
  ```
  /usr/sbin/softwareupdate --install-rosetta --agree-to-license
  ```
