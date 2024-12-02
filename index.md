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

Describe the synthesis and implementation processes. Consider including 1/2 useful screenshot(s). Guideline: 1/2 short paragraphs.
<img src="https://raw.githubusercontent.com/Edmentos/SOC_Project/main/Images and videos/Design Runs.png">

### **Demonstration**
Perhaps add a picture of your demo. Guideline: 1/2 sentences.

## **My VGA Design Edit**
Introduce your own design idea. Consider how complex/achievabble this might be or otherwise. Reference any research you do online (use hyperlinks).
### **Code Adaptation**
Briefly show how you changed the template code to display a different image. Demonstrate your understanding. Guideline: 1-2 short paragraphs.
### **Simulation**
Show how you simulated your own design. Are there any things to note? Demonstrate your understanding. Add a screenshot. Guideline: 1-2 short paragraphs.
### **Synthesis**
Describe the synthesis & implementation outputs for your design, are there any differences to that of the original design? Guideline 1-2 short paragraphs.
### **Demonstration**
If you get your own design working on the Basys3 board, take a picture! Guideline: 1-2 sentences.

## **More Markdown Basics**
This is a paragraph. Add an empty line to start a new paragraph.

Font can be emphasised as *Italic* or **Bold**.

Code can be highlighted by using `backticks`.

Hyperlinks look like this: [GitHub Help](https://help.github.com/).

A bullet list can be rendered as follows:
- vectors
- algorithms
- iterators

Images can be added by uploading them to the repository in a /docs/assets/images folder, and then rendering using HTML via githubusercontent.com as shown in the example below.

<img src="https://raw.githubusercontent.com/melgineer/fpga-vga-verilog/main/docs/assets/images/VGAPrjSrcs.png">
