# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**

1.Initialize the shift register to a known state (e.g., all zeros).

2.Input a bit serially into the shift register.

3.Shift the contents of the register one position to the right (or left).

4.Output the shifted bit from the last stage of the register.

5.Repeat steps 2-4 for each bit you want to input and shift.

**PROGRAM**

```
module siso(din, clk, rst, dout);
 input din;
 input clk;
 input rst;
 output dout;
reg dout;
reg [7:0]x;
always @ (posedge(clk) or posedge(rst)) begin
if (rst==1'b1)
begin
dout=8'hzz;
end
else
begin
x={x[6:0],din};
dout=x[7];
end
end
endmodule
```
Developed by: MITRAN R

RegisterNumber:24006381

**RTL LOGIC FOR SISO Shift Register**

![10](https://github.com/user-attachments/assets/a3057f9a-e56d-4ffb-a24e-b85299bc81e4)

**TIMING DIGRAMS FOR SISO Shift Register**

![10 1](https://github.com/user-attachments/assets/0a7e51be-00c0-4b4e-ac0a-006632ca6ddd)

**RESULTS**

SISO Shift Register using verilog and validating their functionality using their functional tables has successful execution of the program.
