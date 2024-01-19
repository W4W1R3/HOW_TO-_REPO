### How To Close All Open Windows In Linux

One of the most annoying things in any operating system is a situation when you have many open windows and you suddenly want to power off your computer and rush to do something urgent. 

To avoid future problems you should gracefully close all the windows one by one. There is a way to do it with a key combination, but first you need to set it up.

First, you need to install wmctrl, then open your preferred text editor and create the following script:

    #!/bin/bash
    for n in $(wmctrl -l | awk $2 '!/-1/ {print $1}')
    do
        wmctrl -i -c $n;
    done


Save the file, for example as close.sh somewhere within your home directory. Then open your terminal, cd into the directory your script is located and make it executable:

    chmod +x close.sh


Now you need to create a keyboard shortcut that runs the script. For example in XFCE you should open the settings configuration, find the Keyboard section, switch to Application Shortcuts and add the shortcut command, which is the location of your script, e.g. ~/scripts/close.sh. Finally, you will be prompted to set the key combination to run the command. I use Super + Shift + Escape.
