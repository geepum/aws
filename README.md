# AWS

## connecting

#### key pairs for ec2 instance

move the pem file to .ssh folder
```bash
mv Downloads/[filename].pem .ssh/[filename].pem
```
<br>

change permissions of the pem file with the least permissions for security
```bash
chmod 400 [filename].pem
```
<br>

connect to the instance using the key
```bash
ssh -i ./[filename].pem [hostname]@[public IPv4 address]
```
<br>

connecting through bastion host
```bash
chmod 400 [key-name].pem # change permissions of the pem file
ssh-add [key-name].pem # add identity
ssh-add -A -i [key-name].pem ec2-user@[public IP] # A means agent forwarding
ssh ec2-user@[private IP of private subnet] # now connecting to private subnet from bastion host
```
<br>

format filesystem
- `mkfs -t (ext4) (/dev/xvdf1)`
<br>

mount and unmount disk
- `mount /dev/xvdf1 /mnt`
- `umount /dev/xvdf1`
- `mount -o nouuid /dev/xvdf1 /mnt`

check disk and blocks
- `lsblk (-f)`
- `file -s (dev/xvdf)`
- `fdisk -l`
- `blkid`
