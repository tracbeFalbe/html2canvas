
 
Microsoft's "Windows Installer CleanUp Utility" could be used to help fix broken installations of MSI-installer based products. When the installer failed in some strange way and left corrupt data behind, so bad that even Add/Remove Programs couldn't help, you could often fix things by running this utility and then running the application's installer again.
 
I just discovered that Microsoft announced a couple weeks ago that they were discontinuing this utility. They didn't merely say "we're not supporting it anymore"; they seemingly removed it from their site entirely.
 
**Download Zip ★ [https://climmulponorc.blogspot.com/?c=2A0SOT](https://climmulponorc.blogspot.com/?c=2A0SOT)**


 
I have to support a Windows program for a whole bunch of users. Given the number of users, every so often something will go wrong, and this program has been invaluable for me, as a last-ditch line of defense.
 
Windows Installer CleanUp utility was never intended to be used in the wild. It was only meant to be used by software developers. If you occasionally have end users needing to use WCU you have some serious installer quality issues that should be addressed.
 
WCU only removes the Windows Instaleller meta data and doesn't actually uninstall any software. This leaves the machine in a very dirty state. These days with test labs becoming virtualized there's no reason to have this tool anymore. You just roll back to a prior snapshot and keep on working.
 
I've seen all kinds of online forums full of users who think they know what they are doing ( and don't ) suggest using WCU to solve various problems so in the end Microsoft decided to try to get the horse back in the barn.

I have uninstalled previous successful installatin of drivers and rebooted. Reason I had to reinstall everything was because I was running a double nat setup and for some reason I could not get my hardwired device with the router to communicate with the printer.
 
