<h2>Basic functions of a computer</h2>
Input: User presses the button "A", results in code representing the character A sent to computer
Processing: CPU determines what letter was typed by looking up keyboard code from table
Output: CPU sends instructions to graphics card to display "A", which is sent to the monitor
<h2>Components of a computer</h2>

| Input    | Internals  | Output  |
| -------- | ---------- | ------- |
| Keyboard | CPU        | Monitor |
| Mouse    | RAM        | Printer |
|          | Hard Drive |         |
<h2>Input Components</h2>
commonly used input devices: keyboards, microphones, webcams, scanners
External interfaces (i.e. USB ports) get input from external devices
<h2>Processing Components</h2>
<h4>CPU</h4>
Computers main processing component
<strong>Function</strong>: Executes instructions from computer programs, i.e. word processors & the computer OS
CPUs with more than 2 processors are called <strong>cores</strong>.
Multicore CPUs can perform multiple instructions simultaneously; faster performance
<h2>Output Components</h2>
Examples include: Monitors, printers, external storage devices, network cards and speakers
They are external interfaces
<h2> Storage Components</h2>
More storage = better performance 
Contains 2 main categories of storage
<h4>Short Term Storage</h4>
<h5>RAM</h5>
RAM stands for Random Access Memory
RAM is volatile, data will be wiped when computer is powered off
Amount of RAM is important for computer to operate efficiently
RAM commonly referred to "<em>working storage</em>"
If there is not enough RAM, computer will use disk drive to add more RAM (known as <strong>Virtual Memory</strong>)
<h5>Virtual Memory</h5>
Part of disk storage can be set as virtual memory
CPU can only access data/code in RAM; less used data/code is placed in virtual memory
data/code will be moved to RAM when needed by CPU
<h4>Long Term Storage</h4>
Non volatile, will retain data when powered off
Used to store documents
Amount of storage required depends on type and quantity of file stored
examples: Hard disks, CD/DVDs, USB drives, SSDs
<h5>Hard Drives</h5>
Primary long-term storage component
Consists of magnetic disks (<strong>Platters</strong>) using magnetic pulses
Stores documents and applications 
Stores the OS the computer loads up during boot
<h5>Solid State Drives (SSD)</h5>
used in place of hard drives, are much faster and reliable
Contains no moving parts, faster access times
	More expensive than hard drives, more common in mobile devices
<h1>Motherboard</h1>
![[Pasted image 20240417124612.png]]


| <h2>Components</h2>         | <h2>Description</h2>                                                                                                                                                                                                             |
| --------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CPU socket                  | CPU is installed on this socket                                                                                                                                                                                                  |
| PCI bus expansion slots     | Used to add functionality by adding expansion cards with a <strong>Peripheral Component Interconnect</strong> (PCI) connector                                                                                                    |
| PCI-Express expansion slots | PCI-express supersedes PCI, has faster transfer speeds than PCI. Larger slots allow for high performance expansion card, i.e. graphics cards and disk controllers. Smaller slots used for sound cards & network interface cards. |
| RAM slots                   | Slots to install RAM                                                                                                                                                                                                             |
| Chipset with heatsinks      | Consists of two chips referred as <strong>Northbridge</strong> and <strong>Southbridge</strong>. Controls data transfers between memory, expansion slots, i/o devices and CPU. Heatsink prevents overheating.                    |
| SATA connectors             | Used to connect hard drives or CD/DVD that use <strong>Serial AT Attachment</strong> (SATA) specification                                                                                                                        |
| IDE connector               | Connects <strong>Integrated Drive Electronics</strong> (IDE) hard drives and CD/DVD-ROM drives, most systems use this for hard drives and CD/DVD-ROM drives                                                                      |
| Main power connector        | Motherboard receives power from this slot                                                                                                                                                                                        |
<h2>Bus</h2>
Collection of wires carrying signals across the motherboard
![[Pasted image 20240417135530.png]]
Data bus sends data to be stored, Address bar sends data on where the data is stored
<h6>Data Bus</h6>
Carries data signals from RAM to CPU, memory to i/o devices, and etc
<h6>Address Bus</h6>
Carries address signals, for example: memory locations 
<h6>Control Bus</h6>
Carries control signals like read/write from CPU to memory or port/interface
<h3>I/O Polling and Interrupt</h3>
Used to get the CPU's attention when it is busy
CPU needs to respond to inputs from I/O devices 
Polling and Interrupt are methods to handle events when the CPU is busy
<strong>Polling</strong>: CPU checks i/o devices on regular intervals checks if CPU service is required 
<strong>Interrupt</strong>: I/O interrupts the CPU and informs CPU it needs service
<h2>BIOS/CMOS</h2>
<strong>BIOS: Basic Input/Output System</strong>
Stores a set of instructions located in a chip on the motherboard
Tells CPU to perform tasks when power is first applied, tell it to perform <strong>Power On Self Test (POST)</strong>
BIOS offers a chance to open setup to configure hardware components, is stored in memory called <strong>Complementary Metal Oxide Semiconductor (CMOS)</strong>
<h2>Computer Boot Procedure</h2>
1. Power is applied
2. CPU starts
3. CPU carries out BIOS startup routines and POST
4. Boot devices as specified in BIOS configuration, searched for an OS 
5. OS loaded into RAM
6. OS services started
<h2>Network Interface Card (NIC)</h2>
Creates and mediates the connection between a computer and networking medium
Contains MAC address<strong>(Media Access Control Address)</strong>
MAC address = unique identifier; assigned by NIC 
<h3> Wireless NIC</h3>
Must be chosen depending on type or wireless <strong>Access Point</strong>(AP)
Typical are Wireless-n, 802.11ac or 802.11 a/b/g/n, letters refer to the wireless networking standard the device supports
Connects to network using <strong>Service Set Identifier</strong> (SSID)
May need a username and password depending on security configuration