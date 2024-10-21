Create GitHub repo.
Install RISC-V toolchain using VDI shared over whatsapp group. 
Refer to C based Lab video and RISC-V based lab videos. 
Complete exact steps on your machine.
Upload snapshot of compiled C code and RISC-V Objdmp on your GitHub repo.

Contents learnt from this task:

Meaning of the command: riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c

This command is invoking the RISC-V GCC cross-compiler (riscv64-unknown-elf-gcc) to compile a C program (sum1ton.c) into a RISC-V ELF object file (sum1ton.o) for the 64-bit RISC-V architecture. Here’s a breakdown of the individual options:
riscv64-unknown-elf-gcc:
This is the cross-compiler for the RISC-V 64-bit architecture. It is used to compile programs that will run on RISC-V systems but are being compiled on a different host (like x86).
riscv64: Refers to the target architecture, which is RISC-V 64-bit.
unknown-elf: Specifies that the target system is an embedded system using the ELF (Executable and Linkable Format).
-O1:
This flag enables optimization level 1, which applies basic optimizations to improve performance without significantly increasing compilation time. It's a trade-off between execution speed and compilation speed.

-mabi=lp64:
This specifies the ABI (Application Binary Interface) to use. lp64 means:
l: long data type is 64 bits.
p: Pointers are 64 bits.
64: Integer and floating-point values are 64 bits.

-march=rv64i:
Specifies the target architecture to be rv64i, which stands for RISC-V 64-bit with the base integer instruction set (I). This is the minimal instruction set for a RISC-V 64-bit CPU.
-o sum1ton.o:
This specifies the output file name. In this case, the compiled object file will be named sum1ton.o.
sum1ton.c:
This is the input C source file that will be compiled (sum1ton.c).
In summary, this command compiles the C file sum1ton.c for a 64-bit RISC-V system, generating an optimized object file (sum1ton.o) with 64-bit ABI and RISC-V integer instruction set.

Cat is the short form for concatenate

What is ls -ltr?
The ls -ltr command is a combination of options for the ls command in Unix/Linux, which lists directory contents. Here's a breakdown of the flags:
-l: Long format. This option provides a detailed listing that includes file permissions, number of links, owner, group, size, and modification time of the files.
-t: Sort by modification time. Files are sorted by the time they were last modified, with the most recently modified files appearing first.
-r: Reverse order. This option reverses the sorting order. When used with -t, it shows the oldest modified files first (instead of the most recent).
ls -ltr: Lists all files and directories in the current directory (or a specified directory) in long format, sorted by the oldest modification time first.

What is objdump?
objdump is a command-line utility used to display information about binary files, such as object files, executables, shared libraries, or core dumps. It is commonly used for debugging, reverse engineering, or inspecting the internal structure of binaries.
Explanation of command riscv64-unknown-elf-objdump -d sum1ton.c
The riscv64-unknown-elf-objdump is a tool used for disassembling or displaying information about object files or binaries compiled for the RISC-V 64-bit architecture.
-d: This option is for disassembly. It tells objdump to disassemble the machine code in the object file or executable and display it in assembly language.
To disassemble an object file, you'd first compile the C source file (sum1ton.c) into an object file (sum1ton.o) using the RISC-V compiler, and then use objdump on the compiled object file.

How is using this command better in terms of number of instructions?
riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c 
-Ofast:This is an optimization flag. It enables the most aggressive optimizations, more so than -O3. It may break strict standards compliance in favor of improving speed. It includes all -O3 optimizations and disables strict floating-point math operations to increase performance.
Be cautious with -Ofast, as it might change the behavior of programs that depend on strict adherence to standards.




