# PES-ASIC-CLASS
This is my github repo for ASIC classes

<p>ASIC stands for Application Specific Integrated Chip Design and is an integral part of our daily lives.
This course covers key aspects of RISC-V and chip design, spanning design cycles, RISC-V ISA, analog IPs, and mixed-signal flow. It delves into process design kits, libraries, RTL design synthesis, and gate-level simulation. The curriculum also includes RTL-to-GDS flow, encompassing SoC design implementation from floor planning to post-layout timing analysis.</p>
Instructor name: Kunal Ghosh

<p>Installation source: https://github.com/kunalg123/riscv_workshop_collaterals/blob/master/run.sh</p>

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

<h1>INTRODUCTION TO VERILOG</h1>
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
<!--End of LAB 1 ########################################################################################################################################################################################-->
<h2>LAB-2: RTL design using Verilog with SKY130 Technology</h2>
<p><h3>Introduction to Verilog Design, RTL and Synthesis</h3></p>
  <ul>
    Here is a list of tools we will be using:
    <li><b>Yosys:</b> Yosys is an open-source synthesis tool that converts RTL (Register Transfer Level) descriptions written in HDL (Hardware Description Language) into optimized gate-level netlists for digital circuit designs. -Inputs to yosys : liberty file(.lib) and design file(HDL) -Output : synthesized netlist mapped with the provided technology library</li>

  <li><b>Iverilog:</b> Iverilog is an open-source Verilog simulation and synthesis tool that allows designers to verify their digital designs using simulation and generate netlists for synthesis. -Inputs to iverilog : testbench and design files -output : VCD (Value change dump) file that stores data related to simulation</li>

<li><b>GTKWave:</b> GTKWave is an open-source waveform viewer that provides graphical visualization of simulation results produced by digital design simulation tools, aiding in the debugging and analysis of digital circuits. -Inputs : VCD FIle -output : Simulation waveform</li>
  </ul>
  <ul>
    <h4>Here are the terminologies used:</h4>
    <li><b>Simulator :</b> The RTL should be check if it matches with the specifications provided. This work is done by Simulator and is used to simulate the design for its functionality
<p>Example : iverilog</p>
<p>Simulator looks for a change in input, based on which the output is evaluated ==> if there is no change in input, Then output is not evaluated.</p></li>
<li>Design : The set of verilog code(s) that represents the provided functionality/Specification in the form of a netlist.</li>
<li>Testbench : Setup to apply stimulus(test vectors)to the design inorder to check the functionality using the response obtained.</li>
<p><h5>The response is obtained using iverilog in the form of VCD file that is visulaised using gtkwave</h5></p>
<li>Synthesizer : Tool required t convert RTL to netlist</li>
<p>Example : yosys</p>
<li>Netlist : In Synthesis, RTL Design is converted to gate level netlist ie.,design is converted into gates and connections are made between the gates. This is givenout as a file called netlist.</li>

