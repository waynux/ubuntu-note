# ubuntu-note

## Packages

    gitg cpufrequtils fonts-inconsolata fonts-wqy-microhei faba-icon-theme hime
    
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

    
## Power

  cpufreq-set -g {powersave, userspace, ondemand, conservative, performance}

    sudo cpufreq-set -c 2 -g powersave
    
    cat /sys/devices/system/cpu/cpu*/cpufreq/scaling_governor
    
    cat /sys/devices/system/cpu/*/cpufreq/scaling_cur_freq
    
## Git

    git config --global push.default current
    
    git config --global alias.co checkout
    
    git config --global alias.br branch
    
    git config --global alias.s status
    
    git config --global alias.cm commit
    
## /etc/xdg/openbox/autostart

    chromium-browser &
    
    xinput --disable 14 &
    
    sakura -r 40 -c 120 &
    
    xfce4-power-manager &
    
