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
* Install homebrew: https://brew.sh/ ```/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"```  
  * Install zsh: ```brew install zsh```  
  * Set system to use homebrew zsh: ```sudo dscl . -create /Users/$USER UserShell /usr/local/bin/zsh```  
#### Additional Customization  
* Install fonts:  
  
* Install colorls  
  * Install rvm:
    ```
    # Install gpg
    brew install gnupg2  
    
    # Get keys to validate RVM
    gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
    
    # Get RVM
    \curl -sSL https://get.rvm.io | bash
    source ~/.rvm/scripts/rvm
    
    mkdir -p ~/.rvm/src && cd ~/.rvm/src && rm -rf ./rvm && \
    git clone --depth 1 git://github.com/rvm/rvm.git && \
    cd rvm && ./install
  
    # Install latest Ruby
    rvm install ruby --latest
    # or Install with homebrew: 
    brew vendor-install ruby
    ```  
  * Install colorls (finally)```gem install colorls```  
  * Check https://github.com/athityakumar/colorls#flags for flags/combinations for ls aliases
* Install oh-my-zsh: ```sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"```
* Install powerlevel10k: ```git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k```
  * Set oh-my-zsh theme to ```ZSH_THEME="powerlevel10k/powerlevel10k"``` (see (dot)zshrc)  
  * Set oh-my-zsh powerlevel mode to ```POWERLEVEL9K_MODE='nerdfont-complete'```
  
#### Windows (using hyper.js)
