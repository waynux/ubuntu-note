# ubuntu-note

## Packages

    gitg cpufrequtils fonts-inconsolata fonts-wqy-microhei faba-icon-theme hime
    
## Grub

    sudo add-apt-repository ppa:yannubuntu/boot-repair
    
## DNS

    sudo vim.tiny /etc/NetworkManager/NetworkManager.conf
  
    sudo vim.tiny /etc/resolv.conf
  
    sudo systemctl disable systemd-resolved.service
    
## Power

  cpufreq-set -g {powersave, userspace, ondemand, conservative, performance}

    sudo cpufreq-set -c 2 -g powersave
    
    cat /sys/devices/system/cpu/cpu*/cpufreq/scaling_governor
    
    cat /sys/devices/system/cpu/*/cpufreq/scaling_cur_freq
