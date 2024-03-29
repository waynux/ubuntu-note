# ubuntu-note

## autologin
    sudo gpasswd -a $USER nopasswdlogin

## .config/openbox/screenshot.sh

    scrot -s /tmp/foo.png -e 'xclip -selection c -t image/png < $f'     

## .config/openbox/rc.xml or /etx/xdg/openbox/rc.xml
    
    <keybind key="A-F3">
      <action name="Execute">
        <command>sh .config/openbox/screenshot.sh</command>
      </action>
    </keybind>

    <keybind key="A-F2"><action name="Execute"><command>grun</command></action></keybind>

    <keybind key="XF86AudioRaiseVolume"><action name="Execute"><command>amixer set Master 5%+</command></action></keybind>

    <keybind key="XF86AudioLowerVolume"><action name="Execute"><command>amixer set Master 5%-</command></action></keybind>


## .bashrc

    bind '"\e[A": history-search-backward'
    bind '"\e[B": history-search-forward'
    PS1="\n\[\e[33m\]\w > \[\e[m\]"
    alias s='subl'


## /etc/lightdm/lightdm.conf.d/10-autologin.conf

    [Seat:*]
    autologin-guest = false
    autologin-user = wayne
    autologin-user-timeout = 0

    [SeatDefaults]
    allow-guest = false

## Packages

    sudo apt --no-install-recommends tlp tlp-rdw fonts-inconsolata hime xfce4-notifyd xfce4-power-manager obsession adwaita-icon-theme gtk2-engines gtk2-engines-murrine gtk2-engines-pixbuf hime-gtk2-immodule hime-gtk3-immodule policykit-desktop-privileges gvfs firefox im-config curl sakura
    
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
    
## sudo vim.tiny /etc/netplan/00-installer-config.yaml
    
    network:
      version: 2
      renderer: networkd
      ethernets:
        enp0s3:
          dhcp4: true
          optional: true
    
    
## Git

    git config --global push.default current
    
    git config --global alias.co checkout
    
    git config --global alias.br branch
    
    git config --global alias.s status
    
    git config --global alias.cm commit
    
## /etc/xdg/openbox/autostart

    brave-browser &
    
    #xinput --disable 14 &
    
    xfce4-power-manager &
    
    sakura -s &
    
## Command

    im-config -n hime

    nmtui-connect
   
    tig status
    
    printf "\e]2; wow \a"
    
## /etc/systemd/logind.conf

    NAutoVTs=1

    ReserveVT=1
    
## id3v2 -D *.mp3

    curl -T 1.mp3 ftp://192.168.0.103:2121/Download/
    
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
                "node_modules",
                ".git",
                "dist",
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


    
