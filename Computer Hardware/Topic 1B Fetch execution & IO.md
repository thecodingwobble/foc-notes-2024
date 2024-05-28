<h2>Data</h2>
Data is stored in bits
bits hold a 1 or 0 value
5 volts = 1, 0 (no electricity)= 0
In fiber optic: 1 = presence of light, 0 = absence of
Byte = 8 bits
<h2>Functional Units</h2>
<h4>Primary memory</h4>
Organised into <strong>words</strong> of 32 bits typically
32-bit word consists of 8 bit bytes
Programs and its data must be in Primary memory to be executed
<h4>Cache memory</h4>
Adjunct to main memory, fabricated on processor chip
smaller and faster than main memory
Holds parts of program and data currently/frequently executed
<h4>Processor</h4>
1) <strong>Logic units</strong> perform arithmetic and logic on word size data operands
2) <strong>Timing and control circuits</strong> fetch program instructions and data from memory
3) <strong>Registers</strong> (typically 16 or 32) hold one word of operand data
<h5>Processor- Arithmetic and Logic Unit (ALU)</h5>
Most computer operations executed in ALU
Performs arithmetic and logical operations
Result of executed information stored in registers or memory
<h5>Processor- Control Unit</h5>
Memory, ALU and I/O units store and process information and perform input/output operations
Control unit coordinates these units operations
<h6>Example case study: Intel CPU 8086</h6>
Internal registers are 16 bits wide, a firmly established 16 bit microprocessor
20 bit external address provides 1mb physical address space
Address space is addressed by means of internal memory segmentation
<h3>Operation of a computer</h3>
1) Computer accepts information in form of programs & data through input units and stores it in memory
2) Info stored in memory fetched under program control into ALU to be processed
3) Processed info leaves via output unit
4) Activities in computer directed by control unit
<h3>Instruction cycle</h3>
One cycle of operation (also known as <strong>Instruction cycle</strong> or <strong>Machine cycle</strong>) consists of:
Fetch, Decode, Execute, Memory Access and Write Back
1) Fetch instruction; increment program counter
2) Decode instruction and read register from register files
3) Perform ALU operation
4) Read/Write memory data if instruction involves memory operand
5) Write result into destination register if needed
<h3>Instructions and programs</h3>
Instruction specifies an operation and location of data operands 
A 32 bit word typically holds one encoded instruction
Sequence of instructions executed one after another constitutes a program
A program and its data is stored in the main memory
<h4>Instruction types</h4>
1) <strong>Load</strong>: Reads a data operand from memory or input device into processor
2) <strong>Store</strong>: Write a data operand from processor register to memory or output device
3) <strong>Operate</strong>: Perform an arithmetic or logic operation on data operands on processor registers
<h6>Example program</h6>
let A, B, C be memory word addresses
C = A + B is:
<code>Load R2, A</br>
<code>Load R3, B</br>
<code>Add  R4, R2, R3</br>
<code>Store R4, C</br>
<h2>Handling I/O devices</h2>
1) Read data from input device
2) Write data to output
3) Sense readiness of i/o device to perform transfer
<h3>Processor Components</h3>
1) <strong>Program Counter (PC)</strong> register holds memory address of current instruction
2) <strong>Instruction register (IR)</strong> holds current instruction 
3) <strong>General-purpose registers</strong> holds data and addresses (EAX)
4) <strong>Control circuits</strong> and the ALU fetch and execute instructions
<h4>Program Counter (PC)</h4>
Register that contains address of instruction executed currently
As instruction gets executed, program counter increments stored value by 1
After instruction is fetched, program counter points next instruction in sequence
Counter resets to zero when computer is restarted/reset
<h5>performance</h5>
1) Speed of electronic circuits in processor
2) Access times to cache and main memory
3) Design of instruction set
4) Number of instructions performed at once
Improvements in technology = More transistors = more logic functionality & more memory storage capacity
<h4>Parallelism</h4>
Also known as <strong>Parallel Processing</strong>, more processing units fabricated on single chip; called a <strong>core</strong> 
Processor is name of complete chip
<h1>Summary</h1>
1) Basic structure of computer - i/o, Memory, Processor
2) Instruction cycle - Fetch and execute
3) Performance - technology and parallelism
<font color="#00ff00">
<h4>Extra info:</h4>
<h5>EAX or RAX</h5>
accumulator register, stores results of arithmetic operation
32 bit systems use a 32 bit EAX register; 64 but RAX register in 64 bit systems
last 16 bits can be accessed by addressing AX; can be addressed in 8 bits by using AL for lower 8 and AH for higher 8 bits
<h5>ECX or RCX</h5>
Base register, stores base addresses for refrencing an offset
can be addressed as 64-bit RBX, 32-bit EBX, 16-bit BX, and 8-bit BH and BL registers
<h5>EDX or RDX</h5>
Counter register, used for counting operations i.e. in loops
can be addressed as 64-bit RCX, 32-bit ECX, 16-bit CX, and 8-bit CH and CL registers
<h5>ESP or RBP</h5>
Base Pointer, accesses parameters passed by the stack
Used in conjunction with Stack Segment register
 32-bit register called EBP in 32-bit systems and a 64-bit register called RBP in 64-bit systems
 <h5>ESI or RSI</h5>
 Source index register, used for string operations
 Used with Data Segment (DS) register as an offset
 32-bit register called ESI in 32-bit systems and a 64-bit register called RSI in 64-bit systems
 <h5>EDI or RDI</h5>
 Destination index register, used with Extra Segment (ES) as an offset
 called EDI in 32-bit systems and a 64-bit register called RDI in 64-bit system
 <h5>R8 - R15</h5>
 64 bit general purpose registers not found in 32 bit systems
 addressable in 32 bit, 16 bit and 8 bit modes
 we can use R8D for lower 32-bit addressing, R8W for lower 16-bit addressing, and R8B for lower 8-bit addressing. Suffix D stands for Double-word, W stands for Word, and B stands for Byte 
 <h5>RIP</h5>
 RIP is a instruction pointer, stores the address of next instruction to run (typically overwritten with a function address in a buffer overflow attack)
</font>

