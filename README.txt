+-----------------------------------------------------------------------------+
| IMPORTANT:   ONLY FOR VMware Workstation 15.5.0 or 15.5.1                   |
| ==========                                                                  |
|                                                                             |
| Don't remove files after installation!!!                                    |
|                                                                             |
+-----------------------------------------------------------------------------+
--Operation confirmed with--
Intel CPU
Windows 10, 64-bit  (Build 18363) 10.0.18363
macOS Catalina 10.15
--------------------

--How To--
1. Install VMware Workstation first.
2. Extract files to any folder.

3. Windows
----------
Explorer right click on the command file and select "Run as administrator".

win-install.cmd   - patches VMware
win-uninstall.cmd - restores VMware
--------------------
3. Linux
----------
On Linux you will need to be either root or use sudo to run the scripts.
You may need to ensure the Linux scripts have execute permissions
by running chmod +x against the 2 files.

lnx-install.sh   - patches VMware
lnx-uninstall.sh - restores VMware
--------------------

4. Editing the VMX File.
If you did not specify location, look in Documents\virtual machines\
Right click on the VMX file and choose "Open with". Choose "More Apps".
From the list of apps that will be seen, choose "Notepad" and press Enter.
At the bottom add the code:

smc.version = "0"

Save the changes.
