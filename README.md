# Experimrnt-6:Synchornous-counters - up counter and down counter
### AIM: To implement 4 bit up and down counters and validate  functionality.
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 

## UP COUNTER :
The counter is a digital sequential circuit and here it is a 4 bit counter, which simply means it can count from 0 to 15 and vice versa based upon the direction of counting (up/down). 

The counter (“count“) value will be evaluated at every positive (rising) edge of the clock (“clk“) cycle.
The Counter will be set to Zero when “reset” input is at logic high.
The counter will be loaded with “data” input when the “load” signal is at logic high. Otherwise, it will count up or down.
The counter will count up when the “up_down” signal is logic high, otherwise count down

Since we know that binary count sequences follow a pattern of octave (factor of 2) frequency division, and that J-K flip-flop multivibrators set up for the “toggle” mode are capable of performing this type of frequency division, we can envision a circuit made up of several J-K flip-flops, cascaded to produce four bits of output.
The main problem facing us is to determine how to connect these flip-flops together so that they toggle at the right times to produce the proper binary sequence.
Examine the following binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1:
Binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1.

Note that each bit in this four-bit sequence toggles when the bit before it (the bit having a lesser significance, or place-weight), toggles in a particular direction: from 1 to 0.



 
 

Starting with four J-K flip-flops connected in such a way to always be in the “toggle” mode, we need to determine how to connect the clock inputs in such a way so that each succeeding bit toggles when the bit before it transitions from 1 to 0.

The Q outputs of each flip-flop will serve as the respective binary bits of the final, four-bit count:

 
 

Four-bit “Up” Counter
![image](https://user-images.githubusercontent.com/36288975/169644758-b2f4339d-9532-40c5-af40-8f4f8c942e2c.png)



## DOWN COUNTER :

As well as counting “up” from zero and increasing or incrementing to some preset value, it is sometimes necessary to count “down” from a predetermined value to zero allowing us to produce an output that activates when the zero count or some other pre-set value is reached.

This type of counter is normally referred to as a Down Counter, (CTD). In a binary or BCD down counter, the count decreases by one for each external clock pulse from some preset value. Special dual purpose IC’s such as the TTL 74LS193 or CMOS CD4510 are 4-bit binary Up or Down counters which have an additional input pin to select either the up or down count mode.
![image](https://user-images.githubusercontent.com/36288975/169644844-1a14e123-7228-4ed8-81a9-eb937dff4ac8.png)


4-bit Count Down Counter
### Procedure:
1.Create a new project in QuartusII software. 2.Name the project as uc for upcounter and dc for
down counter. 3.Create a new verilog hdl file in the project file. 4.Name the module as dc and uc for
down counter and up counter. 5.Within the module declare input and output variables. 6.Create a
loop using if-else with condition parameter as reset value. 7.End the loop. 8.End the module

### PROGRAM :

Developed by: Dharshini K 

RegisterNumber: 23010696

### Code:
### UP Counter:

![UPCOUNTER CODE](https://github.com/dharshini-29/Exp-7-Synchornous-counters-/assets/147474632/aa6e1857-91af-482b-8923-2855e151d1c4)

### Down Counter:

![DOWNCOUNTER CODE](https://github.com/dharshini-29/Exp-7-Synchornous-counters-/assets/147474632/0252fe2d-13b7-4fd6-b764-c92abeb6afed)


### OUTPUT:
### RTL DIAGRAM: 
### UP Counter:

![UPCOUNTER RTL](https://github.com/dharshini-29/Exp-7-Synchornous-counters-/assets/147474632/5469b58d-a0d2-4129-a077-0202e4feaf45)

### Down Counter:

![DOWNCOUNTER RTL](https://github.com/dharshini-29/Exp-7-Synchornous-counters-/assets/147474632/aec0abef-c009-4c03-b328-608530c81041)


### TRUTH TABLE :
### UP Counter:

![UP TT TABLE](https://github.com/dharshini-29/Exp-7-Synchornous-counters-/assets/147474632/f1937d6f-2f10-49b8-a4ed-35db6c626cac)

### Down Counter:

![DOWN TT](https://github.com/dharshini-29/Exp-7-Synchornous-counters-/assets/147474632/61527dc6-80a0-4b34-846b-de07fbfd8d06)


### TIMING DIGRAMS FOR COUNTER  
### UP Counter:

![UP TIME](https://github.com/dharshini-29/Exp-7-Synchornous-counters-/assets/147474632/c8f810fe-9f51-40c3-8b1d-75924901eaf3)

### Down Counter:

![THE REAL DOWN TIME](https://github.com/dharshini-29/Exp-7-Synchornous-counters-/assets/147474632/8e1fd8ce-439b-4cd1-84b9-7e790375760d)

### RESULTS :
Thus Synchornous counters up counter and down counter circuit are studied and the truth table for
different logic gates are verified.
