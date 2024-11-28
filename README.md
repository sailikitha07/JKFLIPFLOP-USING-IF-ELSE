# JKFLIPFLOP-USING-IF-ELSE

**AIM:** 

To implement  JK flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**
The JK Flip-Flop is a sequential circuit element that eliminates the indeterminate state of the SR Flip-Flop and supports toggling functionality. It operates with two inputs, J (set) and K (reset), along with a clock signal, producing outputs Q and Q̅. The flip-flop’s functionality is defined by its truth table, where the outputs depend on the combination of J and K. It is widely used in counters, frequency division, and shift registers.
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
1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**PROGRAM**

```

/* Program for flipflops and verify its truth table in quartus using Verilog programming.
 Developed by:sai likitha RegisterNumber:24009865
module jkffgate(q, qbar, j, k, clk);
input j, k, clk; 
output q, qbar;
wire nand1_out;
wire nand2_out;
nand (nand1_out, clk, j, qbar); 
nand (nand2_out, clk, k, q); 
nand (q, nand1_out, qbar);
nand (qbar, nand2_out, q);
endmodule
*/

```

**RTL LOGIC FOR FLIPFLOPS**
![Screenshot 2024-11-28 182649](https://github.com/user-attachments/assets/1ebaafec-263f-4f2d-aab9-79a2224a358b)

**TIMING DIGRAMS FOR FLIP FLOPS**
![Screenshot 2024-11-28 204801](https://github.com/user-attachments/assets/0aac5142-5095-42b5-ab15-6d1405710807)

**RESULTS**
Thus to implement JK flipflop using verilog and validating their functionality using their functional tables done successfully.
