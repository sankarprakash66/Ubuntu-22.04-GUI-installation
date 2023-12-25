Ubuntu-22.04-GUI-installation

In this tutorial you will learn: How to install tasksel How to select GUI from tasksel tasks How to install GUI How to login to newly installed GUI
Ubuntu 22.04 Install GUI step by step instructions
Start off by updating the apt package index and installing the tasksel tool with these Linux commands.

$ sudo apt update

$ sudo apt install tasksel
Next, select the GUI you wish to install. Below table shows main desktop environments available for installation via tasksel:
For additional GUI selection execute the below command:

Task Description kubuntu-desktop Kubuntu desktop ( KDE Desktop ) lubuntu-desktop Lubuntu Desktop ( LXQt desktop ) ubuntu-budgie-desktop Ubuntu Budgie desktop ubuntu-desktop Ubuntu desktop ( default GNOME ) ubuntu-desktop-minimal Ubuntu minimal desktop ( default GNOME ) ubuntu-mate-desktop Ubuntu MATE desktop ubuntustudio-desktop Ubuntu Studio desktop ( Xfce-based desktop ) ubuntustudio-desktop-core Ubuntu Studio minimal DE installation ( Xfce-based desktop ) xubuntu-desktop Xubuntu desktop ( Xfce desktop )

$ tasksel --list-tasks
Once you have selected the GUI you wish to install on Ubuntu, execute the following tasksel command. As an example, we will install the default Ubuntu desktop environment, which is GNOME. But you may change this command to match your own selection.

$ sudo tasksel install ubuntu-desktop
After installation, reboot your system.

$ reboot
At this point, the GUI should start. You may need to select your desired desktop flavor on the login page before you login. In case the GUI is not starting at all, make sure your system boots into the graphical target. To do so execute:

$ sudo systemctl set-default graphical.target
