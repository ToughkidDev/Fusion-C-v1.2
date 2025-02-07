# Fusion-C-v1.2
 
Fusion-C 1.2 is a free C library with which you can program software and games for MSX computers under MSX-DOS with C language.
You must use Fusion-C with SDCC 3.6.0 compiler (other versions have not been tested, but should work with more or less changes in the FUSION-C compilation script)
Library is providing functions to work with every aspects of MSX computers (MSX1, MSX2, MSX2+, MSX TURBO-C) easily. The package is ready to use to make games and others tools.

The Fusion-C Library can be supplemented by the book "FUSION-C COMPLETE JOURNEY" which you can buy on Amazon :
https://www.amazon.fr/FUSION-C-MSX-Library-complete-journey/dp/1730828612/ref=sr_1_1?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&keywords=msx+Fusion-c


Have fun coding for MSX !
Eric Boez January/august 2019


-------------------------------------------------------------
History


—————————————————— 2019 - Sptember 13 ——————————————————
FUSION-c 1.2
Changes :

- added support functions for GFX9000/V990 and TCPIP for the Gr8NET. Both in beta version 

- New Library compilation Scripts

- Fixed error or rewritten functions : 
		RleWBToRam and RleWBToVram		(msx_fusion.h)
		MouseRead				(msx_fusion.h)
		LMMM ( \!/ variables order changed) 	(vdp_graph2.h)
		Line  (Now Works on Screen 7)		(vdp_graph2.h)
		Point (Now Works on Screen 7)		(vdp_graph2.h)
		Pset  (Now Works on Screen 7)		(vdp_graph2.h)
		CheckBreak 				(msx_fusion.h)
		PutCharHex				(msx_fusion.h)
		PrintHex				(msx_fusion.h)



- added function to library and to manual/book :
	 	HMMM (Vram to Vram copy function)	(vdp_graph2.h)
		LMMC (Ram to Vram copy function)	(vdp_graph2.h) 
		YMMM (Vram to Vram CopyY position)	(vdp_graph2.h)
		HMMV (High speed rectangle fill)	(vdp_graph2.h)
		LMMV (High speed rect. fill with OP)	(vdp_graph2.h)
		MouseReadTo (Read mouse to structure)	(msx_fusion.h)
		Itoa (Integer to Char cons.)		(msx_fusion.h)
		StrReverse (Reverse a char string)	(msx_fusion.h)
		BoxFill					(vdp_graph2.h)
		BoxLine  				(vdp_graph2.h)
		
- Removed functions :
		Rect  (Same as BoxFill)

- examples added or modified :
		loadScreen5Image.c
		ReadMouseTo.c
		MouseRead.c
		RlewbToVram.c
		sprites-msx2.c
		lineandbox.c
		vdptest5.c
		vdptest8.c

		GFX9000 examples Folder
		Gr8NET_TCPIP Example Folder

Updates on SublimeText Build System and Makefile Compilation script for MacOS users.
Now the current file you are working on with SublimeText is detected and can be 
compile on the fly the build Sublime Text Build system.
-Update your Build Script by copying  
./Working Folder/Tools/_for Sublime Text/MacOs/sdcc-build.sublime-build
To /Users/<YOUR USER NAME>/Library/Application\ Support/Sublime Text 3/Packages/User/
-update the Makefile provide with this Fusion-C version.

—————————————————— 2019 - June 17 ——————————————————
FUSION-c 1.1a
Changes :

- Correction of a bug introduced in 1.1 version inside Print function


—————————————————— 2019 - May 28 ——————————————————
FUSION-c 1.1
Changes :

- Missing function definition added in msx_fusion.h :
		SetBorderColor

- Errors in definitions fixed in msx_fusion.h  :
	  	StrToLower 	  renamed into CharToLower
	  	StrToUpper 	  renamed into CharToLower
	  	keyboardRead 	  renamed into KeyboardRead
		EnableInterupt    renamed into EnableInterrupt
		DisableInterupt   enamed into DisableInterrupt	

- Mistakes or Errors Fixed in Manual/Book :
	  	SetScrollH
	  	SetScrollV 
	  	Sprite16
	  	Sprite8
	  	SetSC5Palette
	  	Vpoke
	  	other typo

- Removed fonctions from previous version :
	 	WaitForKey 	(msx_fusion.h) idem as WaitKey 
	  	KeyboardHit 	(msx_fusion.h) idem as Inkey 
		Getcon		(msx_fusion.h) idem as Getche

- Errors in variable type fixed :
	  	Ltell second parameter is  Long type variable
	  	Lseek second parameter is  Long type variable
 
- added instruction details in manual/book :
		printf

- added long support to printf


- Fixed or rewritten source code’s functions :
		getche.s
		vdp_graph2.s
		setdate.s
		inkey.s
		waitkey.s
		getche.s
		joystickRead.c
		triggeread.c
		killekeybuffer.c
		fillvram.c
		crt0_msxdos.s



- added functions to library and to manual/book :
		MouseRead		(msx_fusion.h)
		SetRealTimer		(msx_fusion.h)
		RealTimer		(msx_fusion.h)
		CovoxPlay		(msx_fusion.h)
		SC2Circle		(vdp_circle.h)
		SC2FilledCircle		(vdp_circle.h)	
		VDPLinesSwitch		(msx_fusion.h)
		RleWBToVram		(msx_fusion.h)
		RleWBToRam		(msx_fusion.h)
		GetDiskParam		(io.h)
		GetDiskTrAddress	(io.h)
		SetDiskTrAddress	(io.h)
		SectorRead		(io.h)
		SectorWrite		(io.h)
		CopyRamToVram		(msx_fusion.h)
		CopyVramToRam		(msx_fusion.h)
		PutText			(msx_fusion.h) (Function Enhanced with Logical Operator)	
		GetVramSize		(msx_fusion.h)
		InitInterruptHandler	(msx_fusion.h)
		EndInterruptHandler	(msx_fusion.h)
		SetInterruptHandler	(msx_fusion.h)


- added code example : 
		random-number.c 
		hardware-scroll.c 
		mouse.c 
		timer.c
		16x16_pixels_sprites.c
		arguments.c
		vsync_do.c
		vdp_blanking_test.c
		Circle_Msx1.c
		sc5Palette.c
		rlewbToVram.c
		riewb-test.c
		rlewbToRam.c
		readDiskParamandsectors.c
		printTextGraphic.c
		RamVramCopy.c
		interrupt.c

- Compilation scripts Makefile & Compil.bat enhanced with conditional starting of openMSX

—————————————————— 2019 - January 08 ——————————————————
- Fusion-C V1.0 Initial Release 