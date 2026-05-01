# Half adder- CMOS Design & Verilog Implementation
Table Of Contents
1.Introduction
2.Truth Table
3.Logic Gates & Boolean Expressions
4.Circuit Diagram (Gate Level)
5.CMOS Implementation in LTspice
6.Verilog Code
7.Simulation Waveforms
8.Tools Used
9.How to Run

Introduction
A Half Adder is one of the fundamental building blocks of digital arithmetic circuits. It performs binary addition of two single-bit inputs and produces two outputs:
Sum (S) — the result of the addition
Carry (C) — the overflow bit carried to the next significant position

Unlike a Full Adder, the Half Adder does not account for a carry input from a previous stage  hence the name half. Despite its simplicity, it forms the basis of all arithmetic logic units (ALUs) in modern processors.

This project demonstrates the Half Adder implemented in two ways:
CMOS transistor-level design — simulated using LTspice
Register Transfer Level (RTL) design — written in Verilog HDL and simulated using ModelSim

Truth Table
The Half Adder operates on two binary inputs A and B:
<img width="393" height="255" alt="Truth-table-for-half-adder_W640" src="https://github.com/user-attachments/assets/8c60f294-1156-4320-ad05-de1fa1898ada" />




