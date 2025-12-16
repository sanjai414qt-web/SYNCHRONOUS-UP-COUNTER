### SYNCHRONOUS-UP-COUNTER
**Date:16/12/2025**

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**

/* write all the steps invloved */

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 
```
module ex11(out,clk,rst);
input clk,rst;
output reg [3:0]out;
always @ (posedge clk)
begin
   if(rst)
     out<=0;
   else 
     out <= out+1;
end
endmodule
```
Developed by:Sanjai K RegisterNumber:25018325
*/

**RTL LOGIC UP COUNTER**
<img width="974" height="407" alt="Screenshot 2025-12-16 161228" src="https://github.com/user-attachments/assets/978210e5-e896-4a3e-9cfb-7b4d509e3ba0" />

**TIMING DIAGRAM FOR IP COUNTER**
<img width="1233" height="278" alt="Screenshot 2025-12-16 161248" src="https://github.com/user-attachments/assets/a912185b-e065-42ad-9038-a67e9d2cdc16" />

**TRUTH TABLE**

![Truthtable](https://github.com/user-attachments/assets/ead9a162-74fc-4da5-84a5-aa37ff9311e8)

**RESULTS**
Thus the Synchronous Up  Counter using verilog and validating their functionality using their functional tables is verified

.
.
.

.

.

.


.

.

.
.

.
.
.
.
.
.

.
.
.
.
.
.
.

.
.
.

.
.
.
.
.

.
.
.
.


.
.

..


.

.
.
.
.
.
.
.
.


.

.
.
.
.
.

.
.
.
.
.
.
.

..

.

.
.
.

.

.
.
.
.

.
.
.
.

.
.
.

.
.

.
.
.
.
.

.
.
..

.
.
.

.


.

.
.
.
.
.
.

.
.

.
.
.

.
.
.

.
.
.
.

.
.

.
.
.
.


.
.

.
.

.
.
.


.

.
.
.


.
.

.

.
.


.

.
.

..

.


.


.
.

.

.
.
.
.
.

.
.
.
.
.

.
..

