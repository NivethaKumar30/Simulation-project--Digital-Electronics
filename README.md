# TITTLE

Design and simulate 2 bit synchronous upcounter with T flip flop using Verilog.

# THEORY

A 2-bit synchronous up-counter is a sequential circuit that counts sequentially from 00 to 11 and then wraps around back to 00. It has two output bits, representing the counter value. The counting operation is synchronized with a clock signal, meaning the counter increments its value only on a specific clock edge (e.g., rising edge or falling edge).

To implement a 2-bit synchronous up-counter using T flip-flops, you can follow these steps:

Step 1: Declare the input and output ports: clk: The clock signal used to synchronize the counting operation. reset: A reset signal that initializes the counter to 00. count[1:0]: The 2-bit output representing the counter value.

Step 2: Internal signals and flip-flops: Declare a 2-bit register to store the counter value, typically denoted as q. Declare a single-bit input for the T flip-flop, usually denoted as t.

Step 3: Instantiate T flip-flops and connect them: Instantiate two T flip-flops, one for each bit of the counter (q[1] and q[0]). Connect the clock signal (clk) and reset signal (reset) to each T flip-flop. Connect the output of the first flip-flop (q[0]) to the input of the second flip-flop (q[1]).

Step 4: Define the T input based on the counter value: Use a combinational logic circuit (e.g., an if-else statement) to determine the T input for the T flip-flops. When the counter is at the value 01, set the T input to 1. This will toggle the next flip-flop and increment the counter. For all other counter values, set the T input to 0, so the counter remains unchanged.

Step 5: Assign the counter value to the output: Assign the value of the 2-bit counter register (q) to the output ports (count[1:0]). By following these steps, you can implement a 2-bit synchronous up-counter using T flip-flops. The counter will increment its value on each clock edge, following the defined logic for the T input. The reset signal can be used to initialize the counter to 00, ensuring predictable behavior when the circuit starts.


# LOGIC DIAGRAM

![image](https://github.com/NivethaKumar30/Simulation-project--Digital-Electronics/assets/119559844/66456216-289d-4d25-bc6f-9558b30c986a)

# NETLIST DIAGRAM

![Screenshot (570)](https://github.com/NivethaKumar30/Simulation-project--Digital-Electronics/assets/119559844/8bcee6aa-71cb-434b-b016-47b9292394f7)

# TIMING DIAGRAM

![Screenshot (571)](https://github.com/NivethaKumar30/Simulation-project--Digital-Electronics/assets/119559844/50d28f8f-b285-4d8e-84fe-34df3bdf525e)

# PROGRAM
```
DEVELOPED BY: NIVETHA .K
REFRENCE NUMBER: 212222230102

module sp (clk,a);
input clk;
output  reg [1:0]a;
always@(posedge clk)
begin
   a[1]=(a[0])^a[1];
	a[0]=1^a[0];
end
endmodule
```
#REFERENCE:

https://github.com/NivethaKumar30/Simulation-project--Digital-Electronics/edit/main/README.md


# RESULT :

Thus , the 2 bit synchronous upcounter with T flip flop using Verilog in quartus 2 is executed sucessfully.
