# CC3-SpeedBump-V1R1 - TheLittleEngineers.org-CC3-SpeedBump-V1R1-30-MARCH-1987
<html>

<head>
<meta name="GENERATOR" content="Tandy Radio Shack TRS-80 Color Computer 3">
<meta name="ProgId" content="TeleWriter-128">
<meta http-equiv="Content-Type" content="text/html; charset=windows-1252">
<meta http-equiv="Content-Language" content="en-us">

</head>

<body>

<div align="center">
  <center>
  <table border="0" cellpadding="0" cellspacing="4" width="94%">
    <tr>
      <td valign="bottom" colspan="3">
      <p align="center"><font size="6">
      <a href="https://github.com/TheLittleEngineers/CC3-SpeedBump-V1R1" target="_blank">CC3-SpeedBump-V1R1</a> - 
      <a href="https://oshpark.com/shared_projects/ZUfVJGEa" target="_blank">TheLittleEngineers.org-CC3-SpeedBump-V1R1-30-MARCH-1987</a><br></font>
      <font size="5"><em>
      <a href="http://www.TheLittleEngineers.org/files/html/pages/CC3-SpeedBump-V1R1.htm" target="_blank">SpeedBump</a> - A Hardware Project For The Tandy Radio Shack TRS-80 Color Computer 3</em><br></font><font size="4">A 
      <a href="http://www.TheLittleEngineers.org/files/html/pages/CC3-SpeedBump-V1R1.htm" target="_blank">Project</a> By <a href="http://www.TheLittleEngineers.org/" target="_blank">
The Little Engineers</a>.<br>Copyright &copy;2019, by:<br>
Robert "The R.A.T." Allen Turner<br>
<a href="http://www.TheLittleEngineers.org/" target="_blank">http://www.TheLittleEngineers.org/</a><br>
<a href="mailto:TheLittleEngineers@outlook.com">TheLittleEngineers@outlook.com</a><br>
<a href="mailto:OurLittleEngineers@gMail.com">OurLittleEngineers@gMail.com</a></font><hr><font size="4">
<p align="justify">This product, 
<a href="https://github.com/TheLittleEngineers/CC3-SpeedBump-V1R1" target="_blank">TheLittleEngineers.org-CC3-SpeedBump-V1R1-30-MARCH-1987</a>, is intended to add the old TRS80 Color Computer 1 and 2 High-Speed POKE back to the Tandy Color Computer 3, in hardware.</p>
      <hr>
<p align="center">
<a href="http://www.TheLittleEngineers.org/files/html/pages/CC3-SpeedBump-V1R1.htm" target="_blank">SpeedBump</a> - A 
<a href="http://www.TheLittleEngineers.org/files/html/pages/CC3-SpeedBump-V1R1.htm" target="_blank">Hardware</a>
<a href="http://www.TheLittleEngineers.org/files/html/pages/CC3-SpeedBump-V1R1.htm" target="_blank">Project</a> For The Tandy Radio Shack TRS-80 Color Computer 3 by 
<b>"Ankle" Bob</b> <i>a.k.a.</i> <b>&quot;The R.A.T.&quot;</b></p>
<p align="justify">This is a relatively simple project to restore, to an extent, the 
<i>Color Computer 1 and 2</i> <b>high-speed POKE</b> to the <i>Tandy Color Computer 3</i>. Some might consider this to be a bit of folly, after all,
<b>"Doesn't the Color Computer 3 possess a superior high-speed POKE?"</b> <i>Yes, indeed it does.</i> However, one of the very first things that I noticed about my newly acquired
<i>CoCo 3</i>, circa 1986, was the fact that the old <b>high-speed POKE</b> <i>no longer functioned</i>. This had the effect of rendering some of my favorite programs, such as
<b>"Paint King"</b>, unusable, or nearly so. Now, it was a very simple matter to patch 
<b>"Paint King"</b> and similar <b>BASIC</b> and <i>unprotected</i> programs by simply substituting the 
<b>new POKE</b> for the <b>old</b>. In fact, this actually <i>improved</i> the functionality of programs such as
<b>"Paint King"</b>. This was due to the <i>CoCo 3</i> <b>high-speed POKE NOT BEING ADDRESS DEPENDENT</b>, as it was on the
<i>CoCo 1 and 2</i>. Many <i>machine-language and "protected"</i> programs proved difficult, and in some cases, 
<i>impossible</i> to patch. After wasting many hours with a <b>"Disk Zapper"</b>, hacking and patching, I set about to solve the problem, once and for all, in hardware. In theory, at least, it should be quite possible and simple enough to socket the 
<b>MC68B09E</b> <b>CPU</b> and stick a circuit between the <b>CPU</b> and the rest of the system to monitor the 
<b>Address Buss</b> and pass all addresses straight through, <i>EXCEPT</i> for the 
<b>old high/slow-speed POKE addresses</b>. The <b>old high/slow-speed POKE addresses</b> would be 
<i>modified</i> (<i>converted</i> to the N<b>EW high/slow-speed addresses</b>) and passed through as the 
<b>new addresses</b>. Thanks to the amazingly versatile (at the time) <b>PALs</b> and 
<b>PLDs</b> of the <i>era</i>, <b>this is exactly what I did.</b> Two <b>PLD/PALs 
from MMI</b> provided an elegant <i>two chip</i> solution. And so, this circuit 
board sat in one of my <i>CoCo 3's</i> for decades, until such time as I passed 
my <i>vintage computing and electronics collection</i> on to my brother, <b>J.R. 
(John Robert)</b> who then passed it on to his son, <b>J.E. (John Eric or 
&quot;Little John&quot;).</b></p>
      <hr>
