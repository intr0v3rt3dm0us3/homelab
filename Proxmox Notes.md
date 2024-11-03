
**Proxmox Notes**

## Helper Scripts

Proxmox VE Post Install

    bash -c "$(wget -qLO - https://github.com/community-scripts/ProxmoxVE/raw/main/misc/post-pve-install.sh)"


Proxmox VE CPU Scaling Governor

    bash -c "$(wget -qLO - https://github.com/community-scripts/ProxmoxVE/raw/main/misc/scaling-governor.sh)"

Proxmox VE Processor Microcode

    bash -c "$(wget -qLO - https://github.com/community-scripts/ProxmoxVE/raw/main/misc/microcode.sh)"

Proxmox VE Kernel Clean

    bash -c "$(wget -qLO - https://github.com/community-scripts/ProxmoxVE/raw/main/misc/kernel-clean.sh)"

Proxmox VE Kernel Pin

    bash -c "$(wget -qLO - https://github.com/community-scripts/ProxmoxVE/raw/main/misc/kernel-pin.sh)"

source of helper scripts

[Helper Scripts](https://community-scripts.github.io/Proxmox/)

## cli commands

How to reboot Proxmox

    shutdown -r +1

How to update ProxMox

    apt update -y && apt full-upgrade -y && apt autoremove -y && apt clean -y && apt autoclean -y

TBD



> Written with [StackEdit](https://stackedit.io/).
