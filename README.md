### SYNCHRONOUS-UP-COUNTER

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
```
``` 
Step1: Define the specifications and initialize the design. 
Step2: Declare the name of the entity and architecture by using VHDL source code. 
Step3: Write the source code in VERILOG. 
Step4: Check the syntax and debug the errors if found, obtain the synthesis report. 
Step5: Verify the output by simulating the source code. 
Step6: Write all possible combinations of input using the test bench. 
Step7: Obtain the place and route report

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by:VEMBARASI.A.R. RegisterNumber:24900729
```
```
module EX11(out,clk,rst);
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

*/

**RTL LOGIC UP COUNTER**
![Screenshot (130)](https://github.com/user-attachments/assets/50683804-4788-4e9f-8dad-2b195b94a440)


**TIMING DIAGRAM FOR UP COUNTER**
![Screenshot (131)](https://github.com/user-attachments/assets/19ed7cc4-2ce2-4082-8347-68bc22cc23de)


**TRUTH TABLE**

![Screenshot (48)](https://github.com/user-attachments/assets/5b75a021-c54f-467e-9463-85ea3e4fe0b4)


**RESULTS**
Thus the OUTPUT’s of Synchronous UP counter are verified by synthesizing and 
simulating the  VERILOG code.

