# Digital-Systems-Notes

__Combinational Logic__
* No feedback
* present output depends on present input only
* Faster in operation

 __Sequential Logic__
* Present Output depends on present input and past stateof the circuit
* slower in operation
* Complex design

**Minterm and Maxterm**
* A minterm is a product term. 
* A maxterm is a sum term.
* Example for a 3-input Boolean function:
* There are 2^3 = 8 possible minterms and 8 possible maxterms.
* For example, the minterm for the input combination A=1, B=0, C=1 is A.B'.C.
* The corresponding maxterm for this input combination is A'+B+C'.
* **SOP: A Boolean function can be expressed as a sum of minterms. Each minterm represents a combination of input variables that produces a 1 output.
    POS: A Boolean function can also be expressed as a product of maxterms. Each maxterm represents a combination of input variables that produces a 0 output.**
  
__Half addeer__
1+1= 1 1

![image](https://github.com/user-attachments/assets/ad306b0e-9cbe-4e75-8bb9-2bf07e7f88b5)

app: Digital circuits: Half-adders can be used in various digital circuits, such as counters, registers, and decoders.

__Half Subtractor__

0-1 = 1 1

![image](https://github.com/user-attachments/assets/cb3c19af-b73b-4945-afed-0f14a1ae6e30)

App:Signal Processing: Half-subtractors are used in various digital signal processing applications, such as filtering, modulation, and demodulation.

__Full Adder__

![image](https://github.com/user-attachments/assets/5d828326-a2c7-4118-b765-49a41c56b21c)

App:Counters are used to count events or measure time intervals.
They often employ full adders to increment or decrement the count.

__Full Subtractor__
0-1-1= 0 1

![image](https://github.com/user-attachments/assets/4b9c9d02-3f1d-4856-a518-4a84c840ed12)

App: Comparators: Full subtractors can be used to compare two numbers. By subtracting one number from the other and checking the result, it is possible to determine if the numbers are equal, greater than, or less than each other.


**IC-7483- 4 bit parallel addition (4 full adders)**

__Adder/Subtractor using 7483__

![image](https://github.com/user-attachments/assets/424b2d35-7631-4669-8c61-e45f88e3aad0)

XOR : 0+0=0;
1+1=0

if Cin is 0 whatever input will be passed 

if Cin is 1 input will be complimented (**2's compliment addition is equivalent to subtraction**)

__Digital Comparators__

App: DACs use comparators to convert digital signals into analog signals.
The comparator compares the digital input with a reference voltage to determine the output analog voltage.

__Carry-Lookahead Adder__
 pre-calculating carry-outs, look-ahead carry adders can significantly reduce the carry propagation delay, resulting in faster addition operations.

 App: In cryptographic algorithms, look-ahead carry adders are used for various operations, such as modular arithmetic and encryption/decryption.


![image](https://github.com/user-attachments/assets/607a9d0b-452b-423e-9426-b1fd0e569097)

* C output = A.B + A(XOR)B. Cin (**Based on Truth table of CARRY of Full adder**)
* C=g + p.Cin

__MULTIPLEXER__

They allow multiple data inputs to be selected and routed to a single output based on a control signal.

* Signal Multiplexing: They can be used to combine multiple signals onto a single channel, reducing the number of required wires or transmission lines.

![image](https://github.com/user-attachments/assets/fa730153-794d-4cd2-b81e-fcc3a75c4040)

For 8:1 MUX, we use two 4:1 MUX which has 3 select lines, where 1 select line acts as ENABLE input.

* MINTERMS : SOP
* MAXTERMS : POS
* MUX produces SOP equation

__Decoder__(IC-74139)

![image](https://github.com/user-attachments/assets/379fd618-6d46-433a-8d25-2fa0c5a5786b)

* decoder produces series of minterms (ANDed OUT)
* ACTIVE LOW outputs


**full adder using 3:8 decoder** 

![image](https://github.com/user-attachments/assets/4b34223a-ad20-4065-bf07-bce85f338419)


__Encoder__(IC - 74147)

![image](https://github.com/user-attachments/assets/ba652d36-b72d-49f3-97a6-38521e6209ae)

* encoders produce series of MAXTERM (ORed out)
* ACTIVE HIGH outputs
* **Priority encoders are used to differentiate, when all the i/p lines are 0 and when D0 is 0 (as it produces same output)**

## FlIP FLOPS (CLK i/p)

* SR (Set-Reset) Flip-Flop: A simple flip-flop with two inputs (Set and Reset) and one output (Q). It can be set to 1 or reset to 0.
* D (Data) Flip-Flop: A clocked flip-flop that stores the data present at the D input **(stores data based on clock pulse)** when the clock signal rises or falls.
* JK Flip-Flop: A clocked flip-flop with two inputs (J and K) and one output (Q). It can be set, reset, or toggle **(when set and reset are triggered at the same time)** its output depending   on the input values and clock signal.
* T (Toggle) Flip-Flop: A clocked flip-flop that toggles its output (changes to the opposite state) on each rising or falling edge of the clock signal.
  
Applications of Flip-Flops:
* Registers: Flip-flops are used to create registers, which are groups of flip-flops used to store data.**(D type flip flops are used)**
* Counters: Counters are digital circuits that count events or measure time. They often use flip-flops as their basic building blocks.**(JK flip flops are used)**

  __SR Latch:__

* Asynchronous: An SR latch does not have a clock input. It changes state immediately in response to changes on the S (Set) and R (Reset) inputs.
* Unstable States: If both S and R inputs are high at the same time, the output becomes undefined or unstable. This is known as a "forbidden state."
  SR Flip-Flop:

![image](https://github.com/user-attachments/assets/595fc501-1760-440c-9ba2-81e839433f04)

Disadvatges: The flip flop enters forbidden state if both S & R are high -> This is overcomed by using D and JK flip flop

__JK FLIP FLOP__

* The output changes on the rising and falling edge of the clock pulse

  ![image](https://github.com/user-attachments/assets/f62c4574-1388-4d1c-822e-8f2ea05c12fd)

From the TT 
* if JK is 0 0 = prev state
* 0 1 = Reset
* 1 0 = Set
* 1 1 = Toggle previous state (which was not defined for SR latch)

  ![image](https://github.com/user-attachments/assets/7177208f-4c2e-48ee-89d0-d1f5484ff230)

Con: TRACE AROUND CONDITION- When J&K are 1 1 and clk is HIGH, the prev state of the output is unknown in order to toggle.






















