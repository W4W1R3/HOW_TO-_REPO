# How To Clear .Cache Folders and Free Up Space On Your Linux PC

## Disk Usage Analyzer

Disk Usage Analyzer, formerly known as Baobab, is a graphical disk usage analyzer for the GNOME desktop environment. It was part of gnome-utils, but has been a standalone application since GNOME 3.4.

The software gives the user a graphical representation of a disk drive’s contents. The interface allows for selection of specific parts of filesystem so a single folder, the entire filesystem, and even remote folders and filesystems can be scanned and listed at the folder level.

The graphical representation can be switched between a ‘Rings’ chart and a ‘Treemap’ chart to better suit the content being viewed.
Installation

If you don’t already have Disk Usage Analyzer installed, you first need to install the baobab package:

On Ubuntu

    sudo apt install baobab

On Debian

    sudo apt-get install baobab

On Arch Linux

    sudo pacman -S baobab

Fedora

    sudo dnf install baobab

On OpenSUSE

    sudo zypper install baobab

## Clear Cache files and folders

### Step 1:

Click on home for your user data .

Click on your second disk i.e Vostro-14-3468 as shown in the image below .

Note: Names will be different on your own computer.

Here, the other disks shown as New Volume / 262 GB volume are formatted disks for a dual boot system, in my case Ubuntu 20.10 and Windows 10.

### Step 2:

As you click on it, the Disk Usage Analyzer will start to scan your directory for files and folders. Be patient and allow it to finish. After Disk Usage Analyzer is done scanning your Linux PC for files it shows the live illustration of Linux disk usage as the form of a pie chart.

To see updated changes in your filesystem, you’ll need to refresh the scan as it won’t track these storage changes “live.”

Look in the folder tree structure for .cache, and click on it .

### Step 3:

Once you click on the .cache folder, the disk usage analyzer will show you the space it’s consuming graphically on the right side .

    Find the sub folders inside it which you wish to delete .
    Right-click each one
    Select Move to trash / bin
    Now empty your trash / bin

And you are done!

    Do not worry about deleting these folders. It is totally safe and the software will recreate them if and when it needs to.
