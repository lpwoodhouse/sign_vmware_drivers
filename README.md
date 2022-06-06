# Bash Script: sign_vm_modules.sh
## Purpose
Sign VMware drivers on Linux host with secure boot enabled, so that VMware Workstation can run VMs successfully.
## Cause
On Linux host with secure mode enabled, it is not allowed to load any unsigned drivers. Due to this, VMware drivers, such as vmmon and vmnet, are not able to be loaded which prevents virtual machine to power on.
## Resolution
Ref Article: https://kb.vmware.com/s/article/2146460
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
### Step 4: Reboot
```shell
shutdown -r now
```
### Final Step
Upon Reboot the option to 'Enroll MOK' should appear. Follow the on-screen instructions. When finished and backup and running, virtual machines in VMware Workstation should be able to power on again. Steps will have to be repeated every time the system kernel is updgraded.
