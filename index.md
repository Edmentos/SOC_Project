---
layout: home
title: FPGA VGA Driver Project
tags: Edmond Wilkinson
categories: demo
---

This is my project on FPGA VGA. I will show you the colourful images that I created and what I started from.

![A GIF showing The Different Colours](https://raw.githubusercontent.com/Edmentos/SOC_Project/main/IMG_1861.gif)
### **Project Set-Up**
The project setup was easy I had to plug in my board and get run my synthesis run my implementation generate a bitstream and program the board. It was that simple for me.
I know other people had problems choosing which board but because Michele had it on the Moodle I picked the right one first time. Above is a gif of what the first design looked like how it works. I made sure that I had all my sources in the right spot and I got that design pattern first time.

<img src="https://raw.githubusercontent.com/Edmentos/SOC_Project/main/Images and videos/Project Summary.png">

### **Template Code**
For the FPGA/VGA design above it uses a state machine which changes the state after every 0.5 seconds using the count and count to which counts every 67,108,864 clock cycles. Black,Red,Yellow,Green,Cyan,Blue,Magenta and white are all states that gets the colour to show up using (colour <= 12'b000000001111;) this line of code and then it shows up on the screen.
<img src="https://raw.githubusercontent.com/Edmentos/SOC_Project/main/State_Machine.png">

The colour cycle instance provided here initialises the different variables and the different colours from my understanding and uses them inside the colour cycle to make sure that the counter goes up and the number that it counts to is initialised and resets the counter once the counter reaches the assigned time. The parameters are initialised at the very start of the module.
<img src="https://raw.githubusercontent.com/Edmentos/SOC_Project/main/Images and videos/TestBench.png">

### **Simulation**
Explain the simulation process. Reference any important details, include a well-selected screenshot of the simulation. Guideline: 1/2 short paragraphs.
When I tried to run the simulation for the colour stripes portion of the project I ran into a problem with my simulation. I never set my TestBench as top in my simulation sources. I set it as my top and then ran into another problem I hadnt spelled one of my sources right. The screenshot that I have included shows the values of each of the my variables over time using the simulation I was able to make sure throughout the week without a programme board that my designs would work as the values change over the course of time in my simulation. 
<img src="https://raw.githubusercontent.com/Edmentos/SOC_Project/main/Images and videos/Simulation.png">
I tried to make a spiral pattern but I couldnt complete that on time and it was taking up too much of my time. Unfortunately I lost the screenshots of my code that I was working on but I got my inspiration from a multitude of youtube videos https://youtube.com/playlist?list=PLtChGkQ0aIK-gBHwiymN0nBvCj7Z_Cyoa&si=-tTw3waGaRIRp3pa that is a link to the youtube playlist that I got my inspiration from. The most I could do is get a box to show up on my screen but i couldnt get it to move in the spiral that I wanted.

### **Synthesis**

With the Vivado Design Suite the proccess for synthesis and implementation Is stimple. As long as your code works and everything is running properly synthesis is just one click away. Once my synthesis had ran it the image below showed me alot of data. In the methodology section it showed me that I had 2 critical warnings and 13 warnings for my code. which sounds like alot but it was the same without any changes to the code my guess is that the updated version of vivado cant run the old code.
The implementation is just as easy with just one click I was able to generate my bitstream. The annoying part is that everytime i tried to run my code i had to generate my bitstream and that might take a minute. each change for my swirl design got longer and longer to generate a bitstream because the code got longer and longer. The whole process for everything was easy enough due to the Vivado Design Suite. 
<img src="https://raw.githubusercontent.com/Edmentos/SOC_Project/main/Images and videos/Design Runs.png">

### **Demonstration**
Finally, I programmed the FPGA board with the design. Below is an image of the Irish flag displayed on the VGA screen. This is done by splitting the screen into 3 and changing the colour of the section to green white and orange. This is done by getting the hex code of the colour and inputting it into the section. Unfortunatly I tried to change the code to get multiple different flags on the screen and I somehow lost my original code and was unable to get it back to a working state.
This project helped me understand how to manipulate pixel coordinates and colors to create custom VGA outputs.
<img src="https://raw.githubusercontent.com/Edmentos/SOC_Project/main/IMG_1939.jpg">

## **My VGA Design Edit**
My own design idea was orignially a spiral pattern, it was supoosed to be like those toys that you would put a pencil into and spiral around the page but after seeing how complex that would be I instead decided to focus on simpler designs. I got an Irish flag to show up and then went to try and have it so that the flag would change into another flag after a short period of time this turned out to be harder than I expected and I had to get some help from my fellow classmates. Alex was the person to point out that I was using the wrong file to try get something changing as i was using a stativ file that never changed. I changed to the colourcycle and tried to get that running but unfortunatly I ran out of time.
### **Code Adaptation**
I changed the original code for the colourstripes.v file to display an Irish flag. This posed a bit of a challenge as i had to learn what everything meant in that file. I found out how to change the size of the portion of the screen and that the screen was 680units long. This then made it easy to change the screen into three equal parts after a bit of messing around to get it equal.
I then changed the colour associated with that section by getting the hex code for the colours 
Briefly show how you changed the template code to display a different image. Demonstrate your understanding. Guideline: 1-2 short paragraphs.
### **Simulation**
Show how you simulated your own design. Are there any things to note? Demonstrate your understanding. Add a screenshot. Guideline: 1-2 short paragraphs.
### **Synthesis**
Describe the synthesis & implementation outputs for your design, are there any differences to that of the original design? Guideline 1-2 short paragraphs.
### **Demonstration**
If you get your own design working on the Basys3 board, take a picture! Guideline: 1-2 sentences.

