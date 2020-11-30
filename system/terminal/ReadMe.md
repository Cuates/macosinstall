[iTerm2](https://iterm2.com/)<br />
[iTerm2 Color Schemes](https://iterm2colorschemes.com/)<br />
[Oh My Zsh](https://github.com/ohmyzsh/ohmyzsh)<br />
[Powerlevel 10k](https://github.com/romkatv/powerlevel10k)<br />
[Zsh Syntax Highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)<br />
[Zsh Syntax Highlighting Install](https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md)<br />
[Powerline Fonts](https://github.com/powerline/fonts)<br />
[Color Hex](https://www.color-hex.com/)<br />
[Customizing iterm2 with ZSH and PowerLevel9k | Z shell Tutorial](https://www.youtube.com/watch?v=pTW02GMeI74)<br />
[Give an awesome look to your terminal!](https://www.youtube.com/watch?v=JnJm4gRrWN8)<br />
[Powerlevel 9k Personalise Your Terminal Prompt For Any Programming Language](https://blog.hassler.ec/wp/2018/11/23/powerlevel9k-personalise-your-terminal-prompt-for-any-programming-language/)

* Download the iterm2 application for Mac OS
  * Install the application into the Application Folder on the Mac OS machine
* Download any itemcolors for your iterm2 application
  * Install
    * <pre>
      Launch iTerm 2. Get the latest version at iterm2.com
      Type CMD+i
      Navigate to Colors tab
      Click on Color Presets...
      Click on Import
      Select the .itermcolors file(s) of the scheme(s) you'd like to use
      Click on Load Presets and choose a color scheme
      </pre>
* Navigate to the ohmyzsh github page
  * Install ohmyzsh within your iterm2 application
    * `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
    * <pre>
      Looking for an existing zsh config...
      Found ~/.zshrc. Backing up to /home/<username>/.zshrc.pre-oh-my-zsh
      Using the Oh My Zsh template file and adding it to ~/.zshrc.

      Time to change your default shell to zsh:
      Do you want to change your default shell to zsh? [Y/n] Y Enter

      Changing the shell...
      Changing shell for &lt;username&gt;.
      Password:
      Shell changed.
      Shell successfully changed to '/usr/bin/zsh'.

              __                                     __
        ____  / /_     ____ ___  __  __   ____  _____/ /_
      / __ \/ __ \   / __ `__ \/ / / /  /_  / / ___/ __ \
      / /_/ / / / /  / / / / / / /_/ /    / /_(__  ) / / /
      \____/_/ /_/  /_/ /_/ /_/\__, /    /___/____/_/ /_/
                              /____/                       ....is now installed!


      Before you scream Oh My Zsh! please look over the ~/.zshrc file to select plugins, themes, and options.

      • Follow us on Twitter: https://twitter.com/ohmyzsh
      • Join our Discord server: https://discord.gg/ohmyzsh
      • Get stickers, shirts, coffee mugs and other swag: https://shop.planetargon.com/collections/oh-my-zsh
      </pre>

* Navigate to the Powerlevel10k github page
  * Install Powerlevel10k in iterm2 application
    * Choose the Oh My Zsh installation instructions
      * `git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k`
* Modify .ZSHrc File
  * `vim ~/.zshrc`
    * Add term color mode
      * <pre>
        # 256 color mode
        export TERM="xterm-256color"
        </pre>
    * Add powerlevel9k mode
      * <pre>
        # POWERLEVEL9K Mode
        POWERLEVEL9K_MODE="nerdfont-complete"
        </pre>
    * Change your ZSH_THEME to the new powerlevel10k in ~/.zshrc file
        * Navigate to the ZSH_THEME and modify it with "powerlevel10k/powerlevel10k"
          * ZSH_THEME="powerlevel10k/powerlevel10k"
  * Save and quit file
* Quit from iterm2 application
  * Full quit from iterm2 as the red X button will not fully exit the application on a Mac OS machine
* If not want to quit iterm2/terminal then
  * `source ~/.zshrc`
* Reopen iterm2 application
* Mac OS
  * Download Font TTF Files
    * `wget https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Regular.ttf`
    * `wget https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold.ttf`
    * `wget https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Italic.ttf`
    * `wget https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold%20Italic.ttf`
  * Install Font TTF Files
    * Double click on each MesloLGS NF TTF file
* On initial install you will need to get true type fonts ttf
  * Following the onscreen prompts
    * Install Meslo Nerd Font?
      * (y) Yes (recommended).
* Download and Install Additional Fonts
  * Clone fonts
    * `git clone https://github.com/powerline/fonts.git --depth=1`
  * Change working directory
    * `cd fonts`
  * Install fonts
    * `./install.sh`
  * Change working directory
    * `cd ..`
  * Remove cloned fonts
    * `rm -rf fonts`
  * Installed  fonts at the following location
    * <pre>
      Copying fonts...
      Powerline fonts installed to /Users/&lt;username&gt;/Library/Fonts (Mac OS)
      </pre>
* Once the ttfs are downloaded and configured close and open the iterm2 application
* On initial install for powerlevel10k you will need to go through the onscreen prompts to configure powerlevel10k
  * If you have already configured the prompts and want to make modifications to the prompt via the wizard execute the following command
    * Configure Wizard
      * `p10k configure`
  * Following the onscreen prompts
    * Does this look like a diamond (rotated square)?
      * `(y) Yes.`
    * Does this look like a lock?
      * `(y) Yes.`
    * Does this look like a Debian logo (swirl/spiral)?
      * `(y) Yes.`
    * Do all these icons fit between the crosses?
      * `(y) Yes. Icons are very close to the crosses but there is no overlap.`
    * Prompt Style
      * `(3) Rainbow.`
    * Character Set
      * `(1) Unicode.`
    * Show current time?
      * `(2) 24-hour format.`
    * Prompt Separators
      * `(4) Round.`
    * Prompt Heads
      * `(1) Sharp.`
    * Prompt Tails
      * `(5) Round.`
    * Prompt Height
      * `(2) Two lines.`
    * Prompt Connection
      * `(2) Dotted.`
    * Prompt Frames
      * `(1) No frames.`
    * Connection Color
      * `(4) Darkest.`
    * Prompt Spacing
      * `(2) Sparse.`
    * Icons
      * `(2) Many icons.`
    * Prompt Flow
      * `(2) Fluent.`
    * Enable Transient Prompt?
      * `(n) No.`
    * Instant Prompt Mode
      * `(1) Verbose (recommended).`
    * Apply changes to ~/.zshrc?
      * `(y) Yes (recommended).`
    * Final output
    * <pre>
      New config: ~/.p10k.zsh.
      Backup of ~/.zshrc: $TMPDIR/.zshrc.t1rWg873hv.

      See ~/.zshrc changes:

        diff $TMPDIR/.zshrc.t1rWg873hv ~/.zshrc

      File feature requests and bug reports at
      https://github.com/romkatv/powerlevel10k/issues
      </pre>
* Modify and add the following
  * `vim ~/.p10k.zsh`
    * Locate
      * typeset -g POWERLEVEL9K_RIGHT_PROMPT_ELEMENTS=(
        * Add above time line
          * date # current date
        * Uncomment below lines  (OPTIONAL)
          * <pre>
            # load
            # disk_usage
            # ram
            # swap
            # battery
            # wifi
            </pre>
      * typeset -g POWERLEVEL9K_TIME_FORMAT='%D{%H:%M:%S}'
        * Add above time_format line
          * <pre>
            ####################################[ date: current date ]####################################
            typeset -g POWERLEVEL9K_DATE_FORMAT='%D{%Y-%m-%d}'
            typeset -g POWERLEVEL9K_DATE_FOREGROUND="#ff6700"
            typeset -g POWERLEVEL9K_DATE_BACKGROUND="#650000"
            </pre>
      * Uncomment below lines
        * <pre>
          typeset -g POWERLEVEL9K_TIME_FOREGROUND=0
          typeset -g POWERLEVEL9K_TIME_BACKGROUND=7
          </pre>
        * Modify with below lines
          * <pre>
            typeset -g POWERLEVEL9K_TIME_FOREGROUND="#3664ff"
            typeset -g POWERLEVEL9K_TIME_BACKGROUND="#00074a"
            </pre>
      * `typeset -g POWERLEVEL9K_PROMPT_CHAR_{OK,ERROR}_VIINS_CONTENT_EXPANSION='❯'`
        * Modify with below line
          * `typeset -g POWERLEVEL9K_PROMPT_CHAR_{OK,ERROR}_VIINS_CONTENT_EXPANSION='$'`
      * Uncomment below lines (OPTIONAL)
        * <pre>
          typeset -g POWERLEVEL9K_WIFI_CONTENT_EXPANSION='%F{${my_wifi_fg[P9K_WIFI_BARS+1]}}$P9K_WIFI_LAST_TX_RATE Mbps'
          typeset -g POWERLEVEL9K_WIFI_VISUAL_IDENTIFIER_EXPANSION='%F{${my_wifi_fg[P9K_WIFI_BARS+1]}}${my_wifi_icon[P9K_WIFI_BARS+1]}'
          </pre>
  * Save and Exit
  * Refresh p10k.zsh
    * `source ~/.p10k.zsh`
* ZSH Syntax Highlighting
  * Clone ZSH syntax highlighting
    * `git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting`
  * Change working directory
    * `cd ~/.oh-my-zsh/custom/plugins/`
  * Echo string into ZSHrc file
    * `echo "source ${(q-)PWD}/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> ${ZDOTDIR:-$HOME}/.zshrc`
  * Refresh ZSH syntax highlighting
    * `source ./zsh-syntax-highlighting/zsh-syntax-highlighting.zsh`
