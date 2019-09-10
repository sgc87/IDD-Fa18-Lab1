# IDD-Fa18-Lab1: Blink!

**Samuel Choi (sgc87)**

**Due: September 10, 2019**

## Part A. Set Up a Breadboard

![Part A Breadboard](https://github.com/sgc87/IDD-Fa18-Lab1/blob/master/20190905_103013.jpg)


## Part B. Manually Blink a LED

**a. What color stripes are on a 100 Ohm resistor?**

brown black brown gold
 
**b. What do you have to do to light your LED?**

I had to connect one end of the switch to 5V and the other to the LED and resistor in series.


## Part C. Blink a LED using Arduino

### 1. Blink the on-board LED

**a. What line(s) of code do you need to change to make the LED blink (like, at all)?**

I didn't have to change any lines of code. I did have to configure the board type on the Arduino software.

**b. What line(s) of code do you need to change to change the rate of blinking?**

I had to change the delay between turning the LED on and off
```
// the loop function runs over and over again forever
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(12);                       // wait for a second
  digitalWrite(LED_BUILTIN, LOW);    // turn the LED off by making the voltage LOW
  delay(12);                       // wait for a second
}
```

**c. What circuit element would you want to add to protect the board and external LED?**

I would need to add a resistor device to protect the board and external LED.
 
**d. Change the delay parameter to modify blink rate of your LED to make it blink faster. At what delay can you no longer perceive the LED blinking? (And how can you prove to yourself that it is, in fact, still blinking?**

Below a delay of 15, it gets harder and harder to tell if there is a delay. I couldn't tell around a delay of 12. 
To prove that the LED is still blinking, one can use a camera to see if it's flickering.

**e. Modify the code to make your LED blink your way. Save your new blink code to your lab 1 repository, with a link on the README.md.**

[I made the LED blink faster](https://github.com/sgc87/IDD-Fa18-Lab1/blob/master/Blink.ino)

### 2. Blink your LED

**Make a video of your LED blinking, and add it to your lab submission.**

[Blinking LED Video](https://youtu.be/lvP25NpGK_Y)


## Part D. Manually fade an LED

**a. Are you able to get the LED to glow the whole turning range of the potentiometer? Why or why not?**

Yes, the LED is glowing throughout the whole range of the potentiometer. This is because current is flowing
no matter the resistance. In order for there to be no glow, the resistance would have to be so high that the 
light is either not visible or does not meet the minimum current required to light up the LED. 


## Part E. Fade an LED using Arduino

**a. What do you have to modify to make the code control the circuit you've built on your breadboard?**

To make the code control the circuit, I had to change the value of variable int led from 9 to 11. 

**b. What is analogWrite()? How is that different than digitalWrite()?**

analogWrite is a PWM function where the input specifies the duty cycle of a PWM output for a specified pin. digitalWrite is a digital output function that only has two possible states, HIGH an LOW.


## Part F. FRANKENLIGHT!!!

### 1. Take apart your electronic device, and draw a schematic of what is inside. 

Here is a rough schematic. The red is the added LED. 

![Frankenlight Schematic](https://github.com/sgc87/IDD-Fa18-Lab1/blob/master/69964337_635284323545155_278662653600071680_n.jpg)

**a. Is there computation in your device? Where is it? What do you think is happening inside the "computer?"**

Yes, there is a processor on the device that centralizes the data input and outputs it to its radio antenna to the receiver. The processor is circled in red, but under the capacitor in the picture. 

![Frankenlight Computer](https://github.com/sgc87/IDD-Fa18-Lab1/blob/master/69868316_748237088931791_979148489315319808_n.jpg)

**b. Are there sensors on your device? How do they work? How is the sensed information conveyed to other portions of the device?**

There is an infrared optical sensor at the bottom of the mouse. It collects light reflected on the surface reflected by the infrared LED blaster on the device. There is also a scrollwheel, a scrollwheel button, right and left click buttons, and a mouse LED sampling rate button at the bottom. All inputs received on these sensors are relayed to the processor

![Frankenlight Device](https://github.com/sgc87/IDD-Fa18-Lab1/blob/master/70291245_2446622165594817_6371284186308804608_n.jpg)

**c. How is the device powered? Is there any transformation or regulation of the power? How is that done? What voltages are used throughout the system?**

The device is powered by a single AA battery, which is approximately 1.5V. There are capacitors on the PCB, which help store and regulate power for some componets. Besides the capacitors there does not seem to be a significant power regulator. There are also resistors on the PCB to help with resistance for some of the components. 

**d. Is information stored in your device? Where? How?**

No information is not stored in the computer car mouse. There may be small caches to store temporary data but no permanent flash memory onboard. 

### 2. Using your schematic, figure out where a good point would be to hijack your device and implant an LED.

**Describe what you did here.**
I hotwired my additional LED from the two LEDs already on the computer car mouse that illuminate the headlights when the mouse is turned on. Since the tailights don't have lights on this device, I decided to add one working taillight. Being limited to one white LED, I was only able to add one working taillight. 

I essentially connected another LED in the circuit in parallel. 

![Frankenlight Placement](https://github.com/sgc87/IDD-Fa18-Lab1/blob/master/69732680_2936167329743349_2063788578080555008_n.jpg)

### 3. Build your light!

**Make a video showing off your Frankenlight.**
[Computer Car Mouse with added taillight functionality... on one side](https://youtu.be/f65La6CNChs)

**Include any schematics or photos in your lab write-up.**
