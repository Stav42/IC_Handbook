 # Multiplexer
Multiplexing is the property of combining one or more signals and transmitting on a single channel. You will get a sense of what that means as you read this tutorial. This is achieved by the device multiplexer. A multiplexer is the most frequently used combinational circuits and important building block in many in digital systems.

There are four types of Multiplexers
 
 * 1.2-1 multiplexer ( 1select line)
 * 2.4-1 multiplexer (2 select lines)
 * 3.8-1 multiplexer(3 select lines)
 * 4.16-1 multiplexer (4 select lines)
 
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

