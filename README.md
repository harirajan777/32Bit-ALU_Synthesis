# 32Bit-ALU_Synthesis

## Aim:

Synthesize 32 Bit ALU design using Constraints and analyse area and Power reports.

## Tool Required:

Functional Simulation: Incisive Simulator (ncvlog, ncelab, ncsim)

Synthesis: Genus

### Step 1: Getting Started

Synthesis requires three files as follows,

◦ Liberty Files (.lib)

◦ Verilog/VHDL Files (.v or .vhdl or .vhd)

Creating Source Code:

Verilog code:

module alu_32bit_case(y,a,b,f);

input [31:O]a;

input [31:0]b;

input [2:0]f;

output reg [31:0]y;

always@(*)

begin

case(f)

3'b000:y=a&b; //AND Operation

3'b001:y=alb; //OR Operation

3'b010:y=~(a&b); //NANO Operation

3'b011:y= ~(alb); //NOR Operation

3'b100:y=a"b; //XOR Operation

3'b101:y=~(a"b); //XNOR Operation

3'b110:y=~a; //NOT of a

3'b111:y=~b; //NOT of b

endcase

end endmodule

### Step 2 : Performing Synthesis

The Liberty files are present in the library path,

• The Available technology nodes are 180nm ,90nm and 45nm.

• In the terminal, initialise the tools with the following commands if a new terminal is being
used.

◦ csh

◦ source /cadence/install/cshrc

• The tool used for Synthesis is “Genus”. Hence, type “genus -gui” to open the tool.

• Genus Script file with .tcl file Extension commands are executed one by one to synthesize the netlist.

#### Synthesis RTL Schematic :
![Screenshot 2024-11-23 164045](https://github.com/user-attachments/assets/bedd7a6b-b1fa-480a-8441-45d8b1e29933)

#### Area report:
![Screenshot 2024-11-23 164109](https://github.com/user-attachments/assets/a1eec007-428b-43e8-888c-fd4ca20d1a89)

#### Power Report:
![Screenshot 2024-11-23 164126](https://github.com/user-attachments/assets/3bfd594c-1e65-4e80-87ce-87fc1ee6814a)

![Screenshot 2024-11-23 164139](https://github.com/user-attachments/assets/fc34c413-e850-4af5-9afe-e57b54d95939)

#### Result: 

The generic netlist of 32 bit ALU  has been created, and area, power reports have been tabulated and generated using Genus.
