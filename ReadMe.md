# Simon Game
#### This module is designed for implementation in CPLD modules.
##### by CADcom from SKEL 4273 UTM, supervised by AP. Muhammad Mun`im Ahmad Zabidi



***
***
## What is Simon Game?
***
Simon game is an electronic game of memory skill invented by Ralph H. Baer and Howard J. Morrison, working for toy design firm Marvin Glass and Associates, with software programming by Lenny Cope. The device creates a series of tones and lights and requires a user to repeat the sequence.

### **Description of Game**
The game is played by repeating the sequence of lights shown using the associated touch pads. There are four different sections of lights, each with its own color and tone.
The Simon Game have five major state: 
1.	Idle State
2.	Auto-display state: display the current LEDs sequence
3.	Game state: read the pressed button and check whether input match the displayed sequence
4. 	Step-Up state: moving to the next level after winning that sequence.
5. Win state: display the “win” sounds and and “win” sequence.

Once user lose the sequence, it will back to idle state.




### rtl-ASM chart
***
![rtl_asmchart](https://user-images.githubusercontent.com/69129985/124562114-3a8e3100-de71-11eb-9be1-286e883d246f.png)

## Simon Game

### Functional Block Diagram
<img width="448" alt="SimonGame_FBD" src="https://user-images.githubusercontent.com/69129985/124562310-75906480-de71-11eb-9568-9c9577d38612.PNG">




## Datapath Unit 
Datapath unit is combination of several modules and behavioural modelling. The modules invovled are:


| Modules | Description|
|---      | -----      |
| Memory  | A accessible memory used to store the random input for the sequence.|
| Counter | A 5-bit counter which will provide address to the memory.|
| Randomizer| A 2-bit counter which uses smaller scale of clock frequency to achieve random output and provides to the memory input.|
| Display | A 2-to-4 decoder for LED display|
| Encoder | A 4-to-3 encoder which encodes the button's input|
| Comparator| Used to compare 2 bit data|
***


Functional block diagram ( some signals are abstracted to reduce clutter):
![fbd_DU](https://user-images.githubusercontent.com/69129985/124562370-88a33480-de71-11eb-9235-d7bb5cee3938.png)

## Control Unit
Functional block diagram:
![fbd_CU](https://user-images.githubusercontent.com/69129985/124562401-9062d900-de71-11eb-93b2-2a1980ec183e.png)



