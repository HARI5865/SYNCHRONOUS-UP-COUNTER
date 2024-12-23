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

**Procedure**<br>
1.Type the program in Quartus software.<br>

2.Compile and run the program.<br>

3.Generate the RTL schematic and save the logic diagram.<br>

4.Create nodes for inputs and outputs to generate the timing diagram.<br>

5.For different input combinations generate the timing diagram.<br>

/* write all the steps invloved */<br>

**PROGRAM**<br>
module exp11(out, clk,rstn);<br>
 input clk,rstn; <br>
 output reg [3:0]out; <br>
 always @ (posedge clk) <br>
 begin<br>
  if(!rstn)<br>
    out<=0;<br>
  else<br>
	 out <= out+1;<br>
 end<br>
 endmodule<br>

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by:Lokesh M<br> RegisterNumber:24900227
*/

**RTL LOGIC UP COUNTER**<br>
![Screenshot 2024-12-23 140028](https://github.com/user-attachments/assets/aae8cbd0-c33d-4917-9fe2-5bf8d3e1d851)


**TIMING DIAGRAM FOR IP COUNTER**<br>
![Screenshot 2024-12-23 140041](https://github.com/user-attachments/assets/81b41bf0-8f50-4446-9249-be2c0565c935)


**TRUTH TABLE**<br>

**RESULTS**<br>
To implement 4 bit synchronous up counter and validate functionality is verified successfully.
