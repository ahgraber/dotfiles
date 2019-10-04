# .files and configs

## Setting up zsh with oh-my-zsh  

### macOS [Mojave] (using iTerm2)  
#### Prerequisites  
* Install iTerm2  
* Install xcode command line tools: ```xcode-select --install```  
* Install VSCode: https://code.visualstudio.com/  
  * Add ```code``` to command line:  
    1. Launch VS Code.  
    2. Open the Command Palette (⇧⌘P) and type ```shell command``` to find the Shell Command: ```Install 'code' command in PATH command.```  
* Install homebrew: https://brew.sh/ ```/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"``` and add to path
  * Install zsh: ```brew install zsh```  
  * Set system to use homebrew zsh: ```sudo dscl . -create /Users/$USER UserShell /usr/local/bin/zsh```  
#### Additional Customization  
* Install fonts:  
  * Install Awesome Fonts: https://github.com/gabrielelana/awesome-terminal-fonts
  * Install Hack from Nerd Font: https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/Hack
* Install homebrew Ruby: ```brew vendor-install ruby``` and add to path  
* Add gem bin to path (add to ~/.zshrc): 
```
gembin=`(gem env | sed -n "s/.*EXECUTABLE DIRECTORY: \(.*\)/\1/p")`
export PATH=$gembin:$PATH
```
* Install colorls  
  * Install colorls: ```gem install colorls```  
  * Check https://github.com/athityakumar/colorls#flags for flags/combinations for ls aliases
  * Set font to 'Hack Regular Nerd Font Complete' or 'MesloLGF NS' 
  OR  
  (if using iTerm2), use whatever you want for Font and set Non-ASCII Font to 'Hack Regular Nerd Font Complete' or 'MesloLGF NS'
* Install zsh-syntax_highlighting: ```git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting``` and add to plugins list
* Install zsh-completions: ```git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:=~/.oh-my-zsh/custom}/plugins/zsh-completions``` and add to plugins list
* Install oh-my-zsh: ```sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"```
* Install powerlevel10k: ```git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k```
  * run ```p10k configure```
  * Set oh-my-zsh theme to ```ZSH_THEME="powerlevel10k/powerlevel10k"``` (see (dot)zshrc)  
  * Set oh-my-zsh powerlevel mode to ```POWERLEVEL9K_MODE='nerdfont-complete'```
  
#### Windows [WSL] (using hyper)
#### Prerequisites  
* Install hyper: https://hyper.is/  
* Install VSCode: https://code.visualstudio.com/  
* Install Windows Subsystem for Linux (see any guide) -- side note: everything following happens in WSL
  * Add ```code``` to command line: https://code.visualstudio.com/docs/remote/wsl  
#### Additional Customization  
* Install fonts:  
  * Install Awesome Fonts: https://github.com/gabrielelana/awesome-terminal-fonts
  * Install Hack from Nerd Font: https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/Hack
* Install Ruby (using rbenv https://gorails.com/setup/windows/10#ruby-source)
  ```
  cd
  git clone https://github.com/rbenv/rbenv.git ~/.rbenv
  echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc
  echo 'eval "$(rbenv init -)"' >> ~/.bashrc
  exec $SHELL
  
  git clone https://github.com/rbenv/ruby-build.git ~/.rbenv/plugins/ruby-build
  echo 'export PATH="$HOME/.rbenv/plugins/ruby-build/bin:$PATH"' >> ~/.bashrc
  exec $SHELL
  
  rbenv install 2.6.5 # or whatever latest is
  rbenv global 2.6.5
  ruby -v
  ```
* You may have to change the permissions for the .rbenv file: ```sudo chmod -R go-w /home/$USER/```
* Add ruby and gem bin to path (add to ~/.zshrc): 
  ```
  gembin=`(gem env | sed -n "s/.*EXECUTABLE DIRECTORY: \(.*\)/\1/p")`
  export PATH=$gembin:$PATH
  ```
* Install colorls  
  * Install colorls: ```gem install colorls```  
  * Check https://github.com/athityakumar/colorls#flags for flags/combinations for ls aliases
  * Set font to 'Hack Regular Nerd Font Complete' or 'MesloLGF NS' 
* Install zsh-syntax_highlighting: ```git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting``` and add to plugins list
* Install zsh-completions: ```git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:=~/.oh-my-zsh/custom}/plugins/zsh-completions``` and add to plugins list
* Install oh-my-zsh: ```sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"```
* Install powerlevel10k: ```git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k```
  * run ```p10k configure```
  * Set oh-my-zsh theme to ```ZSH_THEME="powerlevel10k/powerlevel10k"``` (see (dot)zshrc)  
  * Set oh-my-zsh powerlevel mode to ```POWERLEVEL9K_MODE='nerdfont-complete'```
