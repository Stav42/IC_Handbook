## 555 Timer 

The 555 timer IC is an integrated circuit used in a variety of timer, pulse generation, and
oscillator applications. Its one of the most used ICs in the industry. It has 8 pins. The __pin diagram__ is shown below

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79270221-56e42d80-7ebb-11ea-98f9-c61f02d35f8a.png"/>
</p> 

### Block Diagram

The IC consists of 2 comparators, a discharge transistor, potential dividers (resistor in this case) and a RS flip flop. The supply voltage required is between 4.5 and 16 V. The block diagram is given below

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79680858-1b868d80-8232-11ea-9161-b306760f1ec4.gif"/>
</p> 

## How does a 555 Timer works?


<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79681118-e7609c00-8234-11ea-86ef-f016320b8805.png"/>
</p> 



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

