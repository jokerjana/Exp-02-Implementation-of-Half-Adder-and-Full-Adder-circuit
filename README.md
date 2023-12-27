```
Name :- Janrthanan B
Reg no :- 212223100014
```

# Exp-03 Implementation of Half Adder and Full Adder circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

### Theory 
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 

### Procedure
Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.

### Program 
```
module project_3(sum,carry,a,b); 
input a,b; 
output sum,carry; 
xor sum1(sum,a,b); 
and carry1(carry,a,b); 
endmodule
```

### RTL Realization
![image](https://github.com/jokerjana/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147173630/905aae8e-5826-488b-802c-695b2b665f9d)

### TIMING DIAGRAM
![image](https://github.com/jokerjana/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147173630/7713a9fb-4559-4f8d-91b9-79a05a5e3c45)

### TRUTH TABLE 
![image](https://github.com/jokerjana/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147173630/331d6544-1c93-473a-90e5-4b84fa2daff3)


### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER

### Program 
```
module project_3_2(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor(sum,a,b,c);
assign carry=a&b | b&c | a&c;
endmodule
```

### RTL Realization
![image](https://github.com/jokerjana/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147173630/1b3fadae-3859-43d1-8963-4baa009c2406)

### TIMING DIAGRAM
![image](https://github.com/Raji1009/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/89059861/6a11b3c6-dc53-400b-9a3d-5ebf6eac532a)

### TRUTH TABLE 
![image](https://github.com/Raji1009/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/89059861/a2d05afa-0f64-4906-9001-e9deb30f4f65)

### Result:
Thus the given logic functions are implemented and their operations are verified using verilog programming
