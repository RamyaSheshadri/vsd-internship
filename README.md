## Name: Ramya Sheshadri 
## College:BMS College Of Engineering,Bengaluru.
## VSDSquadron Mini Research Internship
## Instructor: Mr.Kunal Ghosh

### Download Oracle VirtualBox Manager:
<img width="548" alt="oracle virtualbox" src="https://github.com/user-attachments/assets/d91a57db-cbf1-47f1-a683-8c3cb24e0053">

### Click on "Start" to obtain the following:
![vsdworkshop  Running  - Oracle VirtualBox 16-11-2024 21_41_46](https://github.com/user-attachments/assets/e3e4a933-8c79-44b5-bbe5-43615551bfad)

Oracle VirtualBox Manager is the graphical user interface (GUI) component of Oracle VM VirtualBox, a powerful and free virtualization software developed by Oracle Corporation. It allows users to create, configure, and manage virtual machines (VMs) on their computers. These virtual machines can run multiple operating systems simultaneously on a single physical machine and also provide cross platform support hence making it an essential tool for testing, development, and experimentation.
Therefore this will be used in all the tasks covered in this internship.

# Task 1:
#### Create GitHub repo.
#### Install RISC-V toolchain using VDI shared over whatsapp group. 
#### Refer to C based Lab video and RISC-V based lab videos. 
#### Complete exact steps on your machine.
#### Upload snapshot of compiled C code and RISC-V Objdmp on your GitHub repo


### i)A C program of summation of numbers from 1 to n:
![task 1 part 1](https://github.com/user-attachments/assets/9375fd75-ef2a-4700-88bb-72fcf182ac70)

### ii)The same program can be complied in assembly level language (.o):
![task 1 part 2](https://github.com/user-attachments/assets/bfcb0223-4649-4d0d-a14a-877aafbf890e)

### iii)Checking the number of instructions it takes in .c:
<img width="956" alt="task 1 obj dump" src="https://github.com/user-attachments/assets/17b19258-7c64-4b93-b307-9ba589e056fa">

### iv)Number of instructions significantly reduces when O-fast is used:
<img width="959" alt="task 1 obj dump 2" src="https://github.com/user-attachments/assets/713abcc7-2444-48a1-8e41-6a5352977dda">

## Key takeaways from task1:

### Meaning of the command: riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c

This command is invoking the RISC-V GCC cross-compiler (riscv64-unknown-elf-gcc) to compile a C program (sum1ton.c) into a RISC-V ELF object file (sum1ton.o) for the 64-bit RISC-V architecture. Here’s a breakdown of the individual options:
#### riscv64-unknown-elf-gcc:
This is the cross-compiler for the RISC-V 64-bit architecture. It is used to compile programs that will run on RISC-V systems but are being compiled on a different host (like x86).
#### riscv64:
Refers to the target architecture, which is RISC-V 64-bit.
#### unknown-elf: 
Specifies that the target system is an embedded system using the ELF (Executable and Linkable Format).
#### -O1:
This flag enables optimization level 1, which applies basic optimizations to improve performance without significantly increasing compilation time. It's a trade-off between execution speed and compilation speed.
#### -mabi=lp64:
This specifies the ABI (Application Binary Interface) to use. lp64 means:
#### l:
long data type is 64 bits.
#### p:
Pointers are 64 bits.
#### 64: 
Integer and floating-point values are 64 bits.
#### -march=rv64i:
Specifies the target architecture to be rv64i, which stands for RISC-V 64-bit with the base integer instruction set (I). This is the minimal instruction set for a RISC-V 64-bit CPU.
#### -o sum1ton.o:
This specifies the output file name. In this case, the compiled object file will be named sum1ton.o.
#### sum1ton.c:
This is the input C source file that will be compiled (sum1ton.c).
In summary, this command compiles the C file sum1ton.c for a 64-bit RISC-V system, generating an optimized object file (sum1ton.o) with 64-bit ABI and RISC-V integer instruction set.

#### What is ls -ltr?
The ls -ltr command is a combination of options for the ls command in Unix/Linux, which lists directory contents. Here's a breakdown of the flags:
-l: Long format. This option provides a detailed listing that includes file permissions, number of links, owner, group, size, and modification time of the files.
-t: Sort by modification time. Files are sorted by the time they were last modified, with the most recently modified files appearing first.
-r: Reverse order. This option reverses the sorting order. When used with -t, it shows the oldest modified files first (instead of the most recent).
ls -ltr: Lists all files and directories in the current directory (or a specified directory) in long format, sorted by the oldest modification time first.

#### What is objdump?
objdump is a command-line utility used to display information about binary files, such as object files, executables, shared libraries, or core dumps. It is commonly used for debugging, reverse engineering, or inspecting the internal structure of binaries.
Explanation of command riscv64-unknown-elf-objdump -d sum1ton.c
The riscv64-unknown-elf-objdump is a tool used for disassembling or displaying information about object files or binaries compiled for the RISC-V 64-bit architecture.
-d: This option is for disassembly. It tells objdump to disassemble the machine code in the object file or executable and display it in assembly language.
To disassemble an object file, you'd first compile the C source file (sum1ton.c) into an object file (sum1ton.o) using the RISC-V compiler, and then use objdump on the compiled object file.

#### How is using this command better in terms of number of instructions?
riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c 
#### -Ofast:
This is an optimization flag. It enables the most aggressive optimizations, more so than -O3. It may break strict standards compliance in favor of improving speed. It includes all -O3 optimizations and disables strict floating-point math operations to increase performance.
Be cautious with -Ofast, as it might change the behavior of programs that depend on strict adherence to standards





# Task 2:
### SPIKE Simulation and observation with -O1 and -Ofast. Upload snapshot of compiled C Code, RISC-V Objdmp with above options on your GitHub repo. Write a simple C program for any simple application and compile with RISC-V GCC/SPIKE"

#### i)Running the program in spike simulator:
![task2](https://github.com/user-attachments/assets/399244fd-ef87-4fea-b338-8bc0c66aebca)
#### ii)
![task 2b](https://github.com/user-attachments/assets/de5b26b5-d49e-4210-8b11-1c1adf8e5bc5)
#### iii)Sample C code used for demonstration:
![task 2 output](https://github.com/user-attachments/assets/d5a5bf10-17bf-42bb-b308-c5d7248e93f6)
#### iv)
![task 2 c code](https://github.com/user-attachments/assets/7f86124e-78c6-4f64-aa18-fc9f2594d658)

### Key learnings from Task2:
#### What is the difference between GCC and Spike?
The key difference between GCC (GNU Compiler Collection) and Spike is that GCC is a compiler, whereas Spike is an ISA simulator. They serve different purposes within the software development and testing process, especially when developing for the RISC-V architecture.
#### Spike simulator:
##### Purpose: 
Spike is an ISA simulator for RISC-V, used to emulate the execution of RISC-V machine code instructions.
##### Function: 
Spike doesn’t compile code but rather takes the machine code (generated by a compiler like GCC for RISC-V) and simulates its execution within a virtual RISC-V environment.
##### Role in Development:
Helps developers test and debug compiled code in a controlled RISC-V simulation without needing actual RISC-V hardware.
##### Output: 
Provides debugging insights, such as register values, memory states, and step-by-step execution of instructions, but does not produce a new binary.
##### Workflow: 
A common workflow is to first use GCC to compile code into a RISC-V-compatible binary. This binary is then loaded into Spike to simulate its execution, allowing the developer to test and debug their code.
##### Usage: 
GCC is essential for generating machine code, while Spike is useful for verifying that this machine code behaves as expected on a RISC-V architecture.
In summary, GCC is for compiling code into machine instructions, while Spike is for emulating and testing those instructions on a virtual RISC-V processor.

#### GCC(GNU Compiler Collection):
Purpose: GCC is a compiler that translates high-level source code (such as C or C++) into machine code (assembly or binary) that can be executed on a specific CPU architecture.
Function: GCC compiles code to produce an executable or binary file suitable for a specific ISA, such as RISC-V, x86, ARM, etc.
Role in Development: Used to generate binary files that can run directly on hardware or in an emulator.
Output: Produces machine code that is ready to be executed on a device or emulator.






# Task 3:
#### i)Various RISC-V Instruction Types:
The main RISC-V instruction types include:
R-type: Register-Register operations (e.g., add, sub)
B-type: Conditional branches (e.g., beq, bne)
U-type: Upper immediate (e.g., lui, auipc)
J-type: Jump instructions (e.g., jal)
I-type: Immediate operations (e.g., addi, lw)
S-type: Store instructions (e.g., sw)

![task 3](https://github.com/user-attachments/assets/147e93ae-a223-4763-a877-3d933a80836a)

#### ii)15 unique RISC-V instructions from riscv-objdmp of the application code: 
#### lui:
Loads an upper immediate value into the upper 20 bits of a register.
#### addi: 
Adds an immediate value to a register.
#### li:
Loads an immediate value into a register (a pseudoinstruction, typically expanded to addi with zero).
#### sd: 
Stores a double word from a register to memory.
#### jal: 
Jumps and links to a specific address, storing the return address in a register.
#### ld :
Loads a double word from memory to a register.
#### ret: 
Returns from a function (pseudoinstruction for jalr).
#### auipc:
Adds an upper immediate to the program counter.
#### beqz:
Branches if a register is zero (pseudoinstruction, typically expands to beq).
#### j: 
Unconditional jump (pseudoinstruction for jal).
#### add: 
Adds two registers.
#### sub: 
Subtracts two registers.
#### mv:
Moves a value from one register to another (pseudoinstruction, typically addi with zero).
#### lw: 
Loads a word from memory into a register.
#### c.nop:
Compressed NOP instruction, performing no operation (pseudoinstruction).

## iii)The exact 32-bit instruction code in the instruction type format for 15 unique instructions
#### lui a2, 0x1:
Binary Encoding: 00000000000000000001000110110111
Type: U-Type
#### lui a0, 0x21:
Binary Encoding: 00000000001000000000100010110111
Type: U-Type
#### addi a2, a2, -1093:
Binary Encoding: 11111111101100101010001010010011
Type: I-Type
#### li a1, 77:
Binary Encoding: 00000000010011010001000010010011
Type: I-Type (as addi with zero as source register)
#### sd ra, a0, 384:
Binary Encoding: 00000001100001011000000010100011
Type: S-Type
#### jal ra, <printf>:
Binary Encoding: 00000000000000000000100011101111
Type: J-Type
#### ld ra, 0(sp):
Binary Encoding: 00000000000000010110000010000011
Type: I-Type
#### ret:
Binary Encoding: 00000000000000000000000001100111
Type: I-Type (as jalr to x0)
#### auipc a5, 0xfffff:
Binary Encoding: 11111111111111111111001010110111
Type: U-Type
#### beqz a0, <register_fini+0x18>:
Binary Encoding: 00000000000000000000001001100011
Type: B-Type (pseudoinstruction for beq)
#### j <atexit>:
Binary Encoding: 00000000000000000000000011101111
Type: J-Type (pseudoinstruction for jal)
#### add a0, a0, a2:
Binary Encoding: 00000000001001010000001010110011
Type: R-Type
#### sub a2, a2, a0:
Binary Encoding: 01000000000010101000001010110011
Type: R-Type
#### mv a1, a0:
Binary Encoding: 00000000000001010001000010010011
Type: I-Type (pseudoinstruction for addi)
#### lw a0, 0(sp):
Binary Encoding: 00000000000000010110000000000011
Type: I-Type

# Task 4:Use this RISC-V Core Verilog netlist and testbench for functional simulation experiment. Upload waveform snapshots for the commands on your GitHub. Reference GitHub repo is here. 
 ### i)Create a folder on the desktop in Oracle VirtualBox.
 ### ii)Change the directory to this path to clone the repository:
 cd path/of/folder
 ### ii)Clone the Repository by using the follwing command:
git clone
git clone https://github.com/vinayrayapati/rv32i link
### iii)Navigate to the Cloned Directory.
Change the directory to the cloned repository.
cd rv32i
### iv)Compile the Verilog Code and Testbench.
Run the following iverilog command to compile the Verilog code and testbench.
'iverilog -o iiitb_rv32i iiitb_rv32i.v iiitb_rv32i_tb.v'
### v)Simulate the Verilog Code.
After compiling, simulate the Verilog code by running the compiled file.
'./iiitb_rv321'
### ![task 5](https://github.com/user-attachments/assets/97dbd1ff-99e8-41da-b44a-29cb50c8c1b0)

### vi)Open GTKWAVE to observe the waveforms by using following command:
'gtkwave iiitb_rv321.vcd'
#### Click on iiit_rv32i_tb under SST section.
#### We get a set of commands which we have worked on in Task 3.
#### Click on 'clk' under signals and drag it to the time section so that the corresponding waveform can be seen.
#### Similarly, drag the command 'EX_MEM_ALUOUT[31:0] to obtain the following waveform:
![task 5 ii](https://github.com/user-attachments/assets/e8feb2b7-2d1e-4c12-92e6-315645fb3dcd)


### Instruction 1: ADD r1,r2,r2
![ins 1 task 4](https://github.com/user-attachments/assets/f50b12af-cce1-4f22-8d1c-dfa822915806)

### Instruction 2: SUB r3,r1,r2
![ins 2 task 4](https://github.com/user-attachments/assets/44ab07b7-89bd-45cc-8b65-71760114734d)

### Instruction 3: AND r2,r1,r3
![ins 3 task 4](https://github.com/user-attachments/assets/23fac65a-cdd3-465a-b645-b01caf3186b7)

### Instruction 4: OR r9,r2,r5
![ins 4 task 4](https://github.com/user-attachments/assets/0fe8c175-b93d-4644-a4da-07492b349f03)

### Instruction 5: XOR r8,r1,r4
![ins 5 task 4](https://github.com/user-attachments/assets/601f8513-d7ec-4c39-af56-d943882a2153)

### Instruction 6: SLL r15,r11,r2
![ins 6 task 4](https://github.com/user-attachments/assets/4e1a6f57-8e8d-497a-ad25-53409f0773a6)

### Instruction 7: SLT r10,r2,r4
![ins 7 task 4](https://github.com/user-attachments/assets/8a2eea1c-7786-4939-bbcb-7ec334dc01f1)



# Task 5:
### Project: Ultrasonic Distance Measurement using VSDsquadron Mini Board
#### Overview:
This project aims to create a simple distance measurement system using an HC-SR04 ultrasonic sensor and the VSDsquadron Mini Board. The sensor will measure the distance of an object from the sensor, and the result will be displayed on a serial monitor or LCD screen. The ultrasonic sensor sends sound waves, measures the time taken for the waves to bounce back, and calculates the distance based on the speed of sound.

#### Some real life applications:
The Ultrasonic Distance Measurement application is highly versatile and can be useful in numerous fields. Here's how this application can make an impact:

#### i.Industrial Applications:
#### Object Detection: 
Used in automated manufacturing lines to detect the presence of objects and measure distances accurately.
#### Level Sensing: 
Monitor the level of liquids or solids in containers or silos (e.g., fuel tanks, water tanks).
#### Proximity Sensing: 
Ensure safe operations in machinery by detecting nearby objects or personnel.

#### ii.Robotics:
#### Obstacle Avoidance:
Essential for autonomous robots and drones to navigate safely in dynamic environments.
#### SLAM (Simultaneous Localization and Mapping): 
Helps in creating maps by determining distances to objects.

#### iii.Smart Cities and IoT:
#### Parking Assistance: 
Measure distances between vehicles and walls or other objects in parking systems.
#### Traffic Management: 
Monitor traffic flow by measuring distances between vehicles.

#### iv.Consumer Electronics:
#### Home Automation: 
Implement in smart home systems for tasks like automated door openers or monitoring room occupancy.
#### Security Systems: 
Detect unauthorized entry by sensing proximity.

#### v.Education and Prototyping:
Provides a practical example to learn about:
Sensor integration,
Signal processing and
Microcontroller programming.

#### vi.Healthcare:
#### Blind Assistance Devices: 
Measure distances to help visually impaired individuals navigate safely.

#### Components Required:
1.VSDsquadron Mini Board - 1
2.HC-SR04 Ultrasonic Sensor - 1
3.Breadboard - 1
4.Jumper Wires - Several
5.USB Cable - 1 (for power and programming)
6.Servo Motor: To enable the sensor to rotate and detect the distance of various objects around it.

#### Circuit Connection:
The ultrasonic sensor has four pins: VCC, Trig, Echo, and GND. We will connect these to the VSDsquadron Mini Board as per the pin connections given in the table below.

<img width="506" alt="Screenshot 2024-11-16 222722" src="https://github.com/user-attachments/assets/1b53d419-59be-43c8-8d4c-a0953ed81fda">

### Circuit Explanation:
#### Power Connections:
i.Connect the VCC pin of the HC-SR04 sensor to the 5V pin of the VSDsquadron Mini Board.
ii.Connect the GND pin of the sensor to the GND pin of the board.

#### Trigger and Echo Connections:
i.The Trig pin is connected to PC1; this pin is used to send a pulse to initiate the measurement.
ii.The Echo pin is connected to PC2; this pin receives the reflected signal.

 <img width="533" alt="image" src="https://github.com/user-attachments/assets/4512025e-64c0-4e9a-b176-669410f2d702">


# Task 6:
### Upload Final working code and short video of the application:
#### Working:

### HC-SR04 Ultrasonic Sensor:  
### Transmitter (Tx): 
Emits ultrasonic sound waves at a high frequency (typically 40 kHz).
### Receiver (Rx): 
Detects the reflected sound waves (echo) from an object.
### Microcontroller:
The VSDsquadron Mini Board processes the signals and calculates the distance.
### Power Supply: 
Provides power to the sensor and board.
### Output Display or Indicator: 
Could be an LCD, LED, or serial output to display the measured distance.

### Working Principle:
#### The system operates based on the time-of-flight (ToF) principle:
### Trigger Pulse:
The microcontroller sends a short trigger pulse (usually 10 µs) to the ultrasonic sensor to initiate measurement.
### Ultrasonic Wave Emission:
The transmitter emits an ultrasonic sound wave.
### Reflection of Wave:
The wave travels through the air and reflects back when it encounters an object.
### Echo Detection:
The receiver detects the returning echo wave.
### Time Measurement:
The microcontroller measures the time duration (Δt) between sending the trigger pulse and receiving the echo.

### Distance Calculation:
The distance to the object is calculated using the formula:
#### Distance=(Speed of Sound×Time Duration)/2
The factor of 2 accounts for the round-trip of the sound wave (to the object and back).
### Speed of Sound: 
Depends on air temperature, typically ~343 m/s at 20°C.

### Output Display:
The microcontroller processes the calculated distance and displays it on the chosen output (e.g., an LCD screen) or sends the data via serial communication for further use.

## Working Code:
<img width="956" alt="task 6 code i" src="https://github.com/user-attachments/assets/8922078d-7f29-4744-b5fc-bd50a1a9a51b">

<img width="957" alt="task 6 code ii" src="https://github.com/user-attachments/assets/0c3c0750-37b4-4c57-b8b6-734076a71d27">

<img width="959" alt="task 6 code iii" src="https://github.com/user-attachments/assets/6563d656-6124-4a5f-96c6-8c4cab62f6db">











