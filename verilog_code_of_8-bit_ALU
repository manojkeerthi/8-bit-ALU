`timescale 1ns / 1ps
//////////////////////////////////////////////////////////////////////////////////
// Company: 
// Engineer: 
// 
// Create Date: 13.08.2025 00:08:27
// Design Name: 
// Module Name: ALU_8bit
// Project Name: 
// Target Devices: 
// Tool Versions: 
// Description: 
// 
// Dependencies: 
// 
// Revision:
// Revision 0.01 - File Created
// Additional Comments:
// 
//////////////////////////////////////////////////////////////////////////////////


module ALU_8bit(opcode,A,B,OutALU,Cout);
input wire [2:0] opcode;
input wire [7:0] A;
input wire [7:0] B;
output reg [15:0] OutALU;
output reg Cout;
parameter Add=3'b000,Sub=3'b001,Mul=3'b010,Lsh=3'b011,Rsh=3'b100,AND=3'b101,OR=3'b110,XOR=3'b111;
reg [8:0] temp;
always @(opcode)
case(opcode)
Add:begin
        assign temp = A+B;
        assign OutALU=temp;
        assign Cout=temp[8]; end
Sub:assign OutALU = A-B;
Mul:assign OutALU = A*B;
Lsh:assign OutALU = A << 1;
Rsh:assign OutALU = A >> 1;
AND:assign OutALU = A & B;
OR:assign OutALU = A | B;
XOR:OutALU = A ^ B;
default: assign OutALU = 0;
endcase
endmodule
