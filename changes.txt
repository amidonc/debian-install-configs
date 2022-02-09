# make defualt shell for new users to zsh
/etc/default/useradd
     SHELL=/bin/zsh
     
#change current users shell to zsh
chsh <username> -s /bin/zsh

# remove systemd-bootloader timeout 
/boot/loader/loader.conf
     timeout=0
     
# configure shim with systemd-boot, enable secure boot
      bootctl status **or** dmesg | grep -i secure
     
