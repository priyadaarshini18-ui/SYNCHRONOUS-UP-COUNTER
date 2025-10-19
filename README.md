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
module up_counter_4bit ( input clk, // Clock signal input reset, // Reset signal (active high) output reg [3:0] q // 4-bit counter output );

always @(posedge clk or posedge reset) begin if (reset) q <= 4'b0000; // Reset counter to 0 else q <= q + 1; // Increment counter on each clock pulse end

endmodule

endmodule**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by:priyadaarshini.v RegisterNumber:25013541
*/

**RTL LOGIC UP COUNTER**
<img width="1066" height="553" alt="image" src="https://github.com/user-attachments/assets/1653f905-42f5-47f4-9993-0217ae0e4d6a" />



**TIMING DIAGRAM FOR IP COUNTER**
<img width="1056" height="537" alt="image" src="https://github.com/user-attachments/assets/d2ce13aa-6b03-4aa7-a458-64a66a98f9c4" />



**TRUTH TABLE**
<img width="667" height="681" alt="image" src="https://github.com/user-attachments/assets/28f5f578-55dd-4f56-b120-21b4a7041026" />


**RESULTS**
Thus 4-BIT-SYNCHRONOUS-COUNTER is verified sucessfully.
