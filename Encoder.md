# Encoder

An Encoder is a combinational circuit that performs the reverse operation of Decoder. It has maximum of 2^n input lines and ‘n’ output lines. It will produce a binary code equivalent to the input, which is active High. 

Therefore it 'encodes' a 2^n long binary string to a n long binary string. A combination of 4 ones and zeroes is encoded to a combination of 2 ones and zeroes. This will become apparent as you read on. It is optional to represent the enable signal in encoders.

Since this is a pretty long tutorial, the contents are as follow:

* [Octal to Binary Encoder](#octal-to-binary-encoder)
* [Priority Encoder](#priority-encoder)
* [IC 74148](#ic-74148)

## Octal to Binary Encoder

Octal to binary Encoder has eight inputs, Y7 to Y0 and three outputs A2, A1 & A0. Octal to binary encoder is nothing but 8 to 3 encoder. The __block diagram__ of octal to binary Encoder is shown in the following figure.

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79678248-fb95a080-8216-11ea-921e-bb2f97bf3866.jpg"/>
</p> 
At any time, only one of these eight inputs can be ‘1’ in order to get the respective binary code. The truth table of 8 to 3 encoder is shown below.

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

### Drawback

If more than one input is active High, then the encoder produces an output, which may not be the correct code. For example, if both Y3 and Y6 are ‘1’, then the encoder produces 111 at the output. This is neither equivalent code corresponding to Y3, when it is ‘1’ nor the equivalent code corresponding to Y6, when it is ‘1’.

So, to overcome these difficulties, we should assign priorities to each input of encoder. Then, the output of encoder will be the binary code corresponding to that active HIGH inputs which has higher priority. This encoder is called as priority encoder.

## Priority Encoder

A __4 to 2 priority encoder__ has four inputs Y3, Y2, Y1 & Y0 and two outputs A1 & A0. Here, the input, Y3 has the highest priority, whereas the input, Y0 has the lowest priority. In this case, even if more than one input is ‘1’ at the same time, the output will be the binary code corresponding to the input, which is having higher priority.

We considered one more output __V__ in order to know whether the code available at outputs is valid or not. If all the inputs are LOW, V is LOW. If at least one input is HIGH, V is HIGH.

The __Truth table__ of 4 to 2 priority encoder is shown below. 

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79679088-7adba200-8220-11ea-9cf4-b1b783d0b7a1.png"/>
</p> 

The __boolean expression__ for the truth table above is

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79679125-c2622e00-8220-11ea-8284-97250ca35ddf.png"/>
</p> 

We can implement the above Boolean functions using logic gates. The __circuit diagram__ of 4 to 2 priority encoder is shown in the following figure.

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79679162-035a4280-8221-11ea-987f-d0e86021d2e5.jpg"/>
</p> 

The above circuit diagram contains two 2-input OR gates, one 4-input OR gate, one 2input AND gate & an inverter. Here AND gate & inverter combination are used for producing a valid code at the outputs, even when multiple inputs are equal to ‘1’ at the same time. Hence, this circuit encodes the four inputs with two bits based on the priority assigned to each input.

## IC 74148