Update - called back in. One hour wait but it was worth it. Got another tech named Cory who had me up and running in about 15 minutes. Two things additional things he tried. One - drop the all in one installer (in my case "MF731CMFDriverV5401W64usEN") into the root of your C drive (aka "C:\") and install from there with admin privileges through Windows explorer (right click/run as admin). Two - I think more importantly what did it. There is a program in the "misc" folder (whether you are in the x32 or x64 folder). The file is called, " UNINSTAL.exe" Yes it has one "L." Run that as admin. It should wipe out any traces of old files and registry entries from previous installs. Final thing to download as a bonus if you are using the scanner. Program is called, "[Windows 32bit & 64bit] MF Scan Utility Ver.1.9.0.0." You can download it from the software tab.
 
After one or more unsuccessful printer or driver install attempts, it possible for windows to retain incorrect settings, such as TCP/IP port or WSD information making these resources unavailable to the driver when it tries to install.
 
Last step, software doesn't always remove every piece of a device's installed configuration. You can go a step further and delete the port or WSD information from Device and Printers > Propertes > Ports tab as well.
 
This is a great tool - MS Install / Uninstaller Utility Completely safe, from microsoft and specific for windows. Is similar to the old Revo uninstal utility, but differs in that it corrects installation problems in addition to removing orphaned registry entries.
 
Thank you for the tips. I just spent 75 minutes on the phone with Canon support and the rep had no idea how to fix the problem. Wen't to print managment and removed any instances of Canon. Disabled firewall and antivirus. Tried installing with admin privileges (even though I already had them. Tried installing just the scanner driver. Same error every time with that all in one installer. Nothing helped.
 
No question all of my computers can see the printer on the network. I can put in the IP address and the setup program finds the printer. I don't think lack of a static IP is the issue. The second router (the onhub) is wired behind the Netgear Nighthawk 7000 on a different subnet.
 
The problem is that every time I try the install with the "all in one" program, I immediately get the above message (could not install print driver). After getting off with Canon support, I tried downloading just the print driver ("[Windows 64bit] Generic Plus UFR II Printer Driver V2.10") and it installs. I was able to print a test page.
 
Thanks Rick for showing me where to find the ports section. I don't remember from all the installs and uninstalls of the drivers, but at one point I would see the device listed but there was no way to select properties (I was looking to see if I could print a test page). Anyway, thanks again for your help. Do you work for Canon? If not, they should put you on the payroll.
 
The Universal USB Installer (Imager), also known as UUI, is USB bootable pendrive software. This ISO to USB utility allows you to easily create a multisystem bootable USB from ISO files. It enables you to boot from USB Windows setup installers, Linux operating systems, stand alone Antivirus software, along with several system diagnostic and PC repair tools.

 
Take all your favorite Live Linux distributions, Windows Installers, system recovery, backup, and diagnostic tools with you, capable of booting from one USB drive. The most popular antivirus scanners, disk cloning software, penetration testing, and system diagnostic tools can be stored on and configured to boot from the same single multisystem bootable pendrive. You can even use UUI to fully install, boot, and run Windows 11 entirely from USB.
 
Using this open source USB boot maker software is easy as 123. Simply select your target flash drive, choose your distribution from the list, browse to the ISO file (or choose to download the ISO), and then click Create. Once finished, you should have a ready to run Live USB containing the Live operating system, Windows installer, or system diagnostics utility, or advanced system cleaner tool you previously selected.
 
Some boot from USB tools use simple DD (Disk/Data Duplicator) copy and convert commands to directly burn ISO to USB. The DD method of copying, also commonly referred to as "Data Destroyer" works by overwriting the entire file system on a flash drive with that of a CD or DVD image. This process causes the drive to appear limited to the size of the chosen ISO file which can prevent you from continuing to use the drive for storage purposes. However, if the filesystem used by the CD/DVD image supports expansion, it may be possible to recover lost USB drive space or storage capacity by extending the space and creating another partition to use for storage.
 
UUI offers a more practical method than DD through the use of an exFAT partition for storing bootable ISO files and block images, along with a separate hidden secondary FAT boot partition which is used to boot those files. This method allows your USB drive to appear to Windows as a regular exFAT formatted flash drive and enables you to continue using your removable device for traditional storage purposes.
 
Another key feature of this bootable USB maker is the use of persistent storage, where available. This persistence feature allows you to save changes and then restore those changes on subsequent boots. Ubuntu based Casper persistence works with FAT32, NTFS, or exFAT formatted drives. Starting with version 2.0.1.6, the USB drive is formatted with an exFAT filesystem, so an option to use a larger than 4GB casper-rw or live-rw persistent block file, (also known as an overlay image) is now possible. Currently supporting up to 40GB persistence.
 
Instead of relaunching this Live Linux USB Creator to add more distributions, you can simply drag additional ISO, IMG, WIM, VHD(x), VDI.vtoy, and EFI files from any folder on your computer and drop them onto any folder under the UUI folder on your flash drive. You can also create your own folders within the UUI folder to use for storage. During bootup, the system will automatically populate the menu entries for those newly discovered items.
 
**Important**: UUI will show drives detected by Windows as either removable media (USB Drive) or a fixed (Local Disk). See the recommended list of some of the fastest and best USB flash drives to use with this tool.
 
**WARNING**: You must backup any data you wish to keep before using this tool on any Disk. When choosing the "Prepare this Device" option, all volumes and partitions on the select (Disk #), even if they are hidden, will be wiped clean.
 
You can use the UUI4Linux UUI.sh bash shell script to prepare and make a Multiboot bootable USB from Linux. After the drive is prepared, you can proceed to add ISO distributions and create persistence files by running the Universal-USB-Installer-2.0.2.4.exe executable from WINE.
 
Once finished, the included Universal-USB-Installer-2.0.2.4.exe executable can be run from within WINE to learn more about a distro, download related ISO files, and install additional distributions + create persistence files on any prepared drive.
 
This USB boot maker software allows you to make a custom bootable USB drive from ISO files of the following Live Linux Portable Operating Systems, Windows Installers, Windows PE, System Diagnostic Tools, Cloning Tools, and Antivirus Utilities. Choose from a selection of Windows Installers and popular Live Linux distributions to put on your flash drive. It's easy as 123.
 a2f82b0cb4
 
