# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![Screenshot 2023-11-27 213937](https://github.com/MangariDeeraj/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365485/bf06c40c-c0d6-441c-8e66-079381197439)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.

![Screenshot 2023-11-27 213951](https://github.com/MangariDeeraj/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365485/58fb1874-c701-4338-aa7d-19a6e8ba2e7a)



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State

![Screenshot 2023-11-27 214055](https://github.com/MangariDeeraj/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365485/d85c167a-8c52-43eb-b110-015cf03983c3)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.


 ![WhatsApp Image 2023-11-28 at 10 10 25_6c276f62](https://github.com/MangariDeeraj/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365485/5b027433-9546-4f3a-b7fb-7ab580ecb33e)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![Screenshot 2023-11-22 134417](https://github.com/MangariDeeraj/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365485/1b70b77f-36ba-4f2b-9e3c-3cca776de89d)


![Screenshot 2023-11-22 140021](https://github.com/MangariDeeraj/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365485/e18413e3-6484-4f32-8116-fdaae92af334)


Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D


![Screenshot 2023-11-22 134513](https://github.com/MangariDeeraj/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365485/ddc8e6f5-07dc-4f52-910c-5a0290b0c4e8)


Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.
![WhatsApp Image 2023-11-28 at 10 10 41_30152e47](https://github.com/MangariDeeraj/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365485/2898619c-e6ee-42d3-b33f-0071b92d2945)


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

 ![Screenshot 2023-11-22 142318](https://github.com/MangariDeeraj/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365485/c5e6d130-6b83-49c0-9871-9a0aed4cf8c1)

This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.

![Screenshot 2023-11-22 142335](https://github.com/MangariDeeraj/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365485/a0083a58-06a1-4d7f-8966-49f9dd36a963)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![Screenshot 2023-11-22 142510](https://github.com/MangariDeeraj/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365485/dc2ba6db-4c94-4ca1-a24f-ccc9f60752d9)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 ![WhatsApp Image 2023-11-28 at 10 11 02_49690dbe](https://github.com/MangariDeeraj/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365485/9fd190d1-4bcb-484e-acd8-53bd340d0a73)


The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
/* write all the steps invloved */



### PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: 
RegisterNumber:  
*/






### RTL LOGIC FOR FLIPFLOPS 









### TIMING DIGRAMS FOR FLIP FLOPS 








### RESULTS 
