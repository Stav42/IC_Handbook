# Non programmable ICs

Integrated Circuits(IC) are the cornerstone of modern electronics. They are basically an arrangement of various electronics components like op-amps,resistors, transistors etc. They are used extensively. 

## 555 Timer 

The 555 timer IC is an integrated circuit used in a variety of timer, pulse generation, and
oscillator applications. The 555 can be used to provide time delays, as an oscillator, and
as a flip-flop element.Its one of the most used ICs in the industry. It has 8 pins. The pin connections are shown below

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79270221-56e42d80-7ebb-11ea-98f9-c61f02d35f8a.png"/>
</p> 

### Block Diagram

The IC consists of 2 comparators made of op amps, a discharge transistor, potential dividers (resistor in this case), a RS flip flop. The supply voltage required is between 4.5 and 16 V. The block diagram is given below

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79270640-20f37900-7ebc-11ea-9a36-8fcd124b9145.png"/>
</p> 

__GND Pin__

Pin-1 is a GND pin which is used to supply a zero voltage to the IC.

__Trigger Pin__

Pin 2 is the trigger pin and connected to the inverting input of the lower comparator. A comparator essentially compares the voltages given at the two inputs. If the voltage at non inverting input is greater, it basically gives a digital output of 1 otherwise 0. The output here depends on the voltage given at trigger pin. These binary values convert the flip flop from set to RST (reset)

__Output Pin__

Pin 3 is the output pin. It gets the output from the flip flop.

__Reset Pin__

Resets the flip flop

__Control Voltage Pin__

Pin-5 is the control voltage pin used to control the pulse width of the output waveform and also the levels of threshold and trigger. When an external voltage is applied to this pin, then the output waveform will be modulated

__Threshold Pin__

Pin-6 is the threshold pin, when the voltage is applied to threshold pin, then it contrasts with a reference voltage. The set state of the FF can be depends on the amplitude of this pin.

Pin 7 is the discharge pin and pin 8 is voltage supply

They are used in three modes - __Astable, Monostable, Bistable__. Look'em up

Article - https://www.edgefx.in/555-timer-ic-introduction-and-working-with-operating-modes/

Video Explanation - https://youtu.be/i0SNb__dkYI

### Applications
1. Monostable multivibrator
2. Voltage controlled oscillator
3. Ramp generator

## 4029 IC

One of the most common requirements in digital equipment is counting. And the most
common counting requirement has to do with time. From a basic digital clock (which
is incorporated into most digitally-controlled appliances) to interval timers and event
counters, the need for counting circuits is very great.

The 4029 IC is a presettable up/down counter which counts in either binary or decade mode depending on the voltage
level applied at binary/decade input whenever a signal is recieved at the CLOCK. 

### Functioning
The pin connections are shown below

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79280375-d5e26180-7ecd-11ea-8fce-5c1838e54a22.png"/>
</p> 


The internal schematic diagram of the 4029 is quite complex. However, we can’t reach the internal circuitry in any
case, so the functional diagram to the right is far more useful for our purposes.
Most of the designations are straightforward and intuitive.

__UP/DN__

Pin 10 tells the counter to count up if it is a logic 1, or down when it is logic 0

__BIN/DEC__

A logic 1 to the bin/dec input i.e Pin 9 causes the counter to operate in binary mode, while a logic 0 switches it to decimal (sometimes called decade) mode.

__CIN__

Pin 5. If CIN is logic 1, the counter won’t count at all. When CIN goes to logic 0, the counter operates normally.

__PE__

The pe input is the preset enable line. When this line is logic 0, the counter operates normally. However, when pe becomes logic 1, the logic signals present on the four jam input lines get copied directly to the four bits of the counter, overriding any prior count.

### Multiple 4029s
If multiple 4029s are cascaded for a larger count, all up/dn pins are connected together and driven from a common signal, as are all bin/dec lines. The CIN and COUT lines form the means of cascading counters and still keeping a fully synchronous count. 

If CIN is logic 1, the counter won’t count at all. When CIN goes to logic 0, the counter operates normally. Then, when the counter reaches its terminal count (9, 15, or 0 depending on the states of up/dn and bin/dec), COUT goes to logic 0. This is connected to the CIN line of the next IC to allow the next higher order of magnitude to count once. Then COUT goes to logic 1 again. 

The first counter IC in the set, representing the least significant digit, has its CIN line grounded to logic 0 so it will always count. The clock input, like up/dn and bin/dec, is fed to all 4029s in an extended counter circuit. This is the signal that represents whatever is to be counted. Any 4029 that is enabled by having its CIN line at logic 0 will change state to the next count when the clock rises from logic 0 to logic 1. Any changes to the CIN and COUT lines will occur just after that rising edge, and so will be ready for the next clock pulse.

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
