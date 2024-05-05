# PES-ASIC-CLASS
This is my github repo for ASIC classes

<p>ASIC stands for Application Specific Integrated Chip Design and is an integral part of our daily lives.
This course covers key aspects of RISC-V and chip design, spanning design cycles, RISC-V ISA, analog IPs, and mixed-signal flow. It delves into process design kits, libraries, RTL design synthesis, and gate-level simulation. The curriculum also includes RTL-to-GDS flow, encompassing SoC design implementation from floor planning to post-layout timing analysis.</p>
Instructor name: Kunal Ghosh

I<p>nstallation source: https://github.com/kunalg123/riscv_workshop_collaterals/blob/master/run.sh</p>

<h1>DAY 1:</h1>

  <p>1)we learn how to type and execute a c code in the linux terminal
  
![Screenshot from 2023-08-21 23-11-19](https://github.com/AkashRK1216/PES-ASIC-CLASS/assets/98165735/d4839919-0f72-404c-abe0-67fa124b2f3d)
![Screenshot from 2023-08-21 23-12-39](https://github.com/AkashRK1216/PES-ASIC-CLASS/assets/98165735/6edddcea-9ebb-4391-aec5-41ea9adae824)</p>

 <p>2) we learn to break down the C code into assembly code:
![Screenshot from 2023-08-21 23-19-02](https://github.com/AkashRK1216/PES-ASIC-CLASS/assets/98165735/08ba8c54-d60a-4745-a764-f6ab079190fc)
here is the assembly version of only the main() part of the C program:

![Screenshot from 2023-08-21 23-28-00](https://github.com/AkashRK1216/PES-ASIC-CLASS/assets/98165735/b2b199be-419c-476f-a65a-92ec62cf363e)
![Screenshot from 2023-08-21 23-21-03](https://github.com/AkashRK1216/PES-ASIC-CLASS/assets/98165735/3ca3315b-e5ee-44ea-9635-91607d2b0cb1)</p>

<p>This concludes day 1.</p>

<h1>DAY 2:</h1>
<p>An Application Binary Interface (ABI) defines how binary code interacts at a low level, specifying data structures, calling conventions, and system-level details to ensure compatibility between compiled software components on a given platform.

Application software -(API)-> Standard Libraries -> OS -(ISA)-> Processor Architecture -(RTL)-> Hardware
API - Application Programming Interface
ISA - Intruction Set Architecture
RTL - Register transfer level</p>
<p>In the below code, we write a C program that iterates from 1 to n and finds the sum</p>
<p>!![Screenshot from 2023-08-25 20-31-32](https://github.com/AkashRK1216/PES-ASIC-CLASS/assets/98165735/0f8ac11b-262b-4049-b11d-d2c22d7e2c98)</p>

<ol><h1>INTRODUCTION TO VERILOG</h1>
<p>In this set of labs, we will learn about the Hardware Descriptive Language (HDL) called iverilog and its usage through a Command Line Interface</p>
<p> GTKWave acts as a waveform simulator for us to verify the working of the hardware simulation</p>
<h2>LAB-1</h2>
  <h2>Memory Allocation for Double Words</h2>
  <p>64-bit number (or any multi-byte value) can be loaded into memory in little-endian or big-endian. It involves understanding the byte order and arranging the bytes accordingly

Little-Endian: In little-endian representation, you store the least significant byte (LSB) at the lowest memory address and the most significant byte (MSB) at the highest memory address.
<p>Big-Endian: In big-endian representation, you store the most significant byte (MSB) at the lowest memory address and the least significant byte (LSB) at the highest memory address.</p>
<p>For example, consider the 64-bit hexadecimal value 0x0123456789ABCDEF.</p>
In Little-Endian representation, it would be stored as follows in memory:
![image](https://github.com/AkashRK1216/PES-ASIC-CLASS/assets/98165735/6e229be0-7336-4484-804c-11da572ac186)


In Big-Endian representation, it would be stored as follows in memory:
[image](https://github.com/AkashRK1216/PES-ASIC-CLASS/assets/98165735/586f2b87-85ab-45c4-9cf3-a7f7547c71fe)
<h2>Load, Add and Store instructions</h2>
<p>Load, Add, and Store instructions are fundamental operations in computer architecture and assembly programming. They are often used to manipulate data within a computer's memory and registers.

<h4>Load Instructions:</h4>
Load instructions are used to transfer data from memory to registers. They allow you to fetch data from a specified memory address and place it into a register for further processing.
<p>Example:  <code>ld x6, 8(x5)</code></p>
In this Example:
<b>ld</b> is the load double-word instruction.
<b>x6</b> is the destination register.
<b>8(x5)</b> is the memory address pointed to by register x5 (base address + offset).

<h4>Store Instructions:</h4> Store instructions are used to write data from registers into memory.They store values from registers into memory addresses
<p>Example <code>sd x8, 8(x9)</code></p>

<p>In this Example</p>

<p><b>sd</b> is the store double-word instruction.</p>
<p><b>x8</b> is the source register.</p>
<p><b>8(x9)</b> is the memory address pointed to by register x9 (base address + offset).</p>

<p>Add Instructions: Add instructions are used to perform addition operations on registers. They add the values of two source registers and store the result in a destination register.</p>
<p>Example <code>add x9, x10, x11</code></p>

In this Example

<b>add</b> is the add instruction.
<b>x9</b> is the destination register.
x10 and x11 are the source registers.</p>
<h2>Application Binary Interface</h2>
<p>The choice of the number of registers in a processor's architecture, such as the RISC-V RV64 architecture with its 32 general-purpose registers, involves a trade-off between various factors.</p>
<p>While modern processors can have more registers but increasing the number of registers could lead to larger instructions, which would take up more memory and potentially slow down instruction fetch and decode.</p>

<h3>ABI Names</h3>
<p>ABI names for registers serve as a standardized way to designate the purpose and usage of specific registers within a software ecosystem. These names play a critical role in maintaining compatibility, optimizing code generation, and facilitating communication between different software components.</p>
<img>![image](https://github.com/AkashRK1216/PES-ASIC-CLASS/assets/98165735/7ba065fb-b805-4c9b-b345-cc209a7abf0d)


  This is the first lab where we simulate the waveform of a hardware component.
  <p>Tools used: iverilog and gtkwave</p>
  <p> here are the commands used to generate the waveform</p>
  ![Screenshot from 2023-09-07 20-29-26](https://github.com/AkashRK1216/PES-ASIC-CLASS/assets/98165735/6d8326c0-3986-4c24-94f7-63c2d3e88c8d)
  <p><h3>Waveform</h3></p>
  ![Screenshot from 2023-09-07 20-13-05](https://github.com/AkashRK1216/PES-ASIC-CLASS/assets/98165735/1df232cf-a43b-4e9f-b2e3-1e9878ce5530)
<h5>This completes Lab 1</h5>
<h2>LAB-2: RTL design using Verilog with SKY130 Technology</h2>
<p><h3>Introduction to Verilog Design, RTL and Synthesis</h3></p>
  <ul>
    Here is a list of tools we will be using:
    <li><b>Yosys:</b> Yosys is an open-source synthesis tool that converts RTL (Register Transfer Level) descriptions written in HDL (Hardware Description Language) into optimized gate-level netlists for digital circuit designs. -Inputs to yosys : liberty file(.lib) and design file(HDL) -Output : synthesized netlist mapped with the provided technology library</li>

  <li><b>Iverilog:</b> Iverilog is an open-source Verilog simulation and synthesis tool that allows designers to verify their digital designs using simulation and generate netlists for synthesis. -Inputs to iverilog : testbench and design files -output : VCD (Value change dump) file that stores data related to simulation</li>

<li><b>GTKWave:</b> GTKWave is an open-source waveform viewer that provides graphical visualization of simulation results produced by digital design simulation tools, aiding in the debugging and analysis of digital circuits. -Inputs : VCD FIle -output : Simulation waveform</li>
  </ul>
  <ol>Here are the steps followed while using yosys:
    <li><p>initating yosys and reading the mux file:</p>
    ![image](https://github.com/AkashRK1216/PES-ASIC-CLASS/assets/98165735/4842dcfa-4af0-49ce-b62e-3bd397872b84)
    </li>
    <li><p>Next, we use the "synth" command to synthesize the working of the good_mux file and we generate the stats of that particular component </p>
    ![image](https://github.com/AkashRK1216/PES-ASIC-CLASS/assets/98165735/0042e70f-6a29-4790-b6c8-f1fdcf04e399)
    </li>
  
  </ol>









</ol>







