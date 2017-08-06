# ubuntu-note

## Packages

    fonts-inconsolata hime xfce4-notifyd xfce4-power-manager obsession lxdm
    
## Grub

    sudo add-apt-repository ppa:yannubuntu/boot-repair
    
## DNS

    sudo vim.tiny /etc/NetworkManager/NetworkManager.conf
    
    dns=none
  
    sudo vim.tiny /etc/resolv.conf
  
    sudo systemctl disable systemd-resolved.service
    
    sudo vim.tiny /etc/dhcp/dhclient.conf
    
    supersede domain-name-servers 168.95.1.1, 8.8.8.8;
    prepend domain-name-servers 192.168.0.1;
    
## Git

    git config --global push.default current
    
    git config --global alias.co checkout
    
    git config --global alias.br branch
    
    git config --global alias.s status
    
    git config --global alias.cm commit
    
## /etc/xdg/openbox/autostart

    chromium-browser &
    
    #xinput --disable 14 &
    
    xfce4-power-manager &
    
    sakura -s &
    
## Command

    nmtui-connect
   
    tig status
    
    printf "\e]2; wow \a"
    
## Console

   sudo vim.tiny /etc/systemd/logind.conf

   NAutoVTs=1
   
   ReserveVT=1
    
## .config/sublime-text-3/Packages/User/pp.sublime-snippet

        <snippet>
          <content><![CDATA[
        import pprint
        pprint.pprint()
          ]]></content>
          <tabTrigger>pp</tabTrigger>
          <scope>source.python</scope>
        </snippet>

        {
            "color_scheme": "Packages/Color Scheme - Default/Monokai.tmTheme",
            "ensure_newline_at_eof_on_save": true,
            "file_exclude_patterns":
            [
                "main.js.map",
                "main.js"
            ],
            "folder_exclude_patterns":
            [
                "e2e-report",
                "node_modules",
                ".git",
                "dist",
                "screenshots",
                "manual"
            ],
            "font_face": "Inconsolata",
            "font_size": 17.0,
            "ignored_packages":
            [
                "Vintage"
            ],
            "tab_size": 2,
            "translate_tabs_to_spaces": true,
            "trim_trailing_white_space_on_save": true
        }


    
