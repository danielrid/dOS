---
layout: home
---
<h1 align="center">dOS</h1>

<p align="center" width="100%">
	Research OS written from scratch<br/>
	Retro look, new code<br/><br/>
	<img src="assets/scr_4.png" width="100%" />
<hr>
	<img src="assets/scr_1.png" width="100%" />
<hr>
	<img src="assets/scr_2.png" width="100%" />
</p>

***

<a id="top"></a>
## OS Features
+ [Modern 64-bit Kernel](#kernel-features)
+ [Graphical User Interface](#graphical-user-interface)
+ [3D Graphics Stack (DirectX 12, Vulkan, OpenGL)](#graphics-and-compute-apis)
+ [Compute and Machine Learning Stack (CUDA)](#graphics-and-compute-apis)
+ Network Stack (TCP, UDP, IPv4/IPv6, DHCP)
+ USB Stack (USB 3.0, USB 2.0)
+ Audio Stack (Server, Mixer)
+ [Win32 Subsystem (Run Windows applications!)](#win32-subsystem)
+ [Virtualization Hypervisor (Type-2)](#virtualization-hypervisor)
+ [Terminal and Command-Line Utilities](#terminal-and-command-line)
+ FAT32 (R/W), NTFS (R/W), ISO 9660

<h4 style="margin-bottom:0px"><a href="#screenshots">Videos and Screenshots</a></h4>
<h4><a href="#hardware">Supported Hardware</a></h4>
***
## Kernel Features
+ Preemptive multithreaded kernel
+ Multi-core and hyperthreading support (SMP, SMT)
+ Virtual memory
	- Swap and copy-on-write support
	- Mapped files and shared memory
	- Automatic background paging (swapper)
+ Process and memory protection (kernel and user mode)
+ Exception handling (SEH, custom, try-catch)
+ Virtual file systems with symbolic links
	- Infinite file system cache
	- Pipes and interprocess communication (IPC)
	- Mountable and networked file systems
	- DeviceFS, NetworkFS, PipeFS, RamDisk
+ Extensible synchronization primitives
	- Spinlock, Mutex, Futex, Event, Semaphore
+ Deferred and asynchronous execution
	- Deferred Procedure Calls (DPC)
	- Asynchronous Procedure Calls (APC)
+ PE executables and DLLs
	- Loadable drivers and plugins
+ WOW64: 32-bit processes on 64-bit systems
+ Kernel profiling
+ Event tracing (ETW)
+ Debugging
	- Breakpoints and stack traces
	- Symbols and source-level debugging (PDB)
	- Debugger support (LLDB)

***

## Graphical User Interface
+ Fast window manager
+ DPI scaling
+ Shell and File Explorer
+ Native UI controls and menus
+ Optimized rendering (AVX-512, AVX, SSE)
+ Transparent windows
+ Window regions
+ Themes
<p align="center" width="100%">
	<b>Transparent windows with complex regions</b><br/>
	<p></p>
	<img src="assets/gui_1.png" width="100%" />
</p>

***

## Graphics and Compute APIs

**Graphics**
+ DirectX 12 + Raytracing
+ Vulkan 1.3 + Raytracing
+ DirectX 11
+ OpenGL 4.6+

**Compute and Machine Learning**
+ CUDA 12.9 (Native / Driver API)
+ CUDA Runtime (CUDART)
+ cuBLAS
+ cuDNN

<p align="center" width="100%">
	<b>DirectX 12 (Raytracing)</b><br/>
	<p></p>
	<img src="assets/dx12_1.png" width="100%" />
</p>
<p align="center" width="100%">
	<b>Doom 3: BFG Edition (OpenGL)</b><br/>
	<p></p>
	<img src="assets/doom3_1.png" width="100%" />
	<img src="assets/doom3_4.png" width="100%" />
</p>

***

## Win32 Subsystem
+ Run Windows applications
	- Applications run on both dOS and Windows
	- Most dOS apps are standard Windows binaries
+ Native performance
	- Win32 API calls translated directly to native APIs
+ Supported APIs
	- UI: Win32 controls (partial)
	- 3D: DirectX, Vulkan, OpenGL
	- Compute / ML: CUDA
	- Audio: XAudio2, WinMM
	- Network: Winsock2
	- Event tracing (ETW)
+ Win32 and Win64 support

***

## Virtualization Hypervisor
+ Type-2 hypervisor
+ Intel VMX and AMD SVM support
+ Emulated hardware
	- APIC, PIC, PIT, CMOS
	- IDE controllers
	- Intel E1000/E1000e
	- VirtIO (disk, console)
+ KVM-like interface
+ Virtualized Ubuntu Linux (similar to WSL 2)
+ Supported guests: Linux, Windows, FreeDOS
	
<p align="center" width="100%">
	<b>Ubuntu 64-bit VM running on dOS</b><br/>
	<p></p>
	<img src="assets/ubuntu_2.png" width="100%" />
</p>
<p align="center" width="100%">
	<b>Windows VM running on dOS</b><br/>
	<p></p>
	<img src="assets/win_2.png" width="100%" />
</p>

***

## Terminal and Command Line
+ Terminals
	- VT100 support
	- Console attachments
+ Command-line utilities
	- Cmd.exe and core utilities
	- Pipes
	- Batch files
+ Development tools
	- Clang, GCC, Make, NMAKE
	- NASM, YASM, MASM
	- C# Native AOT
	- Python 3
	- LLDB debugger
	- Remote debugging with VS Code (LLDB)
	
<p align="center" width="100%">
	<b>Development tools<br/>
	dOS compiling itself, Python 3, C#</b><br/>
	<p></p>
	<img src="assets/dev_1.png" width="100%" />
</p>

***

<h2 id="hardware">Supported Hardware</h2>
+ CPU: x64, x86
+ Bus: PCI, MSI, MSI-X
+ Boot: UEFI, BIOS, Network (PXE/TFTP)
+ Disk: NVMe, AHCI, IDE
+ USB: xHCI (3.0), EHCI (2.0)
+ Network
	- Realtek (8169/8125)
	- Intel (E1000/E1000e)
	- Broadcom (BCM5722D)
+ Sound: Intel HDA, Ensoniq ES1371
+ Hypervisor: Intel VMX, AMD SVM

<p align="center" width="100%">
	<img src="assets/desktop_1.jpg" width="100%" />
</p>
<p align="center" width="100%">
	<img src="assets/laptop_2.jpg" width="49%" />
	<img src="assets/laptop_31.jpg" width="49%" />
</p>

***

<h2 align="center" style="margin-bottom:2px" id="screenshots"><b>Videos and Screenshots</b></h2>

***

<p align="center" width="100%">
	<b>DirectX 12 Raytracing</b><br/>
	{% include youtube.html id="ArRCZhUg3Rk" %}  
</p>
<p align="center" width="100%">
	<b>Doom 3: BFG Edition</b><br/>
	{% include youtube.html id="46fWmfxIx_U" %}  
</p>
<p align="center" width="100%">
	<b>Demos</b><br/>
	{% include youtube.html id="clI-W78U8s4" %}  
</p>
<p align="center" width="100%">
	<b>Self-hosting (compiling itself)</b><br/>
	{% include youtube.html id="LQxa1k08zMw" %}  
</p>
***
<p align="center" width="100%">
	<img src="assets/scr_1.png" width="100%" />
	<br/><br/>
	<img src="assets/scr_2.png" width="100%" />
	<br/><br/>
	<img src="assets/dos_commander.png" width="100%" />
	<br/><br/>
	<img src="assets/scr_4.png" width="100%" />
	<br/><br/>
	<img src="assets/scr_3.png" width="100%" />
</p>

<span style="
		  width: 80px;
		  height: 40px;
		  text-align: center;
		  line-height: 100%;
		  font-weight: bold;
    	  font-size: 14px;
		  position: fixed;
		  bottom: 0;
		  right: 5%;
		  margin: 0;
">
[(&uarr; TOP &uarr;)](#top)
</span>