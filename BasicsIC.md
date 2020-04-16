# Non programmable ICs

Integrated Circuits(IC) are the cornerstone of modern electronics. They are basically an arrangement of various electronics components like op-amps,resistors, transistors etc. They are used extensively. 


## 7447 IC
74LS47 is a BCD to 7-segment decoder/driver IC. It accepts a binary coded decimal as input and converts it into a pattern to drive a seven-segment for displaying digits 0 to 9. Binary coded decimal (BCD) is an encoding in which each digit of a number is represented by its own binary sequence (usually of four bits).

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79281587-af71f580-7ed0-11ea-875c-7778e023ca34.png"/>
</p> 

### Description
74LS47 IC accepts four lines of BCD (8421) input data and generates their complements internally. The data is decoded with seven AND/OR gates to drive indicator LEDs of the seven segment directly. The following picture clarifies the functioning a bit

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79281751-07a8f780-7ed1-11ea-9dd6-a2e09b48ff55.png"/>
</p> 

Here the boxes represent 1 * 1 + 1 * 2 + 0 * 4 + 0 * 8 = 3 which is shown in the LED display.

## 7805 IC
A voltage regulator IC maintains the output voltage at a constant value. 7805 IC, a member of 78xx series of fixed linear voltage regulators is a popular voltage regulator integrated circuit (IC).

### 7805 IC Rating

Output voltage range = VMax=5.2V ,VMin=4.8V

Input voltage range = 7V - 35V 

Current rating of IC = 1A 

 # Pin Diagram of 7805 IC
**INPUT** Pin 1 is the input Pin. A positive unregulated voltage is given as input to this pin.

**GROUND** Pin 2 is ground the Pin. It is common to both Input and Output.

**OUTPUT** Pin 3 is the output Pin. The output regulated 5V is taken at this pin of the IC.

As you may have noticed, there is a significant difference between the input voltage the output voltage of the voltage regulator. This difference between the input and output voltage is released as heat. So to disipate the heat and protect the instrument from malfunctioning, we have 2 options. Either design your circuit so that the input voltage going into the regulator is limited to 2-3 volts above the output regulated voltage or place an appropriate heat sink, that can efficiently dissipate heat.

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79285522-712e0380-7edb-11ea-80a2-c3e8fc5885d8.png"/>
</p> 

### Applications of 7805 IC
 * Fixed-Output Regulator
 * Positive Regulator in Negative Configuration
 * Current Regulator
 * Reverse bias projection Circuit
 
 ## Multiplexer
 A multiplexer (or mux) is a device that selects one of several digital input signals and directs it to a single output. A multiplexer of 2n inputs has n select lines, which are used to select which input line to send to the output. A multiplexer is also called a data selector. Multiplexers are capable of handling both analog and digital applications. In analog applications, multiplexers are made up of of relays and transistor switches, whereas in digital applications, the multiplexers are built from standard logic gates. When the multiplexer is used for digital applications, it is called a digital multiplexer. Multiplexers are classified into four types:
 
 * 1.2-1 multiplexer ( 1select line)
 * 2.4-1 multiplexer (2 select lines)
 * 3.8-1 multiplexer(3 select lines)
 * 4.16-1 multiplexer (4 select lines)
