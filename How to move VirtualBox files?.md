# How to move VirtualBox files?

The easiest method doesn't require removing your virtual machines and mucking up their settings.

    1. Copy your Virtualbox VMs folder to a new drive. Run the Virtual Box Machine Manager. Run the media Manager File -> Virtual Media Manager

    2. Choose the VM to move storage for. Click the Release button and then the Remove button. On the next dialog, you can either remove or keep the virtual drive. Close the manager leaving you in your Virtualbox Machine Manager.

    3. Select the VM you just removed media for, click the Settings button, Click the Storage section. Add a controller for the media (SATA usually) and then add a hard drive and choose existing disk and select the VD at your new location.

    4. Repeat for each machine you're moving


Fire off your virtual machine at the new location to check. Next time you visit the Virtual Media Manager, hovering over the VM entry will show you where the VD is stored.

Make sure you change your snapshots folders to point to the new drive if you're using them. Each machine has a snapshot folder setting and the VM Manager has a Default Machine folder setting in File -> Settings that needs to be changed as well.

In addition I had to also modify path in xml file. After that it worked flawlessly.

NOTE: Things have changed a bit since this was written, see Rob's answer. It's extremely simple now
