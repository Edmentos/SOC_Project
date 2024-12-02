---
layout: home
title: FPGA VGA Driver Project
tags: fpga vga verilog
categories: demo
---

This is my project on FPGA VGA. I will show you the colourful images that I created and what I started from.

![A GIF showing The Different Colours](https://raw.githubusercontent.com/Edmentos/SOC_Project/main/IMG_1861.gif)
### **Project Set-Up**
The project setup was easy I had to plug in my board and get run my synthesis run my implementation generate a bitstream and program the board. It was that simple for me.
I know other people had problems choosing which board but because Michele had it on the Moodle I picked the right one first time. Above is a gif of what the first design looked like how it works. I made sure that I had all my sources in the right spot and I got that design pattern first time.

<img src="https://raw.githubusercontent.com/Edmentos/SOC_Project/main/Images and videos/Project Summary.png">

### **Template Code**
For the FPGA/VGA design above it uses a state machine which changes the state after every 0.5 seconds using the count and count to which counts every 67,108,864 clock cycles. Black,Red,Yellow,Green,Cyan,Blue,Magenta and white aare all states that gets the colour to show up using (colour <= 12'b000000001111;) this line of code and then it shows up on the screen.
Outline the structure and design of the Verilog code templates you were given. What do they do? Include reference to how a VGA interface works. Guideline: 2/3 short paragraphs, consider including screenshot(s).
<img src="https://raw.githubusercontent.com/Edmentos/SOC_Project/main/State_Machine.png">
### **Simulation**
Explain the simulation process. Reference any important details, include a well-selected screenshot of the simulation. Guideline: 1/2 short paragraphs.
When I tried to run the simulation for the colour stripes portion of the project I ran into a problem with my simulation. I never set my TestBench as top in my simulation sources. I set it as my top and then ran into another problem I hadnt spelled one of my sources right 

I tried to make a spiral pattern but I couldnt complete that on time and it was taking up too much of my time 
### **Synthesis**
Describe the synthesis and implementation processes. Consider including 1/2 useful screenshot(s). Guideline: 1/2 short paragraphs.
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
