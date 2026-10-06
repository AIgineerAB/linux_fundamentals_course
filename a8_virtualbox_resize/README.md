# Resize Virtual Machine Harddrive

<a href="" target="_blank">
  <img src="https://github.com/kokchun/assets/blob/main/linux/.png?raw=true" alt="alias" width="600"/>
</a>


There are two main steps to perform, one in virtualbox to increase the hard drive and one in VM to grow the filesystem

## In your host machine 

Open up a terminal in your host machine and type 

```bash
VBoxManage modifymedium disk "/Users/<username>/VirtualBox VMs/<your_vm>/<your_vm>.vdi" --resize <size_in_bytes>
```


## In VM 

```bash
lsblk
sudo growpart /dev/sda 3
sudo pvresize /dev/sda3
sudo lvextend -l +100%FREE -r /dev/mapper/ol-root
```