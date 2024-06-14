# arch
# Arch Configuration

boot from live iso

archinstall
Language English
Mirrors -> Set to Canada
Locales -> Leave en_US etc
Disk configuration -> Best Efrot
Disk Encryption -> Luks, set password
Bootload -> Grub
Swap -> True
Hostname -> archlinux
Root Password -> <set>
User Account -> cpayne with password, sudo
Profile -> Desktop -> Cinnamon
Audio -> Piperwire
Kernels -> Linux
Additional Pacakges -> git neofetch ansible chromium
Network Configuration -> Use NetworkManager
Timezone -> America/Vancouver
Automatic time sync (NTP) -> True


Install!


Then you can pull this repo as root:

```bash
cd /root
git clone https://github.com/krispain/arch.git
```

and run a few playbooks:
```
cd /root/arch/ansible/ && git pull
ansible-playbook initial-setup.xml
ansible-playbook base-cinnamon.xml
```

Will need to manually install 'yay' as a normal user:

```
pacman -S --needed git base-devel && git clone https://aur.archlinux.org/yay-bin.git && cd yay-bin && makepkg -si
```



