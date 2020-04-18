 # Multiplexer
Multiplexing is the property of combining one or more signals and transmitting on a single channel. You will get a sense of what that means as you read this tutorial. This is achieved by the device multiplexer. A multiplexer is the most frequently used combinational circuits and important building block in many in digital systems.

There are four types of Multiplexers
 
 * 2-1 multiplexer ( 1select line)
 * 4-1 multiplexer (2 select lines)
 * 8-1 multiplexer (3 select lines)
 * 16-1 multiplexer (4 select lines)
 
We will study the concept of multiplexing through a __2-1 multiplexer__. This is the simplest case and the rest are just more complex applications of the same concept.

## What is a multiplexer?

The multiplexer or MUX is a digital switch, also called as data selector. It consists of a few input lines, a select line, and an output line. The select line 'selects' which input line to take information from. This is better illustrated through the picture shown below.

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79624726-55c43200-8141-11ea-9427-15ac98e2ef80.gif"/>
</p> 

In the picture above, the select line chooses one of the inputs. This is the function of select line. Now we can obtain information from that particular input line. The information is sent to the circuit through the output line. We can choose any of the input lines. This is, in a nutshell, the concept of multiplexing.

## How many input lines?

Generally the number of input lines in a single multiplexer come in powers of 2. So you can have 2 input lines, or 4 input lines, or 8 input lines. All of these have a single output line. Hence they are called 2-1 multiplexer, 4-1 multiplexer and so on. Now you know what the list given at the beginning means.

## How many select lines?

The number of select lines is equal to the power raised. So a 2-1 multiplexer needs 1 select line, 8-1 needs 3 select lines, 16-1 needs 4 select lines to be able to select any one particular input line. 

## 2-1 Multiplexer Design

Here we build a 2-1 multiplexer using logic gates. 

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79625823-56f95d00-8149-11ea-94da-c6e85c6ecd12.png"/>
</p> 

The logic equation for the 2:1 Multiplexer is Z = A’ I0 + AI1. The truth table is as shown
<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79625924-09c9bb00-814a-11ea-94b3-d19dd37b1a4f.jpg"/>
</p> 

Here the select line is A. The input lines are I0 and I1. The output line is Z. If A is 0, the AND gate with I0 gives output zero. But because of the NOT gate, the AND gate with I1 gets 1 as one of the input. The output of the lower AND gate becomes A'I1 which is simply I1. So we get I1 as output. If we toggle A we get I0 as output.

# Multiplexer IC 74157

In some cases, two or more multiplexers are fabricated on a single IC because simple logic gates can implement the multiplexer. Generally four 2 line to 1 line multiplexers are fabricated in a single IC as shown in figure below. Some of these ICs of 2 to 1 multiplexers include __IC 74157__ and IC 74158. The selection line controls the input lines to the output in all four multiplexers. The pin diagram is given below

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79626874-65e40d80-8151-11ea-85b4-cee2f1282c8d.png"/>
</p> 

The output Y1 can be selected such that its value may be equal to A1 or B1, Y2 can be either A2 or B2 and so on. The Strobe G enables and disables all the multiplexers, i.e., when G=1, outputs of all the multiplexer is zero irrespective of the value of SELECT line.

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79626822-d3436e80-8150-11ea-99dd-fe2f15a0629e.png"/>
</p> 

The truth table is given below

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79627003-66c96f00-8152-11ea-8b06-57178dafdbd5.png"/>
</p> 


