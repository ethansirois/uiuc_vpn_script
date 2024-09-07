Hello!

Here is the step-by-step guide on how to set-up the automatic connection to the CS426 VM.

**1.** Download the files in this folder.

After downloading them, you need to make them executable using the command:
```
chmod +x 426env enter_cs426_env start_cs426_vm
```
Note: These files should all be located somewhere that has access to your $PATH variable. I put mine in ```~/bin``` You could also put these in ```/usr/bin``` or something.

You can see which directories are in your $PATH variable by running:
```
echo $PATH
```
You can also edit your $PATH variable in your zsh configuration file. I would just google it or ask here if you're confused and unsure how to proceed, but that's usually ```~/.zshrc``` or something.

**2.** Add your NetID, NetID password, and your VM number to the file 426env
You are now set up! 

To enter the VM, you must be on Campus WiFi or use the CISCO AnyConnect VPN (I'm working on finding a way to automate the VPN connection).
See UIUC's help page for working with the CISCO AnyConnect software [here.](https://answers.uillinois.edu/illinois/page.php?id=98773)

Once you are connected to Campus Wifi, or on the campus VPN, you can simply run:
```
426env
```
in your terminal from any directory. You then have to accept the Duo Push on your phone. Then you should automatically connect to the VPN, and then it will automatically connect you to your personal CS 426 VM machine via SSH.

To exit the CS 426 VM machine, just run:
```
exit
```
In the terminal, and it should bring you back to your desktop.


