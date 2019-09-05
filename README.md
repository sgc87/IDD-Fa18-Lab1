# IDD-Fa18-Lab1: Blink!

**A lab report by John Q. Student**

**Fork** this repository to get a template for Lab 1 for *Developing and Designing Interactive Devices* at Cornell Tech, Fall 2018. You should modify this `README.md` file to delete this paragraph and update below. As the lab asks:

> Include your responses to the bold questions on your own fork of the lab activities. Include snippets of code that explain what you did. Deliverables are due next Tuesday. Post your lab reports as `README.md` pages on your GitHub, and post a link to that on your main class hub page.

We've copied the questions from the lab here. Answer them below!

## Part A. Set Up a Breadboard

[insert a photo of your breadboard setup here]


## Part B. Manually Blink a LED

**a. brown black brown gold **
 
**b. I had to connect one end of the switch to 5V and the other to the LED and resistor in series**


## Part C. Blink a LED using Arduino

### 1. Blink the on-board LED

**a. I didn't have to change any lines of code. I did have to configure the board type**

**b. I had to change the delay between turning the LED on and off
// the loop function runs over and over again forever
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(12);                       // wait for a second
  digitalWrite(LED_BUILTIN, LOW);    // turn the LED off by making the voltage LOW
  delay(12);                       // wait for a second
}**

**c. I would need to add a resistor device to protect the board and external LED**
 
**d. Below a delay of 15, it gets harder and harder to tell if there is a delay. I couldn't tell around a delay of 12. 
To prove that the LED is still blinking, one can use a camera to see if it's flickering**

**e. https://github.com/sgc87/IDD-Fa18-Lab1/blob/master/Blink.ino**


### 2. Blink your LED

**Make a video of your LED blinking, and add it to your lab submission.**

[link to your video here; feel free to upload to youtube and just paste in a link here]


## Part D. Manually fade an LED

**a. Yes, the LED is glowing throughout the whole range of the potentiometer. This is because current is flowing
no matter the resistance. In order for there to be no glow, the resistance would have to be so high that the 
light is either not visible or does not meet the minimum current required to light up the LED. **


## Part E. Fade an LED using Arduino

**a. To make the code control the circuit, I had to change the value of variable int led from 9 to 11. **

**b. What is analogWrite()? How is that different than digitalWrite()?**


## Part F. FRANKENLIGHT!!!

### 1. Take apart your electronic device, and draw a schematic of what is inside. 

**a. Is there computation in your device? Where is it? What do you think is happening inside the "computer?"**

**b. Are there sensors on your device? How do they work? How is the sensed information conveyed to other portions of the device?**

**c. How is the device powered? Is there any transformation or regulation of the power? How is that done? What voltages are used throughout the system?**

**d. Is information stored in your device? Where? How?**

### 2. Using your schematic, figure out where a good point would be to hijack your device and implant an LED.

**Describe what you did here.**

### 3. Build your light!

**Make a video showing off your Frankenlight.**

**Include any schematics or photos in your lab write-up.**
