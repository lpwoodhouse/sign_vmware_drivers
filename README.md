# Bash Script: ubuntu_vm_mod_sign
On Ubuntu host with secure mode enabled, it is not allowed to load any unsigned drivers. Due to this, VMware drivers, such as vmmon and vmnet, are not able to be loaded which prevents virtual machine to power on.

### Step 1: Get the Script
```shell
wget https://raw.githubusercontent.com/lpwoodhouse/ubuntu_vm_mod_sign/master/sign_vm_modules.sh
```
### Step 2: Make the script executable
```shell
chmod +x sign_vm_modules.sh
```
### Step 3: Run the script
```shell
./sign_vm_modules.sh
```
