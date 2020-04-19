# Demultiplexer

The action of a demultiplexer (or __demux__) is opposite to that of the multiplexer. As inverse to the mux , demux is a one-to-many circuit. With the use of a demultiplexer, the binary data can be bypassed to one of its many output data lines.

## What is a demultiplexer?
A demultiplexer passes information (usually binary) to one of various output lines. It consists of an input line, output lines and a few select lines. The output lines are usually in power of 2. So we have demultiplexers of type -

* 1-To-2 
* 1-To-4 
* 1-To-8 

We'll understand the concept of demultiplexing through a 1-To-4 Demux. Same concept applies to other types of demultiplexers. The diagram below illustrates the basic idea of demultiplexing.

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79627971-587f5100-815a-11ea-8847-b723d57eac47.gif"/>
</p> 

## How many select lines?

The number of select lines is the same as the power raised. So a 1-To-2 Demux will have 1 select line, 1-To-4 will have 2 select lines and 1-To-8 will have 3 select lines to be able to send information to any one output line.

## Demultiplexer design 

The logic circuit built using AND and OR gates is given below

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79628212-91202a00-815c-11ea-8b0d-2fd2ebe9fb71.gif"/>
</p> 

The Boolean expression for this 1-to-4 Demultiplexer above with outputs A to D and data select lines a, b is given as:

F = a'b'A + a'bB + ab'C + abD. 

The truth table is as follows
<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79628406-58815000-815e-11ea-8171-91c01559a5a0.png"/>
</p> 

The important idea here is the combinations of the two selection lines. Each line can be in an off and on state (0 and 1 respectively). So the combinations for the two lines are 2 * 2 = 4 which allows for selection of any of the four output lines. Each combination points to one particular output line.  

# IC 74139

IC 74139 is a dual 1-To-4 demultiplexer. It has two demultiplexers. It uses the same concept and lines as described above. The input line is basically the Enable line you'll encounter in a while.

The Pin diagram is given below

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79628670-9c755480-8160-11ea-8339-ff6723fd51c1.png"/>
</p> 
 
Each demux has an active LOW Enable (E). When E is HIGH all outputs are forced HIGH. An active low device is a device that either outputs 0V when triggered on or that accepts 0V as input to turn on.

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79628716-24f3f500-8161-11ea-96f5-5bbb587d7cf8.png"/>
</p> 

Each of the two demux accept two binary weighted inputs (A0, A1) and provide four mutually exclusive active LOW outputs (O0– O3). 

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79628833-43a6bb80-8162-11ea-80b6-6ed28f4f1e25.png"/>
</p> 

__The datasheet is available [here](https://www.uni-kl.de/elektronik-lager/417705)__
