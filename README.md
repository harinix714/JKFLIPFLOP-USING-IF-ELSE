# JKFLIPFLOP-USING-IF-ELSE

**AIM:** 

To implement  JK flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**JK Flip-Flop**

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/a649c30b-232b-4558-b188-fd6c09845180)


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/c4360742-e8a8-4937-b089-c46c0433f9a3)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/6c275261-a6d5-4c37-a3a7-1e88ca11c4cd)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/5174f41b-0ce0-4329-a372-6d1943ea6673)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

**Procedure**

/* write all the steps invloved */

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming
 Developed by:Harini S K
 RegisterNumber:25018849
module jkflipflop ( input J, K, clk, reset, output reg Q ); always @(posedge clk or
 posedge reset) begin if (reset) Q <= 0; // Reset the flip-flop else begin case ({J,K}) 2'b00:
 Q <= Q; // No change 2'b01: Q <= 0; // Reset 2'b10: Q <= 1; // Set 2'b11: Q <= ~Q; //
 Toggle endcase end end endmodule


**RTL LOGIC FOR FLIPFLOPS**


<img width="803" height="372" alt="Screenshot 2025-10-20 161431" src="https://github.com/user-attachments/assets/ca717c53-4d49-45fb-bad6-ad791e672644" />


**TIMING DIGRAMS FOR FLIP FLOPS**

<img width="1171" height="653" alt="Screenshot 2025-10-20 161455" src="https://github.com/user-attachments/assets/0c089813-ae34-4998-bd33-8c7bda08e1c3" />



**RESULTS**

 Thus the JK flipflop is implemented and verified