<p align="justify">A request from my <i>nephew</i>, <i>"Little John"</i>, prompted me, in part, to redesign the device utilizing a single 
<b>22V10 GAL</b>. This was a desirable decision due to the scarcity of the older
<b>PLD</b> and <b>PAL</b> devices and the fact that often, when purchased, <i>the older devices have already been programmed</i>. Being 
<i>fusible link based devices</i>, this renders them <i>unusable</i> and <i>completely useless</i>. A 
<b>GAL</b> chip is also much faster and <i>flash-based (reusable)</i> with some offering 
<i><b>I</b>n <b>S</b>ystem <b>P</b>rogramming</i> (such as the <b>ISPGAL22V10</b> from 
<i>Lattice</i>.) The <b>ISP</b> version is not used here, as they are a bit difficult to obtain, so you'll need a 
<i>GAL programmer</i> to complete this project, or at least access to one. The 
<b>g22v10d</b> is recommended due to its higher speed than the <i>&quot;plain vanilla&quot;</i>
<b>g22v10</b>, although it should work as well. The <b>A, B</b> and <b>C</b> versions could 
also be used. The <b>CUPL</b> <i>code</i> is <i>self-explanatory</i> and this truly is a very simple device. Note that the 
<b>two old addresses</b> are simply converted to the <b>two new addresses</b>. This effectively restores the 
<b>old high-speed POKE</b> with the <i>exception</i> that the machine will run at 
<b>1.79MHz</b> at all times when the <b>POKE</b> is enabled. This is in contrast to the
<i>CoCo 1 and 2</i>, which only ran at <b>1.79MHz</b> during access to the <b>ROM</b> area (<b>0x8000 
- 0xFEFF</b>) and only if the <b>ROMs</b> were enabled and also at a small section of 
<b>I/O addresses</b>. It ran at <b>.89MHz</b> for accesses to the lower <b>32K (RAM area).</b> 
If the machine were a <b>64K RAM</b> machine running in <b>All RAM mode</b>, it would stay at 
<b>.89MHz</b> during accesses to the <b>0x8000-0xFEFF</b> area as well. In short, the 
<b>old high speed POKE</b> <i>only functioned if the</i> <b>BASIC ROMs</b> <i>were in circuit and being executed by the</i>
<b>CPU</b> <i>(using the original</i> <b>74LS783/MC6883 S.A.M.</b> - <i>later versions of the</i>
<b>MC6883</b> <i>and all versions of the</i> <b>74LS785</b> <i>allowed the address dependent mode to function while in</i>
<b>"ALL-RAM"</b> <i>mode as well).</i> This version, the 
<a href="http://www.TheLittleEngineers.org/files/html/pages/CC3-SpeedBump-V1R1.htm" target="_blank">CC3-SpeedBump-V1R1-30-MARCH-1987</a> is licensed under a <a href="https://creativecommons.org/licenses/by-sa/4.0/" target="_blank">Creative Commons Attribution-ShareAlike 4.0 International</a> (<a href="https://creativecommons.org/licenses/by-sa/4.0/legalcode" target="_blank">CC BY-SA 4.0</a>) License.</p>
<p align="justify">There is an
<a href="https://oshpark.com/shared_projects/ZUfVJGEa" target="_blank">OSHPark</a>
<a href="https://oshpark.com/shared_projects/ZUfVJGEa" target="_blank">Page</a> for this project here: <a href="https://oshpark.com/shared_projects/ZUfVJGEa">https://oshpark.com/shared_projects/ZUfVJGEa</a>.</p>
<p align="justify">This design should be thoroughly scrutinized and verified prior to actual use of any kind. 
<b>DISCLAIMER:</b> The following article is provided for informational purposes only. Any attempt to modify your computer without the proper skills to do so may void your computer. Any attempt to modify your computer without unplugging it first may void you. This Information is provided 
<b>"as-is"</b> with no guarantee of fitness for any purpose, either explicit or implied. We disclaim any and all responsibility for losses incurred through the use of this information. By using this information, you are deemed to have accepted these conditions of use, and 
<b>you agree NOT to sue us</b>. <b>CLARIFICATION:</b> The above disclaimer states as plainly as possible that if you decide to make use of any of the information contained within this document that you do so at your own risk. Designing hardware for the
<b>CoCo</b> <i>(<b>Co</b>lor<b>Co</b>mputer)</i> and other vintage hardware is a 
hobby of ours and is not motivated by any desire of profits. As this is a not 
for profit venture, obviously we can't afford not to disclaim the use of this 
information.</p>
<p align="center"><u><b>PLEASE NOTE: THIS VERSION HAS NOT YET BEEN TESTED.</b></u> 

