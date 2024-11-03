**TrueNAS Notes**

***GOAL:***

Create TrueNAS VM in Proxmox and Pass SSD for NFS share to Proxmox for Disk Images, ISO Images, Container templates, VZDump backup files, Containers & Snippets.

[Download TrueNAS Core](https://www.truenas.com/download-truenas-core/)

## TrueNAS VM

 - CPU: 2
 - Memory: 8192

## Pass SSD

Install lshw

    apt install lshw

List physical IDs

    ls -l /dev/disk/by-id/

*looking for output*

    ata-XXX_XXX -> ../../sda

Copy ata-XXX_XXX

Add disk to VM

    qm set 101 -scsi5 /dev/disk/by-id/ata-XXX_XXX

Replace 101 above with VM ID

Replace ata-XXX_XXX above with Copy from prior step

*looking for output*

update VM 101: -scsi5 /dev/disk/by-id/ata-XXX_XXX

source

[Proxmox](https://pve.proxmox.com/wiki/Passthrough_Physical_Disk_to_Virtual_Machine_%28VM%29)

Boot & Install TrueNAS VM

## Create Storage Pool

 - Click **STORAGE**
 - Click **POOLS**
 - Click **ADD**
 - Click **CREATE POOL**
 - Enter a NAME: XXX
 - Select Available Disks
 - Click **CREATE**

## Create dataset

 - Click **STORAGE**
 - Click **POOLS**
 - Find XXX pool created above
 - Click **ADD DATASET**
 - Enter a NAME: XXX
 - Click **SUBMIT**

## Create NFS Share

 - Click **SHARING**
 - Click **NFS**
 - Click **ADD**
 - Find folder /mnt/XXX/XXX and select XXX
 - Click **ADVANCED OPTIONS**
 - Select *MAPROOT USER*: root
 - Select *MAPROOT GROUP*: wheel
 - Enter Authorized Network X.X.X.X
 - Click **SUBMIT**

## Mount TrueNAS NFS Share to Proxmox

 - In Proxmox, Click **DATACENTER**
 - Click **STORAGE**
 - Click **ADD**
 - Click **NFS**
 - Enter ID: XXX
 - Enter Server IP: X.X.X.X
 - Enter Export: /mnt/XXX/XXX
 - Choose Content Types (*select all*)
 - Click **ADD**

TBD

> Written with [StackEdit](https://stackedit.io/).
