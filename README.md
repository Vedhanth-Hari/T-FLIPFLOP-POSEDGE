# T-FLIPFLOP-POSEDGE

**AIM:**

To implement  T flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**T Flip-Flop**

T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/458a68fe-2d08-4a9d-ac4f-7ae0480ce0bd)

 
This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop. The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop. Inputs Present State Next State

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/cdd7fb32-539f-4b66-bb8d-f305a153c886)

 
From the above characteristic table, we can directly write the next state equation as Q(t+1)=T′Q(t)+TQ(t)′ ⇒Q(t+1)=T⊕Q(t)

**Truth Table**

![Screenshot 2024-12-24 221327](https://github.com/user-attachments/assets/12d87f2b-ce88-49dc-a6c8-6d17dd9ab297)

**Procedure**

/* 1.Type the program in Quartus software to implement the T Flip-Flop with positive edge-triggered clock using Verilog.

2.Compile and run the program to check for any errors.

3.Generate the RTL schematic to observe the generated logic circuit and save it for documentation.

4.Create input (T, clk) and output (Q, Q_bar) nodes in the simulation tool.

5.Simulate the design to generate the timing diagram for different combinations of input. */

**PROGRAM**

module tflip (t, clk, rst, q);

input t, clk, rst;

output reg q;

always @(posedge clk or posedge rst)

begin

if (rst)
  q <= 0; // Reset the flip-flop
else if (t==0)
  q <= q; 
 else
    q<=~q;
end

endmodule

/* Program for flipflops and verify its truth table in quartus using Verilog programming. Developed by:H.Vedhanth RegisterNumber:24003775
*/

**RTL LOGIC FOR FLIPFLOPS**

![Screenshot 2024-12-24 221348](https://github.com/user-attachments/assets/220b7e54-ffd4-4732-b982-8d286eed83d0)


**TIMING DIGRAMS FOR FLIP FLOPS**

![Screenshot 2024-12-24 221406](https://github.com/user-attachments/assets/1757c1a3-0dbe-4233-9497-15c4c7f67309)

**RESULTS**
Thus the given T flipflop using verilog and validating their functionality using their functional tables are verified.
