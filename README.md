# <img src="https://github.com/Alex313031/Notepad-NT/blob/main/winnt_flag.svg" width="48">&nbsp; Notepad-NT &nbsp;<img src="https://github.com/Alex313031/Notepad-NT/blob/main/notepad/notepad.ico" width="42">

Windows NT 5.x Notepad with fixes

Modified from the Windows NT 5.2 source, with additions from [NotePadEx](https://github.com/vxiiduu/NotepadEx), and compiler optimizations.

 - Use [SSE2](https://en.wikipedia.org/wiki/SSE2) [SIMD](https://en.wikipedia.org/wiki/Single_instruction,_multiple_data)
   instruction set extensions for both x86 and x64.
 - Use the [/O2 compiler flag](https://learn.microsoft.com/en-us/cpp/build/reference/o1-o2-minimize-size-maximize-speed)
   for maximum optimizations.
 - Change icon to classic NT one.
 - Lint source and remove undefined variables.
 - Fix building on MSVS 2017/2019.
 - Add 'Ctrl+Shift+S' to open the "Save As" Dialog box.
 - Enable "Word Wrap" and "Status Bar" to be enabled at the same time.
 - Reduce flickering when resizing the Window on NT 6.0 and below.
 - Name is changed to "Notepad NT" for most things.

Works on Windows XP - 10 (11 doesn't display it correctly)

### TODO:

 &ndash; Add "Open New Window" option.

 &ndash; Allow "Find" Dialog box to search backwards with 'Shift+F3'

### Building

Requires MSVS 2017 or 2019 *and* the `v141_xp` Windows XP toolchain.  
This can be found in the Visual Studio Installer after going to "Individual Components" and searching for "Windows XP". 
Info [Here](https://learn.microsoft.com/en-us/cpp/build/configuring-programs-for-windows-xp#install-the-windows-xp-platform-toolset).

The original source called for MSVS 2005, and the updated project files from [vxiiduu](https://github.com/vxiiduu) 
called for MSVS 2010, but I wanted it to be able to build on modern Windows and modern MSVS, 
while still being able to build on Windows 7.

 - Open the `Notepad-NT.sln` file and then you can build it.

#### Windows 2000 Support

Requires MSVS 2010 + Windows 7 SDK  
This allows for Windows 2000 support.

 - Open the `Notepad-NT-msvs2010.sln` file and then you can build it.
