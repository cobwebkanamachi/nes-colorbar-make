# nes-colorbar-make
<PRE>
How to make Quietust's Color Bars (https://www.qmtpro.com/~nes/demos/colors.zip). 
If you would not read https://www.qmtpro.com/~nes/ you would check it.

I bought a FlashCart of Mapper 0.
It has Quietust's Color Bars (ver1) in the flash for sell.
I check that's UI and compare several color bar apps, so I found Quietust's one.

I wrote bellow how to reproduce from source to .nes.
I did binary compare, they are identical(no difference).

on cmd.exe of Windows11.
The Pathes are 
c:\Users\user\Downloads
   tasm32 <- "Telemark Cross Assembler 3.2" extracted https://www.ticalc.org/pub/dos/asm/tasm32.zip
   colors <- extracted colors.zip)
   makeines10 <- extracted https://www.qmtpro.com/~nes/tools/makeines10.zip
   makeunif10 <- extracted https://www.qmtpro.com/~nes/tools/makeunif10.zip
del *.nes *.obj *.unif
cd ..\tasm32
.\tasm -65  -b ..\colors\colors.asm ..\colors\colors.obj
cd ..\colors
..\makeunif10\makeunif colors.umk
..\makeines10\makeines colors.imk
If you prefer binary compare, do check fc /b orig.nes build.nes.
I test with this rom, I found this is a hello world with mapper 0(digits, RGB string).
Enjoy!
</PRE>
