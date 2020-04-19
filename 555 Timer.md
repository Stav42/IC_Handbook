# 555 Timer 

The 555 timer IC is an integrated circuit used in a variety of timer, pulse generation, and
oscillator applications. Its one of the most used ICs in the industry. It has 8 pins. The __pin diagram__ is shown below

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79270221-56e42d80-7ebb-11ea-98f9-c61f02d35f8a.png"/>
</p> 

A 555 timer is operated in 3 modes - __Astable, Monostable, Bistable__.

Contents 

* [Inside the IC](#inside-the-ic)
    * [Comparator](#comparator)
    * [Flip Flop](#flip-flops)
* [Astable Mode of Operation](#how-does-a-555-timer-work-in-astable-mode-of-operation)    
## Inside the IC

The IC consists of 2 __comparators__, a __discharge transistor__, __potential dividers__ (resistor in this case) and a __RS flip flop__. The block diagram is given below

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79680858-1b868d80-8232-11ea-9161-b306760f1ec4.gif"/>
</p> 
 
 To understand how a 555 timer works, its necessary to understand how flip flop and Comparators work
 
 ### Comparator
  
<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79681244-57bbed00-8236-11ea-9cd5-e3f84f566818.gif"/>
</p> 
 
If the voltage at __Vin > Vref__, the output voltage __Vout__ is HIGH, in this case, __Vcc__, otherwise the output is 0V. Here the resistors act as __potential dividers__. They split __Vcc__ into __Vcc/2__ at the junction between the two resistors. Therefore __Vref__ becomes **Vcc/2**.

Summary:
* When __Vin > Vref__, __Vout__ =  __Vcc__.
* When __Vin < Vref__, __Vout__ =  __0V__.


### Flip Flops

A flip flop is basically a SR Latch.

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79681405-b03fba00-8237-11ea-8574-7d570c0b8b64.gif"/>
</p>

In simple terms, when __S__ (called __SET__) is HIGH, The ouput __Q__ is HIGH. The important thing about flip flop is that it remembers that configuration. Now it doesn't matter whether S is HIGH or LOW. Q will remain as it is, i.e, HIGH.

Now, in order to turn Q LOW, we have to turn RESET high. Q remains LOW until again we turn S high.

Both Q and S cannot be HIGH at the same time. This is considered an invalid configuration.


## How does a 555 Timer work in Astable Mode of Operation?


<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79681692-afa82300-8239-11ea-9b96-ef638ebb2e76.gif"/>
</p> 

* At the beginning, after we make all the connections, the potential dividers do their work and split the voltages into VCC/3 and 2/3VCC. 
* Supposing initially the __Trigger Pin__ and __Threshold Pin__ is set low. The lower comparator gives a HIGH output and the upper comparator gives LOW output. This configuration drives the flip flop to turn Q high because R is LOW and S is HIGH. 
* As the capacitor charges, the Trigger pin and Threshold Pin give higher voltages as input. As soon as trigger input exceeds 1/3VCC, Lower comparator gives LOW output. This doesn't change the value of Q because R has not yet been turned on.
* After a while, when charge on capacitor increases further, the upper comparator flips too. Earlier, it gave a LOW output. Now it gives HIGH output. This feeds into the R pin of flip flop and Q turns 0.
* As Q turns 0, Q' turns HIGH. This Q' is connected to the discharge transistor. Q' being HIGH, turns on the discharge transistor. This forces the capacitor - resistor circuit to now discharge through the transistor.
* As it does so, the charge on the capacitor decreases. The voltages on Threshold and Trigger Pins decrease. They eventually turn so low that Trigger pin becomes less than 1/3VCC due to which the output of the lower comparator goes HIGH which turns S HIGH. This in turn, sets Q HIGH.
* As Q is set high, the discharge transistor turns off. The capacitor starts charging once again and the cycle repeats on and on.

This is how an __Astable__ 555 Timer works. The cycle is periodically repeated after a set interval. Through output PIN 3 (which is basically Q) we recieve pulses of HIGH voltage periodically. Now how fast the capacitor charges depends solely on the resistors and capacitors. Adjusting their values adjusts the frequency of pulses.

The __waveform__ of pulses is given below

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79682044-bdab7300-823c-11ea-9abd-492a985e6889.gif"/>
</p> 

Following are the standard formula:

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79682098-40343280-823d-11ea-9269-97a8016379be.png"/>
</p> 

## How does a 555 Timer work in Monostable Mode of Operation?

A monostable 555 timer gives HIGH output only for a specific period after which it goes to LOW output and stays there. This time interval where it stays HIGH is dependant on value of resistor and capacitor. A switch is used to turn it ON.


<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79682659-9acf8d80-8241-11ea-88b1-0b6f86b4bd7d.png"/>
</p> 

We shall assume out Flip flop is in initial latch state of Q = 0. This means that when S and R are both LOW, Q is LOW.

* Initially when the switch is open, comparators give outputs 0. Therefore R and S are LOW. Since Q' feeds into the discharge transistor, its HIGH state turns the transistor on and Vcc along with any charge on capacitor discharges. 
* After the switch is pressed, Lower comparators gives HIGH output. Q goes HIGH. Q' goes LOW which turns off the discharge transistor. This allows the capacitor to get charged. 
* As soon as the charge on capacitor is high enough, the upper comparator turns ON, and sets R high. This turns Q low. Q' goes HIGH which turns on the discharge transistor. This drains the capacitor. Eventually the upper comparator goes to 0.
* Now both comparators are at 0 and Q is LOW. This is the initial state of the timer. This is repeated after we again press the switch

Therefore its up to the user to decide when to turn on the timer. The duration for which it stays on is dependant on the resistor and capacitor.

Formula for duration of HIGH state: Time = 1.1 x R x C



Article - https://www.edgefx.in/555-timer-ic-introduction-and-working-with-operating-modes/

Video Explanation - https://youtu.be/i0SNb__dkYI

### Applications
1. Monostable multivibrator
2. Voltage controlled oscillator
3. Ramp generator

