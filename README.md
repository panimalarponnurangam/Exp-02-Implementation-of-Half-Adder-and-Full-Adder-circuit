# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
~~~
module Halfadder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule

module Fulladder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule 

/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: panimalar.p
RegisterNumber: 22009107 
*/
~~~

### Output:
### RTL realization
![Screenshot (78)](https://user-images.githubusercontent.com/121490826/214031686-3c1c3d1e-7c61-45ec-b96a-a76a97172bdb.png)
![Screenshot (79)](https://user-images.githubusercontent.com/121490826/214032094-89586b48-6118-46e3-9c54-035a4ddad51a.png)

### TIMING DIAGRAM
![Screenshot (80)](https://user-images.githubusercontent.com/121490826/214032581-ad23e8dc-1f3f-4ee9-a9d9-5a6f3eee15b3.png)

![Screenshot (81)](https://user-images.githubusercontent.com/121490826/214032852-ee05b842-de7b-4438-98cf-308f49dfd0bf.png)
\

### TRUTH TABLE 
![Screenshot (83)](https://user-images.githubusercontent.com/121490826/214037247-58b1c161-8b16-4328-a682-c1e8f2694f1e.png)
![Screenshot (70)](https://user-images.githubusercontent.com/121490826/214037376-a0474bea-8477-43f9-baae-f8c68cdc0f73.png)


### Result:
thus the output for the half adder and full adder are successfully done
