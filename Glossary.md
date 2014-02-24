**Windows Internals Glossary & Abbreviations**

**Access Control List**

**ACL - Access Control List**

**ALPC** **[Asynchronous Local Procedure Cal**l](#bookmark=id.9s91dnj4870x)

**APC - Asynchronous procedure call** covered in chapter 3

**Asynchronous Local Procedure Call** A form of local IPC on windows that allows the transfer of data between user mode processes and from a kernel mode service to user mode clients. Originally Windows NT implemented IPC via the **[Local Procedure Cal**l](#bookmark=id.lkmqhn2ki1w) or LPC. The LPC api in modern versions of Windows is a wrapper around ALPC

**Automatic Crash Dump**  A new form of [crash dump](Insert Link to ALPC) in Windows 8 and Windows 2012 ([Technet](http://blogs.technet.com/b/askcore/archive/2012/09/12/windows-8-and-windows-server-2012-automatic-memory-dump.aspx))

**AWE - **Address Windowing Extension (Allows 32bit apps to allocate up to 64GB of physical memory and map it to a 2GB virtual address space)

**BCD **- Boot Configuration Database

**BNO - Base named Object**

**BPD** Binary postscript printer description. The windows postscript driver compiles *[PP*D](#bookmark=id.nmugkbs6av7d) files into BPD at runtime.

**BPN**

**Bug Code** another word for [stop code](#bookmark=id.ej4fa1j5j9x3).

**CRT - C Run-Time**

**Complete Memory Dump** a [memory dump](#bookmark=id.p4sf9fsxrnym) that consists of all physical ram at the time of a crash.

**Context Switching - **

**Checked Build - **Debug version with compile-time DBG flag. In checked build if a driver makes invalid system call, the system will stop execution rather than allow data-structures to be corrupted leading to a potential crash.

Checked Build uses ASSERT / NT_ASSERT macros defined in wdm.h and call DbgPrintEx

Ref (How to enable verbose Debug Tracing) - [http://support.microsoft.com/kb/314743](http://support.microsoft.com/kb/314743)

**CSRSS - Client Server Runtime Subsystem **(csrss.exe)

**DMA - Direct Memory Access - **Common cause of pool corruption. Occurs when hardware writes to RAM directly instead of going through a driver.

**DPC - Dispatch or Deferred Procedure Call (interrupt)**

**DRM - Digital rights management**

**ETW - Event Tracing for Windows**

**GDT - Global Descriptor Table**

**HAL - Hardware Abstraction Layer**

**Handle** A reference to an instance of an object. This is a pointer to an address space in memory (we should probably clarify the size of point on 32 vs 64 bit). Processes generally have handles to several objects. Some objects are shared by multiple processes and or threads and therefore multiple processes have handles to them.

**Hyper-Threading (HT) - **Provides 2 logical processor for each physical core.

**IDT - Interrupt Dispatch Table**

**Image** A binary file that is executed by windows. There are the kernel images, ntoskrnl.exe and ntkrnlpa.exe, and then then are images executed by windows to create *[processe*s](#bookmark=id.5wuavoxp8any).

**Interprocessor Interrupt** an interrupt in which a CPU signals another CPU to perform some task.

**Interrupts -**

**Interrupt Request Level** A priority given to an interrupt request by windows to determine the order interrupts are handled. [Wikipedia](http://en.wikipedia.org/wiki/IRQL_(Windows))

**Interrupt Object** a windows object that 

**Interrupt Service Routine** a subroutine provided by a device driver for handling hardware interrupts

**IPI - ****[Interprocessor Interrup**t](#bookmark=id.hhzagqe0zgcr)

**IRQ - Interrupt Request**

**IRQL - ****[Interrupt Request Leve**l](#bookmark=id.1h6xw38n6hw8)

**ISR - ****[Interrupt Service Routin**e](#bookmark=id.ys9lcr7dvhdy)

**Kernel Memory Dump** a [memory dump](#bookmark=id.p4sf9fsxrnym) that only consists of the kernel-mode read and write pages.

**Keyed Event**

**KMCS - Kernel Mode Code Signing - **All 64-bit device drivers must be signed by keys provided by major code-signing authorities.

**KPCR - Kernel Processor Control Region - **Data structure used by Windows Kernel to store processor data. Also uses [IDT](#bookmark=id.dkhqng3e1ex2), [TSS](#bookmark=id.ngc0siwsvzek), [GDT](#bookmark=id.yd56jfa4ds3c)

**KPP - Kernel Patch Protection**

**KPRCB - Kernel Processor Control Block**

**KTM - Kernel Transaction Manager.**

**KMDF - Kernel Mode Driver Framework. Provides an interface to WDM.**

**Local Procedure Call**

**LPC - ****[Local Procedure Cal**l](#bookmark=id.lkmqhn2ki1w)

**LSM - Local Session Manager**

**Mandatory Integrity Control** A feature added in Vista to add Integrity Level based Isolation to processes. The four integrity levels are Low, Medium, High, and System. ([Wikipedia](http://en.wikipedia.org/wiki/Mandatory_Integrity_Control))

**MDL - ****[Memory Descriptor Lis**t](#bookmark=id.sglvkvyaykus)

**Memory Descriptor **A list of addresses that describes the layout of a virtual memory buffer

**Memory Dump** A partial or complete dump of memory performed when windows crashes. The memory dump can 

**MIC - ****[Mandatory Integrity Contro**l](#bookmark=id.lbib3g5ohot2)

**Minidump** see [small memory dump](#bookmark=id.3yszf9hoca1k)

**NUMA** Non-Uniform Memory Access. In NUMA compliant systems each processors are grouped in nodes. Each node has its own processor, memory and nodes are connected through cache-coherent interconnect bus. In Windows SMP, node local memory is faster, than accessing memory attached to other nodes.

**Object** an instance of an object type. Unlike object in OOP like C++, Java and C#, the internals of an object’s data structure are opaque and require specific Win32 API calls.

**Object Attribute** a field that defines a particular *[object’s* ](#bookmark=id.gchdq1uurg2e)property.

**OCA - Online Crash Analysis**

**PCR - Process Control Region**

**PEB - Process Environment Block**

**PFN - Page Frame Number**

**PIC** - **[Process Interrupt Controlle**r](#bookmark=id.oismh0lxo2o1)

**PID** a unique identifier for a process assigned by the operating system. PIDs are 32 bit integers. PIDs can be recycled by the operating system.

**PPD** Text-based PostScript Printer Description files (.ppd files)

**PRCB - Process Control Region Block**

**Process** a container representing the execution of an instance of a process. A process is a running instance of an executable program. It contains one or more execution threads, its own address space, a list of handles to objects, and a security context. Each process has a unique *process identifier (**[PI*D](#bookmark=id.8xxbifluzuso)*)*.

**Process Interupt Controller**

**Remote Procedure Call**

**RPC - ****[Remote Procedure Cal**l](#bookmark=id.2vfk87pcly6t)

**SAM - Security Account Manager (Database of windows account / password LM hash in registry)**

**SAS - Secure Attention Sequence (aka CTRL+ALT+DEL)**

**SCM - ****[Service Control Manage**r](#bookmark=id.o4cel3oovnqh)

**Security Reference Monitor**

**Service Control Manager**

**Shatter Attach** a class of security exploit in which a low privileged process sends a message to the message loop of a process with higher privileges in order to get it to execute code on its behalf 

**Small Memory Dump** commonly known as a minidump and infrequently a triage dump. This is the smallest form of [memory dump](#bookmark=id.p4sf9fsxrnym).

**SMSS - Session manager (smss.exe) - **First user mode process created in the System.

**SMP (Symmetric Multi-processing) / ASMP (Asymmetric multiprocessing) - **Windows uses SMP. In SMP there is no master processor. All processors share just one memory space. In ASMP, OS selects one processor to execute Kernel Code and runs user code in other processors.

**Spinlocks**

**SRM - Security Reference Monitor**

**Stop Code** The code passed to *[KeBugCheckEx(*)](http://msdn.microsoft.com/en-us/library/windows/hardware/ff551961(v=vs.85).aspx) that describes the cause of the crash. Stop codes are defined in the header file Bugcodes.h.

**SUA - Subsystem for Unix Applications **(For Posix compliance)

**TEB - Thread Environment Block**

**Thread**

**TLB - Translation Lookaside Buffer - **

**Triage Dump** see [small memory dump](#bookmark=id.3yszf9hoca1k)

**Trusted Computer System Evaluation Criteria **A Depart Of Defense (DOD) classification of the security protections offered by operating systems, network components, and trusted applications.([http://csrc.nist.gov/publications/history/dod85.pdf](http://csrc.nist.gov/publications/history/dod85.pdf))

**TCSEC - ****[Trusted Computer System Evaluation Criteri**a](#bookmark=id.s4uefcz0d96p)

**TSS - Task State Segment**

**UIPI - User Interface Privilege Isolation**

**UMDF - User mode Driver Framework - **Enables USB / high-latency buses to be implemented as user mode drivers. Each user mode driver runs as a user-mode service that uses [ALPC](#bookmark=id.3mrcykg3t4d7) port to communicate to a kernel-mode wrapper driver. If UMDF driver crashes, the process dies and restarts without affecting the whole system.

**User Interface Privilege Isolation** ([wikipedia](http://en.wikipedia.org/wiki/User_Interface_Privilege_Isolation))

**VAD - Virtual Address Descriptors - **Data Structures used by Memory Manager to keep track of Virtual Addresses used by a process

**WDM - Windows Driver Model**

**WER - Windows Error Reporting.**

