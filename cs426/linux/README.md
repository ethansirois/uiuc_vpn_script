Hello!

Here is the step-by-step guide on how to set-up the automatic connection to the CS426 VM.

**1.** Download necessary packages. You need to install the following dependent packages before you can run this script:
```
openconnect expect lib32ncurses5 lib32tinfo5 lib32z1 libc6-i386 libpkcs11-helper1 openvpn vpnc-scripts net-tools
```
For debian/ubuntu machines, you can just run
```
sudo apt-get install expect openconnect lib32ncurses6 lib32tinfo6 lib32z1 libc6-i386 libpkcs11-helper1t64 openvpn vpnc-scripts net-tools
```
For RHE machines, I think you just replace apt-get with yum or something. Other distros have their own package managers, and you can just use that.

**2.** Download the files in this folder.

After downloading them, you need to make them executable using the command:
```
chmod +x 426env uiucvpnup uiucvpndown enter_cs426_env start_cs426_vm
```
Note: These files should all be located somewhere that has access to your $PATH variable. I put mine in ```~/bin``` You could also put these in ```/usr/bin``` or something.

You can see which directories are in your $PATH variable by running:
```
echo $PATH
```
You can also edit your $PATH variable in your bash configuration file. I would just google it or ask here if you're confused and unsure how to proceed, but that's usually ```~/.bashrc``` or something.

**3.** Add your NetID, NetID password, and your VM number to the file 426env
You are now set up! Simply run:
```
426env
```
in your terminal from any directory. You then have to accept the Duo Push on your phone. Then you should automatically connect to the VPN, and then it will automatically connect you to your personal CS 426 VM machine via SSH.

To exit the CS 426 VM machine, just run:
```
exit
```
In the terminal, and it should bring you back to your desktop.

NOTE: This whole script is a little finnicky due to powering on the VM. It's pretty random, I'd say about 1/2 or 1/3 chance it works, so sometimes you have to run it multiple times. This is because the script tries to continue while the VM is still  being powered on.
