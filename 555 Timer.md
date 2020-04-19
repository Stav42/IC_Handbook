# 555 Timer 

The 555 timer IC is an integrated circuit used in a variety of timer, pulse generation, and
oscillator applications. Its one of the most used ICs in the industry. It has 8 pins. The __pin diagram__ is shown below

<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79270221-56e42d80-7ebb-11ea-98f9-c61f02d35f8a.png"/>
</p> 

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

### Flip Flops (SR Latch)


## How does a 555 Timer works?


<p align="center">
<img src="https://user-images.githubusercontent.com/58845531/79681138-48886f80-8235-11ea-94b4-2195129b9e33.png"/>
</p> 





Article - https://www.edgefx.in/555-timer-ic-introduction-and-working-with-operating-modes/

Video Explanation - https://youtu.be/i0SNb__dkYI

### Applications
1. Monostable multivibrator
2. Voltage controlled oscillator
3. Ramp generator

