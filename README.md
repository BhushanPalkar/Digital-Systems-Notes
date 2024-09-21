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
* **Priority encoders are used to differentiate, when all the i/p lines are 0 and when x0 is 0 (as it produces same output)**
* 






