<li>liberty(.lib) : It contains all cells required to represent any logic and the cells are of different flavours(different power, delay, operating conditions etc)</li>
  </ul>
  <!-- Below lines are for yosys -->
  <ol><h3>Steps to create and obtain a waveform from yosys</h3>
  <li>create a simple design file mux.v mux.v</li>
  <li>write a testbench for it mux_tb.v</li>  
  </ol>
  ![image](https://github.com/AkashRK1216/PES-ASIC-CLASS/assets/98165735/b51d1e8e-09cd-42bd-bec6-aa6b3044ed1a)

  <h3>Some Important Points :</h3>
<p>Every Liberate file has different flavours of cells such as slow,fast and typical.</p>
<p>Every Liberate file has different flavours of cells such as slow,fast and typical.</p>
<p>why slow cells? : If the combinational block provides output very fast, then it becomes harder for the next combinational block to process the signal. Therefore we use slow cells to balance the delay.(ENsure no HOLD issues)</p>
<p>Faster cells and slower cells are differentiated based on the rate of charging and discharging, higher the rate, lesser the delay. This can be done when we can source more current through the transistors that is achieved by widening the transistors.</p>
<p>Wider transistor : Low Delay : More area : More power</p>
<p>Narrow transistors : Larger delay : Less area : Less power</p>
Therofore, to achieve optimal syntheis result, we have to specify constraints to the synthesizer that says which set of cells to be selected for syntheis process.

<h2>Interactive Flow (Synthesis)</h2>
<ol>Here are the Steps required to perform Synthesis using Yosys
  <li>open yosys where the verilog files are present using the command - <code>yosys</code></li>
<li>Specify the technology library to be used - <code>read_liberty -lib <PATH_TO_.lib_FILE_LOCATION>/sky130_fd_sc_hd__tt_025C_1v80.lib</code></li>
<li>specify all the verilog files to be synthesized - <code>read_verilog mux.v</code></li>
<li>since some designs have submodules, it is necessary to mention the topmodule name <code> - synth -top mux</code></li>
<li>Generate synthesized netlist (ABC links the expression declared in design file with cells present in library) <code>- abc -liberty <Path_to_.lib_File>/sky130_fd_sc_hd__tt_025C_1v80.lib</code></li>
<li>To view the graphical representation of sytnthesized netlist<code> - show</code></li>
<li>Write the generated netlist into a verilog file <code>- write_verilog mux_mapped.v</code> or <code>write_verilog -noattr mux_mapped.v</code></li>
</ol>
<p> here is an image of the ABC stats of the mux.v file</p>
<img>![image](https://github.com/AkashRK1216/PES-ASIC-CLASS/assets/98165735/4bb90ca1-22cf-4e26-ade3-e197a36a42c0)
 </img>
 <p> Here is a netlist image of the mux.v File</p>
 ![image](https://github.com/AkashRK1216/PES-ASIC-CLASS/assets/98165735/b87eb68b-464f-44de-8764-0895927f4aad)
<p> this conlcudes Day 1 in RTL design LAB</p>
 <!-- End of Day 1 in Lab 2 -->
 <h2>Day 2 of RTL Design- Timing libs</h2>
 <h3>Some terms in a Liberate File</h3>
 <ul>
 <li><b>tt</b> - Typical PMOS typical NMOS (Regular working speed)</li>

<li><b>025C</b> - Temperature</li>

<li><b>1v80</b> - supply voltage The above 3 parameters shortly known as PVT(Process Voltage Temperature) define how and at what conditions the fabricated silicon works</li>

<li><b>sky130</b> - 130nm Technology node</li>

<li><b>fd </b>- Foundry design</li>

<li>sc - standard cell</li>

<li>hd - high density - This specifies that this library supports using these standard cells at a high density resulting in samller chip area</li>

<li>The library file consists of all the details of the cell ie., leakage power, area, timing etc. for all input combinations</li>   
 </ul>

 <h3>Types of Synthesis</h3>
 <p><b>1.Hierarchial Synthesis:</b>Here the hierarchy is maintained. The submodules are displayed as it is </p>
 <p>For example:</p>
 ![image](https://github.com/AkashRK1216/PES-ASIC-CLASS/assets/98165735/9b861b05-b803-4801-99ac-8c84769480d5)
 <ul><h5>A Few notes</h5>
 <li>While synthesizing OR gate , AND gate, most of the times the tool uses NAND Gates to obtain the functionality as in NAND gates,The NMOS are connected in series and provide better signal transfer.</li>
<li>Submodule level synthesis helps reduce synthesis time when in a massive design, the same submodule has been called many times and also we can synthesize all submodules and stitch them to obtain top level.But here the optimisation also takes place at submodule level ,not at top level.3</li> 
 </ul>

 <h3>Flop coding styles</h3>
 <ul>WHat are flops and why do we need them?
 <li>In digital electronic circuits and digital system design, a "flop" typically refers to a flip-flop, which is a fundamental building block used for storing and manipulating binary information.</li>
<li>Flip-flops are crucial components in digital logic circuits and serve several essential purposes such as Memory Element, Synchronization, Sequential Logic, Clocking, Edge Detection, Pipelining, State Storage, Memory Cells.</li>
<li>Flip-flops are essential components in digital electronics because they provide the means to store, manipulate, and control binary information, enabling the design and operation of a wide range of digital systems and devices, from simple registers to complex microprocessors and digital signal processors.</li>
<li>Their role in sequential logic, synchronization, and memory storage is fundamental to the functioning of digital circuits and systems.</li>
<li>It's a type of sequential logic element that stores binary information (0 or 1) and can change its output based on clock signals and input values.</li>   
 </ul>
 <b>We use a D flip flop largely in circuits and There are two types:</b>
 <ul>
   Synchronous and Asynchronous
   <li>
     <ul><b>Asynchronous Reset</b>
       <li> A D flip-flop with an asynchronous reset is a type of digital flip-flop circuit that includes a "D" (data) input and an asynchronous reset input. It is a fundamental building block in digital electronics and sequential logic circuits.</li>

<li>a D flip-flop with asynchronous reset stores data at the input (D) and transfers it to the output (Q) on a clock edge (depending on the flip-flop type).</li>
     </ul>
     ![image](https://github.com/AkashRK1216/PES-ASIC-CLASS/assets/98165735/a926a263-ed9b-4945-a583-0bd4e284d9a0)
   </li>
   <li>
     <ul><b>Synchronous Set</b>
       <li> When the reset is high on the positive edge of the clock, the output of the flip-flop is forced to 0.</li>
<li>Else, on the positive edge of the clock, the stored value is updated at the output.</li>
     </ul>
     ![image](https://github.com/AkashRK1216/PES-ASIC-CLASS/assets/98165735/c02a489f-552c-4489-88dd-7d0027814981)

   </li>
 </ul>

 <h2>Gate Level Simulation</h2>
 <ul>
   <li> used for post-synthesis verification to ensure functionality and timing requirements</li>
<li>input : testbench ,synthesized netlist of a deisgn, gate level verilog models (since design now is synthesised one , it has library gate definitions in it.so we have to pass those verilog models too)</li>
<li>sometimes there is a mismatch in simulation results for post-synthesis netlist that's called synthesis simulation mismatch</li>
 </ul>
 <h3>Pre and Post synthesis simulations of a conditional mux</h3>
 ![image](https://github.com/AkashRK1216/PES-ASIC-CLASS/assets/98165735/36288cbb-f372-4d74-b7bd-26745a36b25d)


 
 


 
















