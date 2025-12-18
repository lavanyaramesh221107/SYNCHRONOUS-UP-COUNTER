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

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 
```module up_counter (out,clk,rst);
input clk,rst;
output reg [3:0]out;
always @ (posedge clk)
begin
	if(!rst)
		out<=0;
	else 
		out <= out+1;
end
endmodule
```
Down counter
```
module down_counter (out,clk,rst);

input clk,rst; 

output reg [3:0]out;

always @ (posedge clk)

begin

if(!rst)

out<=4'b1111;

else 

out <= out-1;

end

endmodule
````

Developed by:Lavanya R 
RegisterNumber:25017651
*/

**RTL LOGIC UP COUNTER**
![WhatsApp Image 2025-12-18 at 10 01 45 AM](https://github.com/user-attachments/assets/d280d206-fde0-4ab6-bcd1-2d6bce82be74)
**RTL LOGIC DOWN COUNTER**
![WhatsApp Image 2025-12-18 at 10 01 47 AM](https://github.com/user-attachments/assets/7be9e4c2-68d5-4c01-abef-bb25dfb7b85f)




**TIMING DIAGRAM FOR UP COUNTER**
![WhatsApp Image 2025-12-18 at 10 01 46 AM](https://github.com/user-attachments/assets/7b47c9a9-bf3d-40f9-b5a7-e23fc4966eca)
**TIMING DIAGRAM FOR DOUN COUNTER**
![WhatsApp Image 2025-12-18 at 10 01 49 AM](https://github.com/user-attachments/assets/50f79c5a-d22d-41e6-9842-c08e61970db8)




**TRUTH TABLE**

![WhatsApp Image 2025-12-18 at 10 01 50 AM](https://github.com/user-attachments/assets/ca3766f8-1802-469e-972c-8d170b6d4013)


**RESULTS**
