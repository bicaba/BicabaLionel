# **Audio amplifier** 🔊
Sometimes the sound from my laptop is not powerful enough when I'm watching videos or listening to music, so I often have to use my headphones. In my Circuit Theory 2 class, we learned how op-amps work, and I want to apply that knowledge to this project. My goal is to build an audio amplifier to use with my laptop, so I don't always have to rely on my headphones. Additionally, I'm planning to build an AM radio for a future project, and I intend to use this audio amplifier for that as well😊.


 ![pcb_4](https://github.com/bicaba/BicabaLionel/blob/main/Audio%20amplifier/PCB3_12.png)

 
  📌 Audio Amplifier Specification:
   
   
1. Volume Control:

  - The audio amplifier should include a feature to control the volume.
    Volume control should allow for precise adjustment to achieve the desired audio level.
  - The volume control mechanism can be in the form of a rotary knob, slider,     or digital interface.

2. Tone Adjustment:

  - The audio amplifier should have the capability to adjust the tone of the   audio output.

 - These controls can be in the form of rotary knobs, sliders, or digital interfaces to allow for fine-tuning of the audio output to suit user preferences.
 
 

##  Op amp principle 🤔
An op amp (Operationnel amplifer ) is an intagrated circuit (IC) that amplifies the difference in voltage between two inputs( the Inverting input and the Non-inverting input).
- The currents into the inverting input and non-inverting input of an ideal op amp amplifier are zero and the volatage node at the input nodes of an ideals op amp are equal.
- Op amp are used to build circuits that perform mathematical operations. Many of the theses circuits habe been given names. The inverting amplifiers, the non-inverting amplifier, voltage followers are some example of useful op amp circuit.

   - Inverting amplifiers : Gain = V_Output/V_input = -R1/R2

   - Non-inverting amplifiers : Gain = V_Output/V_input = 1+ ( R1/R2)
   - Voltage followers : Gain = 1 

![Op amp symbol](https://github.com/bicaba/BicabaLionel/blob/main/Audio%20amplifier/op-amp-symbol.jpg)

fig 1: the **μA741** is an example of op amp 

####  quick Demonstration of how an op amp work : 

I will built a Non-inverting amplifer using the μA741 for the demonstration
- Simulation on **Multisim** :

![Non-inverting amplifier](https://github.com/bicaba/BicabaLionel/blob/main/Audio%20amplifier/74565.jpg)

fig 3: Circuit of a Non-inverting amplifier

![Oscilloscope out](https://github.com/bicaba/BicabaLionel/blob/main/Audio%20amplifier/741%20oscillos.jpg)

fig 4: Waveform of the circuit. Green= V_input(input voltage) and CH3 = V_output (Output voltage ) Gain = 11.2/2.82 = 3.97

- Test of the circuit
![Non-inverting amplifier](https://github.com/bicaba/BicabaLionel/blob/main/Audio%20amplifier/test%20ciruiot.jpg)

![Oscillocope_output test ](https://github.com/bicaba/BicabaLionel/blob/main/Audio%20amplifier/image.png)

*fig 5: Yellow for input voltage(2.09 V) and Green for Output voltage(8.4 V)* 

The gain is calculated as follows: 
 Gain = 8.4/2.09=4 

As observed, the gain obtained from the **Multisim** simulation is very close to the one measured during the test. This indicates that the input voltage is amplified approximately 4 times at the output of the operational amplifier.


## OP amp IC
the Op amp IC being used in this project is the **LM386** 

- This chip is a powrful amplifers designed for use in low volatage consumer application

- We have a voltage gains from 20 to 200
- the minimum  supply voltage is 4 V and the maximum voltage is 12 V

![datasheet_LM386](https://github.com/bicaba/BicabaLionel/blob/main/Audio%20amplifier/datasheetlm386.jpg)

*fig 6: Pin configuration of the LM386 from the datasheet*

## LTspice simulation 

I used  **LTspice** to build and simulate my audio amplifier circuit with a music waveform file. I then export the amplified music at the output.



![datasheet_LM386](https://github.com/bicaba/BicabaLionel/blob/main/Audio%20amplifier/circuit%20complet%20annot%C3%A9.png)
               

  *fig7: Circuit on LTspice*

![datasheet_LM386](https://github.com/bicaba/BicabaLionel/blob/main/Audio%20amplifier/output.jpg)
*fig8: Waveform (input and speaker)*

### Result 🥁: 

V(input) = The music signal waveform at the input of the amplifier. 


https://github.com/bicaba/BicabaLionel/assets/20146995/9267046d-2571-4ef5-863d-18f8caae642b


V(speaker) = The amplified music signal waveform at the output to the speaker.




https://github.com/bicaba/BicabaLionel/assets/20146995/1c008ecf-ce24-4267-b3fb-768eea33812a




## Part 📃
 - 1 x LM386
 - 1 X 250 uF 16 V electrolytic capacitor or 470 uF 16 V electrolytic capacitor
 - 2 x 10 uF 16 V electrolytic capacitor
 - 1 x 0.05 uF or 0.1 uF Polyester (Mymar) Film capacitor 
 - 1 x 47 pF ceramic capacitor 
 - 3 x 0.27 uF Polyester (Mymar) Film capacitor
 - 1 x 10 ohm 125mW Resistor 
 - 2 x 10k ohm Potentiometer 
 - 1 x 8 ohm Speaker 

## PCB design

I designed the audio amplifier's PCB using **Altium Designer**.

Schematic Design : 

![shematic](https://github.com/bicaba/BicabaLionel/blob/main/Audio%20amplifier/schematic_altium.jpg)

  PCB Design :

![pcb_555](https://github.com/bicaba/BicabaLionel/blob/main/Audio%20amplifier/pcb_.jpg)

![pcb_2](https://github.com/bicaba/BicabaLionel/blob/main/Audio%20amplifier/pcb_1.jpg)

![pcb_1](https://github.com/bicaba/BicabaLionel/blob/main/Audio%20amplifier/PCB3_11.png)

![pcb_3](https://github.com/bicaba/BicabaLionel/blob/main/Audio%20amplifier/PCB3_12.png)

![pcb_4](https://github.com/bicaba/BicabaLionel/blob/main/Audio%20amplifier/PCB3_13.png)

![pcb_5](https://github.com/bicaba/BicabaLionel/blob/main/Audio%20amplifier/PCB3__6.png)


