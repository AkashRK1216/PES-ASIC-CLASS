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
  This is the first lab where we simulate the waveform of a hardware component.
  <p>Tools used: iverilog and gtkwave</p>
  <p> here are the commands used to generate the waveform</p>
  ![Screenshot from 2023-09-07 20-29-26](https://github.com/AkashRK1216/PES-ASIC-CLASS/assets/98165735/6d8326c0-3986-4c24-94f7-63c2d3e88c8d)
  <p><h3>Waveform</h3></p>
  ![Screenshot from 2023-09-07 20-13-05](https://github.com/AkashRK1216/PES-ASIC-CLASS/assets/98165735/1df232cf-a43b-4e9f-b2e3-1e9878ce5530)
<h5>This completes Lab 1</h5>
<h2>LAB-2</h2>
  <p>Here we use a tool called YoSys. It is a framework for RTL synthesis and provides a basic set of synthesis algorithms for various application domains. </p>
  <ol>Here are the steps followed while using yosys:
    <li><p>initating yosys and reading the mux file:</p>
    ![image](https://github.com/AkashRK1216/PES-ASIC-CLASS/assets/98165735/4842dcfa-4af0-49ce-b62e-3bd397872b84)
    </li>
    <li><p>Next, we use the "synth" command to synthesize the working of the good_mux file and we generate the stats of that particular component </p>
    ![image](https://github.com/AkashRK1216/PES-ASIC-CLASS/assets/98165735/0042e70f-6a29-4790-b6c8-f1fdcf04e399)
    </li>
  
  </ol>









</ol>







