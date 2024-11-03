**TrueNAS Notes**

[Download TrueNAS Core](https://www.truenas.com/download-truenas-core/)

## TrueNAS VM

 - CPU: 2
 - Memory: 8192

## Pass SSD

Install lshw

    apt install lshw

List physical IDs

    ls -l /dev/disk/by-id/

looking for output

    ata-XXX_XXX -> ../../sda

Copy ata-XXX_XXX

Add disk to VM

    qm set 101 -scsi5 /dev/disk/by-id/ata-XXX_XXX

Replace 101 above with VM ID

Replace ata-XXX_XXX above with Copy from prior step

looking for output

update VM 101: -scsi5 /dev/disk/by-id/ata-XXX_XXX

source

[Proxmox](https://pve.proxmox.com/wiki/Passthrough_Physical_Disk_to_Virtual_Machine_%28VM%29)

TBD

> Written with [StackEdit](https://stackedit.io/).
