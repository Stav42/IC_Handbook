# Encoder

An Encoder is a combinational circuit that performs the reverse operation of Decoder. It has maximum of 2^n input lines and ‘n’ output lines. It will produce a binary code equivalent to the input, which is active High. 

Therefore it 'encodes' a 2^n long binary string to a n long binary string. A combination of 4 ones and zeroes is encoded to a combination of 2 ones and zeroes. This will become apparent as you read on. It is optional to represent the enable signal in encoders.

## Octal to Binary Decoder

Octal to binary Encoder has eight inputs, Y7 to Y0 and three outputs A2, A1 & A0. Octal to binary encoder is nothing but 8 to 3 encoder. The __block diagram__ of octal to binary Encoder is shown in the following figure.

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79678248-fb95a080-8216-11ea-921e-bb2f97bf3866.jpg"/>
</p> 
At any time, only one of these eight inputs can be ‘1’ in order to get the respective binary code. The __Truth table__ of 8 to 3 encoder is shown below.

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79678278-3e577880-8217-11ea-9bae-240590c132f4.png"/>
</p> 

From Truth table, we can write the __Boolean functions__ for each output as

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79678295-68a93600-8217-11ea-893b-e9231409d2ca.png"/>
</p> 

We can implement the above Boolean functions by using four input OR gates. The __circuit diagram__ of octal to binary encoder is shown in the following figure.

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79678305-8d9da900-8217-11ea-968e-96e1ade264bd.png"/>
</p> 

The above circuit diagram contains three 4-input OR gates. These OR gates encode the eight inputs with three bits.

