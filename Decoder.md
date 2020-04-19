# Decoder

A __decoder__ is a circuit that changes a code into a set of signals. It is called a decoder because it does the reverse of encoding, but we will begin our study of encoders and decoders with decoders because they are simpler to design. 

Decoder is a combinational circuit that has ‘n’ input lines and maximum of 2^n output lines. One of these outputs will be active High based on the combination of inputs present, when the decoder is enabled. That means decoder detects a particular code.
You'll get a sense of what that means as you read on.

Content
* [2 To 4 Decoder](#2-to-4-decoder)
* [3 To 8 Decoder](#3-to-8-decoder)
* [74138 IC](#74138-ic)

## 2 To 4 Decoder

Let 2 to 4 Decoder has two inputs A1 & A0 and four outputs Y3, Y2, Y1 & Y0. The __block diagram__ of 2 to 4 decoder is shown in the following figure.

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79677411-9ccc2900-820e-11ea-8b95-45b0e9d7aa18.jpg"/>
</p> 

One of these four outputs will be ‘1’ for each combination of inputs when enable, E is ‘1’. The __Truth table__ of 2 to 4 decoder is shown below.

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79677456-6511b100-820f-11ea-94aa-de12fa39fe0c.png"/>
</p> 

The __Boolean Equation__ for each output is

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79677514-df423580-820f-11ea-90e2-bd3fcac37b7f.png"/>
</p> 

So each input for A1 and A0 gives out a different output. This output is our code.

## 3 To 8 Decoder

A 3 to 8 Decoder can be made using two 2 To 4 Decoder. Its fairly simple. The __block diagram__ is given below

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79677644-44e2f180-8211-11ea-9c24-628719718a2a.png"/>
</p> 

The parallel inputs A1 & A0 are applied to each 2 to 4 decoder. The complement of input A2 is connected to Enable, E of lower 2 to 4 decoder in order to get the outputs, Y3 to Y0. Using this connection we can get all the outputs we would get from a traditional 3 To 8 decoder made using logic gates only. 

# 74138 IC

74138 IC is a 3 To 8 Decoder and it uses two 2 To 4 Decoder in the manner described above. The two enable pins for the two 2 To 4 decoder are reffered to as G2A and G2B. These are active LOW input which means giving them LOW enable input activates them. The G1 pin (or enable pin) here is the Enable pin for the overall 3 To 8 pin only. 

The __Pin Diagram__ is given below

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79677783-6b555c80-8212-11ea-87ae-ad47b8069879.png"/>
</p> 

The __truth table__ is given below

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79677891-5927ee00-8213-11ea-8174-a72e18ba57bb.png"/>
</p> 

Here E1, E2, E3 are G2A, G2b, and G1 respectively. Remember E1 and E2 are active LOW inputs.

Here is the [datasheet](https://www.ti.com/lit/ds/symlink/sn54ls138-sp.pdf)