</p>
<hr align="justify">
<p align="justify"><a href="https://github.com/TheLittleEngineers/" target="_blank">The Little Engineers</a> is a project began in 2011 by Robert Allen Turner (hereafter, I or Me), for the benefit of foster children and their families (foster and biological). The original intent was simply to provide a means of creating videos with the foster families such that the biological parents did not completely miss out on their children growing up. Providing simple to construct kits seemed a logical choice as a subject for such videos and that is primarily what I attempt to develop for use in such videos. This also makes the process educational. This is a difficult undertaking, as each case must be handled on an individual basis and any such videos and communications must be scrutinized and approved on a per case basis by the case workers, et alia in charge. Although this makes such an undertaking extremely difficult, it is a necessity in order to protect the children. Some are, after all, being protected from abusive family members and so on. So there has to be a very strict set of protocols in place. This has prevented me from fully launching 
<a href="http://www.TheLittleEngineers.org/" target="_blank">The Little Engineers</a> over the past eight years, but I remain committed to the project.</p>
<p align="justify">The logos, names and other material relating to 
<a href="http://www.TheLittleEngineers.org/" target="_blank">The Little Engineers</a>,
<a href="http://www.TheLittleEngineers.org/" target="_blank">TheLittleEngineers.org</a> and 
<a href="http://www.GIMEchip.com/" target="_blank">GIMEchip.com</a> are the sole property of Robert Allen Turner with All Rights Reserved. The rights to the 
<a href="http://www.GIMEchip.com/" target="_blank">GIMEchip.com</a> domain and products were acquired by the author on 25 December 2018. Merry Happy Christmas! Please note that the author is unable to answer any inquiries, including those of support or otherwise, in relation to 
<a href="http://www.GIMEchip.com/" target="_blank">GIMEchip.com</a> prior to his acquisition of same on 25 December 2018. 
As part of the acquisition agreement, all products previously produced by 
GIMEchip.com are being released under a <a href="https://creativecommons.org/licenses/by-sa/4.0/" target="_blank">Creative Commons Attribution-ShareAlike 4.0 International</a> (<a href="https://creativecommons.org/licenses/by-sa/4.0/legalcode" target="_blank">CC BY-SA 4.0</a>) 
License, as time and resources permit.</p>
<p align="center"><a href="http://www.TheLittleEngineers.org/" target="_blank">http://www.TheLittleEngineers.org</a>
</p>
<p align="justify">Please note: This product is derived from an original design by "Uncle/Ankle" Robert 
&quot;The R.A.T.&quot; Allen Turner. It should be thoroughly scrutinized and verified prior to actual use of any kind. 
<b>DISCLAIMER:</b> This article is provided for informational purposes only. Any attempt to modify your computer without the proper skills to do so may void your computer. Any attempt to modify your computer without unplugging it first may void you. This Information is provided "as-is" with no guarantee of fitness for any purpose, either explicit or implied. We disclaim any and all responsibility for losses incurred through the use of this information. By using this information, you are deemed to have accepted these conditions of use, and 
<u><i>you agree NOT to sue us</i></u>. 
<b>CLARIFICATION: </b>The above disclaimer states as plainly as possible that if you decide to make use of any of the information contained within this document that you do so at 
<i>your own risk.</i> Designing hardware for the <b>CoCo</b> <i>(<b>Co</b>lor<b>Co</b>mputer)</i> and other vintage hardware is a hobby of ours and is not motivated by any desire of profits. As this is a not for profit venture, obviously we can't afford not to disclaim the use of this information.<br>
&nbsp;</p>
<p align="center">
<u>
<b><em>
PLEASE NOTE: THIS VERSION HAS NOT YET BEEN TESTED.</em></b> </u>
<br>
I have ordered PCBs (Printed Circuit Boards) and will update this project after 
testing is complete.</p>

<hr>

