# TE-2-20-LED-DICE  PROJECT SIX 

![](https://github.com/SteveJustin1963/TE-2-20-LED-DICE/blob/master/cct.png)

https://easyeda.com/editor#id=42030435fd1a415897ec1d08381c44f0|f208b34686a84562a141e2e0d3bdb559

Each project in this series needs just a few extra components in addition to the previous project to create a completely different circuit and add a new dimension to the possibilities of electronics. This is one such circuit.  Being electronically minded, have you ever wished you could throw away the old dice used in snakes and ladders and replace it with an electronic dice? Well now you can. With this LED DICE the full realism of waiting for a dice to stop rolling or a spinner to stop spinning is re-created with an electronic circuit. It works like this: after placing your finger on the TOUCH PLATE the LEDs begin to flash rapidly. After a second or two they reduce speed to a running sequence. Then they slow down to a walk and finally a crawl. At this stage you are hoping they will jump one more step to make a six. You're in luck! It jumps to a six! But wait, the capacitor may not be fully discharged. You will have to wait a few more seconds to see if the 555 oscillator will clock the CD 4017 one more step. It does. You lose. You get a single solitary ONE for your turn. That's the luck of the game. I've never been lucky at cards, dice or poker but I'm sure this game will bring you luck. Even if you don't win at Ludo or Monopoly you will generate a lot of interest from your family and friends - especially since there is no way of "loading" the circuit; it gives a completely random unbiased result.  

![](https://github.com/SteveJustin1963/TE-2-20-LED-DICE/blob/master/lay.png)

## How it works
When the battery is connected, the BC 557 transistor Q1is biased off via resistor R2. This means that no voltage will be present at the collector. When the TOUCH PLATE is touched with your finger, C1 charges and provides a base-emitter potential to turn on Qi. This potential must be higher than the turn-on voltage of .6v, to turn on Qi. The collector now provides a voltage at its output. Pin 7 of the 555 timer detects this voltage as described in the beginning of the series. It will oscillate at a frequency determined by the voltage on pin 7 and the value of C2. When your finger is removed from the TOUCH PLATE the voltage on capacitor C1 is gradually removed via the two 10M bleed resistors. As this voltage reduces, the base voltage reduces and the transistor provides a reducing voltage at its collector and also on pin 7 of the 555 oscillator. Thus the output frequency of the 555 slows down and finally comes to a complete halt. The output of the 555 drives a CD 4017 decade counter which lights each LED in turn. We are using 6 of its 10 outputs. So that only the first six are clocked, the 7th output is connected to the reset pin number 15.  As the decay of capacitor C1is exponential, the CD 4017 is clocked slower and slower so that suspense is built up when the LEDs are about tostop. You will never quite know whether the CD 4017 will clock just one more time or sit on your lucky number six!   

## Building the circuit: 
The idea behind this progressive series is to add to each of the previous projects to make a more complex project. This way you will be adding a minimum of components and building new ideas at the least expense. Remove the HEADS and TAILS LEDs from the previous project and all the other parts which will not be needed. Notice that some of the wiring will remain in place so refer to the layout diagram before starting. Fit the six LEDs in the centre of the board as shown. They will need connecting wires to the output pins of the CD 4017 so follow the layout diagram carefully. Solder the other components in place and re-check all wiring. Connect the battery and the circuit will come on with one LED illuminated. Touching the TOUCH PLATE will cause the LEDs to flash at a very fast rate and gradually slow down with just one of them lit. We claim that the circuit is unbiased. But don't take our word for it. Complete your own statistical analysis of the circuit by taking 100 samples and putting the results in the following table:  

![](https://github.com/SteveJustin1963/TE-2-20-LED-DICE/blob/master/tbl.png)

Each time the LEDs stop, place a stroke in the aropriate space thus: / after each four strokes: //// the fifth stroke is placed across the four thus: ![](https://github.com/SteveJustin1963/TE-2-20-LED-DICE/blob/master/5.png) This makes the final counting easy as they are now in groups of five. Look at your results. Are the totals of each LED nearly the same? In an article to be presented in a few months, we will be adding a couple more componeats to this circuit and presenting it as a complete project on a printed circuit board. So wait for it.  

![](https://github.com/SteveJustin1963/TE-2-20-LED-DICE/blob/master/dice.png)

## Part list
* R1 10M 1/4watt
* R2 10M
* R3 10k
* R4 1k
* C1 electrolytic 1uF 16v
* C2 capacitor 100n 100v
* Q1 transistor BC 557
* IC1 timer IC NE 555
* IC2 decade counter CD 4017
* LED1 - LED6 Large Red LEDs
* battery clip
* 9v battery
* approx 30cm hook-up wire
* "Experimenter Board 3-ICs" 

