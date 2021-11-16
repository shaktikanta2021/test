# test
Source file/folder structure:
----------------------------

Test
|
|-Windows.flatc.binary
	|-flatc.exe
	|-flatbuffers
		|-include
			|-fb_decoder.cpp
			|-fb_encoder.cpp
			|-ClientSchema.fbs
			|-ClientSchema_generated.h
			|-flatbuffers..
				|-...
				
				
How did I compile/execute:
------------------------
Platform - windows 10
c++ compile/IDE - Visual Studio 2017
tool used to write cpp source code - Notepad++			

1.Go to VS developer command prompt and launch in admin mode.
Below is the path in my machine
"C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Visual Studio 2017\Visual Studio Tools"

2.cd to path where above ".cpp"	are present.

3.compile "ClientSchema.fbs" with "flatc --cpp" command so that "ClientSchema_generated.h" will be generated.
Use this ".h" file in both ".cpp" files.

4.complie both ".cpp" files with command "cl <source file name>"  so that exes will be generated in same folder.

5.Execute both executables one after another in the order	(i)fb_encoder(ii)fb_decoder with required input.
(PS: I have created source files inside flatc directory, so that I can compile and run program without much configruations to find the header dependencies/etc..)

What programs will do:
---------------------
(i) run "fb_encoder" with command: fb_encoder <binary file path>
 <binary file path>: is the name of binary file to which we want to encode.
 It asks command line inputs from user and depending on that, it executes.
 After succesful encoding, it gives message on command promopt.
 Appropriate message will be displayed in case it fails.
 
 (ii)run "fb_decoder" with command: fb_decoder <binary file path>
 <binary file path>: is the same  binary file which created in step (i).
 values are deoded and printed on command prompt, in case of any faliure appropriate message is displayed..
 
 
