# AWS

## key pairs

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
