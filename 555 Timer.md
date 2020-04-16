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

__GND PIN__
Pin-1 is a GND pin which is used to supply a zero voltage to the IC.

__TRIGGER PIN__
Pin 2 is the trigger pin and connected to the inverting input of the lower comparator. A comparator essentially compares the voltages given at the two inputs. If the voltage at non inverting input is greater, it basically gives a digital output of 1 otherwise 0. The output here depends on the voltage given at trigger pin. These binary values convert the flip flop from set to RST (reset)

__OUTPUT PIN__
Pin 3 is the output pin. It gets the output from the flip flop.

__RESET PIN__
Resets the flip flop

__CONTROL VOLTAGE PIN__
Pin-5 is the control voltage pin used to control the pulse width of the output waveform and also the levels of threshold and trigger. When an external voltage is applied to this pin, then the output waveform will be modulated

__THRESHOLD PIN__
Pin-6 is the threshold pin, when the voltage is applied to threshold pin, then it contrasts with a reference voltage. The set state of the FF can be depends on the amplitude of this pin.

Pin 7 is the discharge pin and pin 8 is voltage supply

They are used in three modes - __Astable, Monostable, Bistable__. Look'em up

Article - https://www.edgefx.in/555-timer-ic-introduction-and-working-with-operating-modes/

Video Explanation - https://youtu.be/i0SNb__dkYI

### Applications
1. Monostable multivibrator
2. Voltage controlled oscillator
3. Ramp generator