</font></td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td valign="top" width="48%">
      <p align="justify"><font size="3">This repository and/or publication may contain one or more C.A.D. Libraries, such as for E.A.G.L.E., KiCAD, etcetera. You may use these libraries in your own projects,  however, please take note that we CANNOT guarantee the accuracy of the components (nor any part of these libraries and/or publications). We make NO guarantees that the components, footprints or schematic symbols contained in these libraries are flawless, and we make no promises of fitness for production, prototyping or any other purpose. These libraries and/or publications are provided for informational purposes only, and are used at your own discretion. By downloading these libraries 
      and/or publications, you agree that we cannot be held responsible for faulty PCBs (Printed Circuit Boards). You should always check the footprints with a 1:1 printout. Neither Robert Allen Turner, <a href="http://www.TheLittleEngineers.org/" target="_blank">The Little Engineers</a>, <a href="http://www.TheLittleEngineers.org/" target="_blank">TheLittleEngineers.org,</a> <a href="http://www.GIMEchip.com/" target="_blank">GIMEchip.com</a>, nor anyone affiliated with same shall be held responsible for any outcome resulting from the usage of these files. Should any errors be found, please contact us at one of the above email addresses and we will attempt to repair them. Unless otherwise noted, content of this library is licensed under a <a href="https://creativecommons.org/licenses/by-sa/4.0/" target="_blank">Creative Commons Attribution-ShareAlike 4.0 International</a> 
      <a href="%20https:/creativecommons.org/licenses/by-sa/4.0/legalcode" target="_blank">(CC BY-SA 4.0)</a> License on 04 Junel 2019 in memory of my Father, Robert Embry Turner, 1945-2019 - I LOVE AND MISS YOU DAD! Rest In Peace.
      </p>
     <hr align="justify">
      <p align="justify">The following text serves as a general <i>Introduction</i> to Robert "The R.A.T." Allen Turner, Zombie Software Systems, Binary Systems, <a href="http://www.GIMEchip.com/" target="_blank">GIMEchip.com</a> and <a href="http://www.TheLittleEngineers.org/" target="_blank">The Little Engineers</a> (<a href="http://www.TheLittleEngineers.org/" target="_blank">http://www.TheLittleEngineers.org/</a>). Please note that the <a href="http://www.GIMEchip.com/" target="_blank">GIMEchip.com</a> domain was acquired by Robert "The R.A.T." Allen Turner on December 25, 2018 from the prior owners, which happen to be his brother (J.R. a.k.a. John Robert a.k.a. "Big John") and nephew (J.E. a.k.a. John Eric a.k.a. "Little John"). As such, "The R.A.T." is unable to answer any inquiries regarding any products or services of <a href="http://www.GIMEchip.com/" target="_blank">GIMEchip.com</a> prior to that date. "The R.A.T." has also acquired the rights to all products previously produced by <a href="http://www.GIMEchip.com/" target="_blank">GIMEchip.com</a> and its previous owners. As part of the acquisition agreement, all of those products will be released as open source, under a <a href="https://creativecommons.org/licenses/by-sa/4.0/" target="_blank">Creative Commons Attribution-ShareAlike 4.0 International</a> 
      <a href="https:/creativecommons.org/licenses/by-sa/4.0/legalcode" target="_blank">(CC BY-SA 4.0)</a> License, as time and resources permit.</p>
      <p align="justify"><b>Introducing "The R.A.T.": </b>I have started 
writing this introduction numerous times only to get sidetracked and derailed. Hopefully, I 
will be able to  properly introduce myself this time. I will start at the beginning of my 
computer usage. This would be March 30, 1982. My fourteenth birthday. My parents presented 
me with a <b>Timex Sinclair 1000 (TS1000)</b> computer, after much begging and pleading. The 
<b>TS1000</b> is a <b>ZX81</b> with a few differences: 2K of RAM, an [ENTER] key instead of 
[NEW LINE] or [N/L] and Timex branding. I had wanted a computer for so long, and <b>Sir Clive 
Sinclair</b> succeeded in making it affordable. Timex made it even more affordable as the 
<b>TS1000</b> was placed on sale for $59.99 at the local "Big B" drug store, at the time, a 
division of Brunos Corporation (Food World, Food Fair, Consumer Warehouse, etcetera). I was 
ectstatic - I finally had a computer, limited as it was, I still learned a great deal from 
that machine and it led to the creation of <b>Zombie Software Systems</b>, my first computer 
venture. When Timex announced the <b>Timex Sinclair 2068 (TS2068)</b> after canceling the 
<b>TS2000</b> (a <b>48K Spectrum</b> clone), I knew that I wanted it to be my next computer 
and my parents agreed to buy it for me for Christmas of 1983. Then, it happened: I walked 
into the local franchised Radio Shack store, operated at the time by Cisco Auto Parts, and 
there, on display right next to the entrance, was the newly introduced <b>Color Computer 2 
with 16K and Extended Color BASIC</b>. It took mere moments for me to fall in love with that 
machine and I asked my parents for the <b>Color Computer 2</b> instead of the <b>TS2068</b>. 
They placed it on lay-a-way as Christmas approached. It was eventually paid off and sat under 
the Christmas tree until Christmas Evening of 1983. They allowed me to open it on Christmas 
Evening and I was up all night working through the programs in the manuals. It was wonderful. 
This led to the creation of <b>Binary Systems</b>, my second computer venture. Eventually, I 
came across an advertisement in Radio-Electronics from a company by the name of Unicorn 
Electronics. They had a set of 4164 Dynamic RAM chips with a 150nS access time for, I think 
$9.95. The chips were used but tested. I ordered them, along with a bag of keyboard switches 
(intended to be used for buildinmg a better keyboard for my <b>TS1000</b>). When they arrived, 
I opened the case of my <b>Color Computer 2</b>, installed the 64K chips, soldered in the W1 
jumper and voila - I had a <b>64K ECB Color Computer 2</b>. Although other systems of the 
time had better graphics and sound, the <b>Color Computer</b> line of systems by Radio Shack, 
a division of Tandy Corporation, would become (and remain) my favorite computers of all time. 
In fact, I still use them to this very day, having kept one <b>Color Computer 3 (CoCo 3)</b> 
when I passed my vintage computing collection to my brother, J.R. (John Robert) who then passed 
it on to his son, "Little John" (John Eric), but I will get to that after a brief reminiscence 
of <b>ZSS</b> and <b>BS</b>, as follows:<br><b><center>ZSS or Zombie Software 
      Systems:</center>
      <p align="justify">Zombie Software Systems</b> was formed on my fourteenth birthday, 30 March 1982, as a sole 
proprietorship supporting the Timex and Sinclair computer systems. Supported systems initially 
included:</p>
      <ul>
<li>
<p align="justify">Sinclair ZX80</li>
<li>
<p align="justify">Sinclair ZX81</li>
<li>
<p align="justify">Timex Sinclair 1000</li></ul>
      <p align="justify">Support was eventually added for:</p>
      <ul>
<li>
<p align="justify">Timex Sinclair 1500</li>
<li>
<p align="justify">The PC-8300 "Your Computer"</li>
<li>
<p align="justify">Sinclair Spectrum (All Versions)</li>
<li>
<p align="justify">Timex Sinclair 2068</li>
<li>
<p align="justify">Sinclair QL</li></ul>
      <p align="justify">By 1991, and in conjunction with Binary Systems, support had been added for machines from Mattel, 
Atari, Tomy, Texas Instruments, Tandy Radio Shack, Commodore and many others.<br><br><b>
      </p>
      <center>
BS or Binary Systems:</center>
      <p align="justify">Binary Systems</b> was formed on 23 December 1983, as a sole 
proprietorship supporting the Tandy Radio Shack computer systems. Supported systems initially 
included:</p>
      <ul>
<li>
<p align="justify">TRS-80 Color Computer (CoCo 1)</li>
<li>
<p align="justify">Tandy Data Products TDP-100</li>
<li>
<p align="justify">TRS-80 Color Computer 2 (CoCo 2)</li>
<li>
<p align="justify">Dragon Data Dragon 32</li>
<li>
<p align="justify">Tano Dragon 64</li>
<li>
<p align="justify">TRS-80 Model I</li></ul>
      <p align="justify">Support was eventually added for:</p>
      <ul>
<li>
<p align="justify">TRS-80 Model III</li>
<li>
<p align="justify">TRS-80 Model IV</li>
<li>
<p align="justify">TRS-80 Model 4/4P</li>
<li>
<p align="justify">Tandy Color Computer 3</li></ul>
      <p align="justify">By 1991, and in conjunction with Zombie Software Systems, support had been added for machines from 
Mattel, Atari, Tomy, Texas Instruments, Sinclair, Commodore, Amstrad, Kaypro and many others. The 
operation of <b>Zombie Software Systems</b> and <b>Binary Systems</b> was a <b>labor of love</b> 
more than anything else, as it never made a profit, but it was fun and remains among the best 
memories of my youth and early adulthood and I am thankful that the stroke (see below) did not take 
these memories from me.<hr align="justify">
      <p align="justify">I continued to support these vintage machines until 2007 when I suffered 
a stroke. At that point, I passed operations on to my son, John (he and his cousin share both the 
same name and same date of birth through a very odd coincidence). My son eventually made a mess of 
things and finally moved on to other hobbies. A side effect of the stroke was that I lost 
      almost all 
interest in computers and electronics, vintage and otherwise. It was thus that I presented my entire 
collection of vintage computers and electronics to my brother J.R. (John Robert or "Big John"). He 
took the opportunity to bond with his son, J.E. (John Eric or "Little John"). "Little John" was 
facing a number of health issues, but he jumped in with both feet, teaching himself all about the 
<b>Color Computer</b> and other systems. He began to develop a plethora of hardware projects for the 
<b>Color Computer</b> and other vintage systems. The earliest of his designs were rubbish due to his 
lack of skill, but he appears to have learned rather quickly, producing some amazing designs. I have 
taken it upon myself to "redo" his earliest works, hopefully producing manufacturable products from 
them. The first of his designs to receive the "redesign" treatment from me is the "FlexiMIDI", 
"FlexiROM" and &quot;FlexiBuffer&quot; projects. Those three designs were excellent in concept, but rubbish in practice due to his 
lack of circuit design skills at the time that he developed them. They are certainly worth the time 
and effort to redesign. He would eventually become disillusioned and abandon the hobby altogether. 
This was, in no small part, due to hackers repeatedly taking down his website: 
<a href="http://www.GIMEchip.com/" target="_blank">GIMEchip.com</a>. They (the unknown hackers) eventually compromised 
his eBay and PayPal accounts, rendering them completely useless. That was the straw that broke the 
camels back, so to speak. He ("Little John") gave up and moved to Tennessee. He left everything with 
his father, my brother, and asked that his father release all of his works as open source. J.R. made 
several valiant efforts to honor that request, but never fully succeeded in releasing all of the works 
of "Little John". Fast Forward almost a decade...<hr align="justify">
      <p align="justify"><b>The Beginning of a Family Tragedy:</b><br>November of 2018, my father fell ill and was hospitalized. 
As Christmas approached, he remained in the hospital. Many family members visited and it came to pass 
that I reconnected with J.R. and "Little John". They asked me if I would like to have my old vintage 
computing collection back. At first, I was hesitant and uninterested. As my fathers condition worsened, 
I began to remember how hard my father worked to buy me those first computers. Tons of memories, good 
and bad, began to flood my mind. I decided to accept their offer. In addition to the hardware and 
software, they presented me with the <a href="http://www.GIMEchip.com/" target="_blank">GIMEchip.com</a> domain name. 
This became my Christmas present from my brother and his son. "Little John" asked that I finish what 
his father started: <i>the release of all of "Little John's" work as open source</i>. I reluctantly 
agreed, though I was unsure if I could ever manage the time and effort to do so. I honestly was not 
prepared to take on such a monumental task. Then, <b>tragedy</b> struck.<br></td>
      <td width="4%"></td>
      <td valign="top" width="48%">
      <p align="justify">On the day of 
January 4, 2019, my father died as I held his hand in that hospital room. His death had quite a profound 
effect on me. I almost lost my job while trying to come to terms with never being able to speak to my father 
again. I eventually began to recover, to an extent, but I began to think of everything and everyone that I 
had lost over the years. For one thing, my own son, also named John Eric Turner, and I are estranged. We 
"speak" online, but I have not seen him in a very long time. He was unable to be at the hospital and did 
not get to say goodbye to my father before he died. As mentioned, my son and his cousin are both named 
John Eric Turner, and there is a story behind it, however, for the moment, suffice it to say that they 
both were named In Memory of Jon-Erik Hexum, who died on the set of "Cover Up" on Friday, October 12, 
1984. As my mind wandered, I thought of my mother in law, Sarah Ann Channell, who passed away on 
January 12, 2003 and my father in law, Frank Leon Channell, who passed away on August 23, 2003. Even 
though I was divorced from their daughter, they were still family and their deaths were very painful to 
me and my son. Indeed, their deaths affected my son in such a way that he never fully recovered and that 
is partially what eventually led to our falling out in 2007 or 2008 and the resulting estrangement. I am 
sure that my addled state after that stroke also played a hand in the troubles between my son 
and I because I became very difficult to be around. Thinking about Sarah and Frank caused me to really 
begin missing my son and, even more, my father. I then thought about my best friend from high school, 
David Ray Poe, who died on May 20, 2013. Eight days prior to his death, he had sent me an email that I 
did not see until after he died. That email was a single sentence: "Did you die?". You can perhaps imagine 
the effect that reading the message had on me. In reality, he would often send a message like that when he 
had not heard from me in a while. Another close friend from high school, Steve Allen 
      Cox, died on September 
6, 2016. As all of the thoughts of everything and everyone that I had lost flooded my mind, I began to 
spiral and was in peril of losing myself. I needed a distraction, something to keep my mind occupied and 
perhaps aid in my coming to terms with the death of my father. I found that distraction in the form of that 
vintage computing collection and the projects that "Little John" had created. It is for that reason alone 
that you are now reading this and seeing those products, which I have decided to release under a 
<a href="https://creativecommons.org/licenses/by-sa/4.0/" target="_blank">Creative Commons Attribution-ShareAlike 4.0 
International</a> 
      <a href="https:/creativecommons.org/licenses/by-sa/4.0/legalcode" target="_blank">(CC BY-SA 4.0)</a> 
      License. What this means is that you, or anyone else for that matter, may use the products in almost any 
way that you may desire, even commercially. I am doing all of this to honor the memory of my father, Robert 
Embry Turner, and everyone else that I have lost. I truly hope that these products provide much enjoyment 
to all who discover them. I should point out that I have absolutely no desire to revive the 
<a href="http://www.GIMEchip.com/" target="_blank">GIMEchip.com</a> website, primarily because I do not have all of the 
files necessary to recreate <a href="http://www.GIMEchip.com/" target="_blank">GIMEchip.com</a>. It is very likely that I 
will stumble across some or all of the <a href="http://www.GIMEchip.com/" target="_blank">GIMEchip.com</a> website files as 
I begin to inventory everything that was included with my 2018 Christmas gift from "Big and Little John". I 
also <b>DO NOT</b> wish to invoke the ire of those hackers who targeted my nephew and destroyed his website, 
eBay and PayPal accounts. I will very likely, however, forward the <a href="http://www.GIMEchip.com/" target="_blank">
GIMEchip.com</a> domain to a page on my <a href="http://www.TheLittleEngineers.org/" target="_blank">
http://www.TheLittleEngineers.org/</a> <a href="https://www.facebook.com/OurLittleEngineers/" target="_blank">website</a> 
or perhaps I will forward it to the <a href="https://github.com/TheLittleEngineers?tab=repositories" target="_blank">GitHub
</a> page - I am currently undecided.<br><br>So, there you have it - most of what I wanted to say about how I 
came to posses all of the works of my nephew and his father, as well as their domain name, 
<a href="http://www.GIMEchip.com/" target="_blank">GIMEchip.com</a>. In addition to releasing all of their products under a 
<a href="https://creativecommons.org/licenses/by-sa/4.0/" target="_blank">Creative Commons Attribution-ShareAlike 4.0 
International</a> 
      <a href="%20https:/creativecommons.org/licenses/by-sa/4.0/legalcode" target="_blank">(CC BY-SA 4.0)</a> 
License, I will also be releasing all of the <b>Zombie Software Systems</b> and <b>Binary Systems</b> 
products under <a href="https://creativecommons.org/licenses/by-sa/4.0/" target="_blank">identical</a> 
<a href="%20https:/creativecommons.org/licenses/by-sa/4.0/legalcode" target="_blank">licensing</a> 
<a href="https://creativecommons.org/licenses/by-sa/4.0/" target="_blank">terms</a>.</p>
      <p align="justify"></p>
      <hr align="justify">
      <p align="justify"><b>Is ALL of this really FREE?</b> 	YES! Everything 
      contained in the GitHub Repositories for these projects is free to use, 
      even commercially, in accordance with the terms of the <a href="https://creativecommons.org/licenses/by-sa/4.0/" target="_blank">Creative Commons 
Attribution-ShareAlike 4.0 International</a> 
<a href="%20https:/creativecommons.org/licenses/by-sa/4.0/legalcode" target="_blank">(CC BY-SA 4.0)</a> License. 
      The Amazon Kindle and Paperback Publications, however, are not licensed 
      for redistribution and are only available to our <a href="https://www.patreon.com/rss/TheLittleEngineers?auth=Lf2lxAb1hC7CqtfFqcd47ysxUUx_8AvY" target="_blank">Patrons</a>
	   as a free ".PDF" or for purchase from Amazon. These 
      particular publications help to generate revenue that is used for further 
      developmental efforts. It is not necessary to purchase these publications 
      in order to make use of the GitHub Repositories, however, such purchases 
      provide the funds necessary for the development of future products. The 
      repositories contain all necessary information needed to construct, 
      assemble and use the products described therein. If you would like to 
      support our continued developmental efforts, the remaining paragraphs 
      detail several methods that may be used to offer support of our work.
      <p align="justify">As stated, I have 
absolutely <b>no intention</b> of charging any fees whatsoever in regards to the use of these products. 
Anyone who so desires may manufacture and sell any of these products, though they must state specifically 
that they will be providing any and all support as may be required. However, If you would care to support my 
work, donations are happily accepted, whether they be in the form of funds, vintage computing equipment, 
tools, components, etcetera. I am always in need of such items. I specifically need PAL versions of the TRS80 
Color Computer series (1,2 and 3) as well as NTSC/PAL Dragon D32, D64, D200, etcetera for developmental 
purposes. Monetary donations help to support the hosting needs of 
<a href="http://www.TheLittleEngineers.org/" target="_blank">http://www.TheLittleEngineers.org/</a> as well as the 
development and manufacture of the prototype Printed Circuit Boards.<br><br>Perhaps the easiest and most 
beneficial method of supporting <a href="http://www.TheLittleEngineers.org" target="_blank">The Little Engineers</a> 
(monetarily) would be by becoming a 
<a href="https://www.patreon.com/rss/TheLittleEngineers?auth=Lf2lxAb1hC7CqtfFqcd47ysxUUx_8AvY" target="_blank">Patron</a> on 
<a href="https://www.patreon.com/rss/TheLittleEngineers?auth=Lf2lxAb1hC7CqtfFqcd47ysxUUx_8AvY" target="_blank">Patreon</a> 
The following are among the benefits offered to 
<a href="https://www.patreon.com/rss/TheLittleEngineers?auth=Lf2lxAb1hC7CqtfFqcd47ysxUUx_8AvY" target="_blank">Patrons</a>.
<a href="https://www.patreon.com/rss/TheLittleEngineers?auth=Lf2lxAb1hC7CqtfFqcd47ysxUUx_8AvY" target="_blank">Patrons</a> will 
receive several exclusive benefits, such as:<br><ul>
<li>
<p align="justify">FREE copies of ANY of our detailed Theory of Operation and Assembly 
<a href="https://www.amazon.com/Robert-Allen-Turner/e/B07K5L5HW9" target="_blank">e-books</a> relating to our projects.</li> 
<li>
<p align="justify">Random giveaways of bare Printed Circuit Boards (PCB's) developed by 
<a href="http://www.TheLittleEngineers.org" target="_blank">The Little Engineers</a>.</li>
<li>
<p align="justify">Random giveaways of Kits developed by 
<a href="http://www.TheLittleEngineers.org" target="_blank">The Little Engineers</a>.</li>
<li>
<p align="justify">Random giveaways of assembled projects developed by 
<a href="http://www.TheLittleEngineers.org" target="_blank">The Little Engineers</a>.</li>
<li>
<p align="justify">The opportunity to purchase various bare Printed Circuit Boards (PCB's) developed by 
<a href="http://www.TheLittleEngineers.org" target="_blank">The Little Engineers</a> at discounts of up to 50% off.</li>
<li>
<p align="justify">The opportunity to purchase various Kits developed by 
<a href="http://www.TheLittleEngineers.org" target="_blank">The Little Engineers</a> at discounts of up to 50% off.</li>
<li>
<p align="justify">The opportunity to purchase various assembled projects developed by 
<a href="http://www.TheLittleEngineers.org" target="_blank">The Little Engineers</a> at discounts of up to 50% off.</li>
</ul>
      <p align="justify">A plethora of other benefits will be added exclusively for 
<a href="https://www.patreon.com/rss/TheLittleEngineers?auth=Lf2lxAb1hC7CqtfFqcd47ysxUUx_8AvY" target="_blank">Patrons</a> as 
time and resources allow. Remember, however, that NO donations are required to access the 
<a href="https://github.com/TheLittleEngineers/" target="_blank">project</a> 
<a href="https://github.com/TheLittleEngineers?tab=repositories" target="_blank">repositories</a> which are available to all 
for FREE.<</p>
      <p align="justify">Another method of making monetary donations is the use of the 
<a href="https://www.facebook.com/OurLittleEngineers/" target="_blank">FaceBook</a> 
<a href="https://www.facebook.com/TheLittleEngineers.org" target="_blank">Messenger</a> 
<a href="https://www.facebook.com/groups/985537051651794/" target="_blank">Payment</a> 
<a href="https://www.facebook.com/OurLittleEngineers/" target="_blank">App</a>. 
<a href="http://www.TheLittleEngineers.org" target="_blank">The Little Engineers</a> may be found on 
<a href="https://www.facebook.com/OurLittleEngineers/" target="_blank">FaceBook</a> at the following urls:<br>
<a href="https://www.facebook.com/profile.php?id=100036295840711" target="_blank">
https://www.facebook.com/profile.php?id=100036295840711</a><br>
<a href="https://www.facebook.com/TheLittleEngineers.org" target="_blank">https://www.facebook.com/TheLittleEngineers.org</a>
<br><a href="https://www.facebook.com/OurLittleEngineers/" target="_blank">https://www.facebook.com/OurLittleEngineers/</a>
<br><a href="https://www.facebook.com/groups/985537051651794/" target="_blank">
https://www.facebook.com/groups/985537051651794/</a><br>
We will also be publishing detailed Theory of Operation and assembly manuals for all of our open source 
products in e-book and paperback formats. Purchases of these e-books and/or paperbacks helps to 
support <a href="http://www.TheLittleEngineers.org" target="_blank">The Little Engineers</a> and our continued developmental 
efforts. Donations may also be made in almost any variety of digital currency, including, but not limited to, 
the following:<br><ul>
<li>
<p align="justify">BitCoin (BTC):<br>18C75HESRUSQX7TUZycEiRUBG6wVpqANVv</li>
<li>
<p align="justify">Ethereum (ETH) or any Ethereum based tokens:<br>0x1374528109EDd54ecC2db6F4Ec29a2f520463499</li>
<li>
<p align="justify">BitCoin Cash (BCH):<br>qpu25q42e9zpqc7mx5r0l3yvftw7ezp37v7899c4x6</li>
<li>
<p align="justify">BitCoin Gold (BTG):<br>GRaxchWNUQGcnHaZa3e1guS5HmCakRFpZ3</li>
<li>
<p align="justify">BitCoin SV (BSV):<br>qr7nkqqu83z0k8mx92s76kku48ulnr5jcup06aj4wy</li>
<li>
<p align="justify">LiteCoin (LTC):<br>LdqZaNopx5xVbBZJcQqRRzX9rJhWstgKwp</li>
<li>
<p align="justify">Ethereum Classic (ETC) including any ETC Tokens:<br>0xd9518F33E822eea56FBE8aA0bcEffFbbfa2456C7</li>
<li>
<p align="justify">Stellar Lumens (XLM):<br>GAXIJLUY7NSDAN22TSSYZKIWSBVM5OS5KVTY7MGR6I7PXFTS7U3JK3YV</li>
<li>
<p align="justify">Ripple (XRP):<br>r3dMH6J596vV1LqSMB62ewuuWtsuhdWaoL</li></ul>
      <p align="justify">Should you wish to use digital currency, I highly recommend checking out this referral link: 
<a href="https://www.coinbase.com/join/5a42ff8478e76b05ef28e185" target="_blank">Digital Currency.</a> Signing up from 
that link also helps <a href="http://www.TheLittleEngineers.org" target="_blank">The Little Engineers</a> in the long run. 
If you would like to make a donation by some other means, feel free to contact me by 
<a href="mailto:TheLittleEngineers@outlook.com">e-mail</a> or 
<a href="https://www.facebook.com/profile.php?id=100036295840711" target="_blank">FaceBook</a> 
<a href="https://www.facebook.com/OurLittleEngineers/" target="_blank">Messenger</a>. Please note, however, that donations 
are completely optional, but they do help to further product development. All products developed by 
<a href="http://www.TheLittleEngineers.org" target="_blank">The Little Engineers</a> are completely free to use under the 
terms of the <a href="https://creativecommons.org/licenses/by-sa/4.0/" target="_blank">Creative Commons Attribution-ShareAlike 
4.0 International</a> 
      <a href="%20https:/creativecommons.org/licenses/by-sa/4.0/legalcode" target="_blank">(CC BY-SA 4.0)</a> 
License, even for commercial purposes. </p>
<hr align="justify"> 
      <p align="justify">Please consider subscribing to our <a href="https://www.youtube.com/channel/UCgAwso8p5hkLFN9AdN6oxQg" target="_blank">
YouTube</a> Channel: <a href="https://www.youtube.com/channel/UCgAwso8p5hkLFN9AdN6oxQg" target="_blank">
https://www.youtube.com/channel/UCgAwso8p5hkLFN9AdN6oxQg</a><br>
Please follow us on <a href="https://twitter.com/TLEngineers" target="_blank">Twitter</a>: 
<a href="https://twitter.com/TLEngineers" target="_blank">https://twitter.com/TLEngineers</a><br>
Please check us out on <a href="https://www.twitch.tv/thelittleengineers" target="_blank">Twitch</a>: 
<a href="https://www.twitch.tv/thelittleengineers" target="_blank">https://www.twitch.tv/thelittleengineers</a>
<br>
Please consider following us on <a href="https://www.instagram.com/thelittleengineers_org/" target="_blank">
Instagram</a>: <a href="https://www.instagram.com/thelittleengineers_org/" target="_blank">
https://www.instagram.com/thelittleengineers_org/</a><br>
Please follow us on <a href="https://github.com/TheLittleEngineers" target="_blank">GitHub</a> in order to access all 
of our projects.<br><br>
Thank You for your time. I hope that you enjoy using these products as much as I enjoyed developing them 
(or debugging them in the case of the designs produced by my nephew and his father). - 
<i>Robert "The R.A.T." Allen Turner</i></font></td>
    </tr>
  </table>
  </center>
</div>

</body>

</html>

