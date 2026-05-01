# Half adder- CMOS Design & Verilog Implementation
##Table Of Contents
1.Introduction
2.Truth Table
3.Logic Gates & Boolean Expressions
4.Circuit Diagram (Gate Level)
5.CMOS Implementation in LTspice
6.Verilog Code
7.Simulation Waveforms
8.Tools Used
9.How to Run

##Introduction
A Half Adder is one of the fundamental building blocks of digital arithmetic circuits. It performs binary addition of two single-bit inputs and produces two outputs:
Sum (S) — the result of the addition
Carry (C) — the overflow bit carried to the next significant position

Unlike a Full Adder, the Half Adder does not account for a carry input from a previous stage  hence the name half. Despite its simplicity, it forms the basis of all arithmetic logic units (ALUs) in modern processors.

This project demonstrates the Half Adder implemented in two ways:
CMOS transistor-level design — simulated using LTspice
Register Transfer Level (RTL) design — written in Verilog HDL and simulated using ModelSim

##Truth Table
The Half Adder operates on two binary inputs A and B:
<img width="393" height="255" alt="Truth-table-for-half-adder_W640" src="https://github.com/user-attachments/assets/8c60f294-1156-4320-ad05-de1fa1898ada" />

##Logic Gates and boolean experssion:
Sum= X^Y
Carry= X.Y

##Circuit Diagram:
<img width="768" height="320" alt="image" src="https://github.com/user-attachments/assets/466d5f52-8211-4147-aa12-5d16aa60f248" />

##CMOS Implementation:
The CMOS-level implementation uses complementary MOSFET pairs (PMOS + NMOS) to realize each logic gate.

##LTspice Schematic
<img width="1910" height="875" alt="Screenshot 2026-05-01 190211" src="https://github.com/user-attachments/assets/02235cc2-ae7c-4238-a2f1-5a40ecfa7da2" />

##LTspice waveform
<img width="1918" height="986" alt="Screenshot 2026-05-01 190140" src="https://github.com/user-attachments/assets/dec90cf4-5f23-49c2-951a-fec125b71a15" />

##Verilog code
Module half_adder.v

module half_adder(input a , input b , output sum ,output carry);
assign sum = a ^ b;
assign carry = a & b;

endmodule

##Module tb_half_adder.v


timescale 1ns/1ps
module tb_half_adder;
reg a,b;
wire sum,carry;
half_adder uut(.a(a),.b(b),.sum(sum),.carry(carry));
initial begin
a=0; b=0;
#10 a=0; b=1;
#10 a=1; b=0;
#10 a=1; b=1;
#10 $stop;
end
 
endmodule

##Simulation Waveforms
<img width="1915" height="992" alt="Screenshot 2026-04-24 233016" src="https://github.com/user-attachments/assets/d2b8f5e7-b693-44e2-bd0f-5ad7d025f2f2" />

##Tool Used 
LTspice- CMOS transitor level simulation 
ModelSim-Verilog HDL simulation& Waveforms




