# SR-FLIPFLOP-USING-CASE

**AIM:**

To implement  SR flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

SR Flip-Flop SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/0f710028-ad52-4d3e-9276-8714cf023a25)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of SR flip-flop.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/dabfc4f4-87e3-4cbc-9472-f89ee1b5ed30)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop. Present Inputs Present State Next State

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/dd90d16c-aec5-4290-a586-e2346b1e9eb5)

 
By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/473efad6-d70b-4ca7-aeb7-898bbfca319f)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)

**Procedure**

/* write all the steps invloved */
Step 1: Open Quartus II in your laptop.

Step 2: Write code to implement SR flipflop using verilog and validating their functionality using their functional tables.

Step 3: Run compilation to check for errors.

Step 4: Open waveform output and load input values.

Step 5: Run simulation to get the output.

Step 6: Open in RTL viewers to get RTL diagram output.

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. Developed by:gokul prasad h RegisterNumber:21224050011
*/
```
module sr_ff(s,r,clk,q,qbar);
input s,r,clk;
output reg q;
output reg qbar;
initial
begin
q=0;
qbar=1;
end
always @(posedge clk)
begin
q=s|(~r&q);qbar=r|(~s&~q);
end
endmodule
```

**RTL LOGIC FOR FLIPFLOPS**
![Screenshot (86)](https://github.com/user-attachments/assets/4dc2a759-1699-45f9-b105-f8852233b071)

**TIMING DIGRAMS FOR FLIP FLOPS**
![Screenshot (87)](https://github.com/user-attachments/assets/c36cb9be-62cf-4044-b218-dc62f8afd861)

**RESULTS**
Thus the program to implement a SR flipflop using verilog and validating their functionality using their functional tables is successfully completed
