# Chapter 1: Basic MicroController Functionalities

This set of exercises are meant to discover the basic components that a embedded dev might manipulate dayly. Those exercises will show you how a micro controller or a dev board without OS can interact with different physical object and the world around it. Your job as a embedded Dev is to write consistent and reliable code to make the product functionning without crashing, writting drivers to any piece of electrical components to convert analog signals to numerical, giving an easy to use and precise abstraction between the Software, the Hardware and the Physcal world.

Embedded and Firmware design is one of the most complex field of computer science (there is no computer science without Embedded, Firmware and System design). Regrouping Mathematics, Mechanics, Physics, Electrical, Energy and Programming, this field demand you to not be a simple developper that only write decent code but an expert in it, having a lot of curiousity, resilience and having a grasp on many technical Domain that are not related to programming in any way.

Here in 42 we trust in peer to peer learning, proved that it works in CS field now it is time to elevate the thing to engineer level. Don't stuck on a problem alone, search, ask, try, retry and learn will be your MOTO. 

## Material
*Here is the needed material for this set of exercise*

- MCU of any kind
- Breadboard
- LEDS x4
- Resistor 
- Push button
- Potentiometer

## Exercise 1: Hello World

This is it, you've crossed the line, see yourself as the new best Inventor of our time, the Nikola Tesla of the XXI century ! But hold on buddy ! Every famous genius has to beging somewhere, Nikola (Nik' the Goat) didn't revolute the whole world and bringing energy, movement to a whole country in his first day on earth. He started there, trying to light incandescent lights. Now it's your turn to walk this path !

**Take a LED, a Resistor, an Arduino or any MCU** AND LIGHT THE SHITTOUT OF THAT THING !

*Function Definition:*

```C
void    set_light();
```

## Exercise 2: Night Sky

You did it, damn you're a though one... Your path is now a bit brighter but still envelop within the Night, a looong and daaark night. But what is a Night Sky without it Stars ?

You got it, **add more leds** (at least 3 in total in your circuit).

*Function Definition:*

```c
void    set_multiple_led();
```

Think about your circuit, how much it would cost to make it ? How much energy it consume ?

## Exercise 3: Time past...

What a wonderfull night sky you created, leds are illuminating more on more the path, stars shines in the sky, what a time to be alive. But everything comes to an end, it is the same rule for everyone in the universe. The time will take us all, your leds indeed ! Make them resonate one last time and END. THEIR. LIFE !

Now that you know how to build some tiny circuits and Light multiple leds, it is time to make them **blink**
Create one function to make one led blink periodically.
Create another one to make multiple led blink in multiple pattern.

*Function Definition:*

```C
void    blink_led(uint32_t *actual_time);
void    blink_matrix(uint32_t *actual_time);
```

Think about how do your organize your data, your components. What functionnality to use in the MCU ? What are the pros/cons of that function ? How do you handle time ? Is it safe ? Is it really periodical ?

## Exercice 4: Chenillard

Now that you have the basic of turning a LED on, let's try to make some motif with multiple LEDS. I'll challenge you to make what we call a 'chenillard' which is multiple LEDS organize in a line and a motif like snake from the game go along the line of LEDS from one side to an other. The movement must be fluid and periodic. Good Luck ! 

*Function Definition:*
```C
void    Chenillard(uint32_t *led_matrix);
```

## Exercise 5: Keep in touch

So you now how to make some tiny logic within a MCU and light some LED, form the moment your controller only output some voltage or apply some hardcoded logic within a loop. 

But how can we build something that we can interact with ? With a Button for sure ! Grab a push button, wire it and make a program that light two led, one on the left the other on the right. If we push one time on the button, the first led light on, second time the right led light on and the left light off, third time it is both of the LED that light on.

*Function Definition:*
```C
void    button_logic(uint32_t *leds);
```

## Exercise 6: Analog Conversion

We learned how the MCU can interct directly with the user using a button, now let's discover one of the most important things a MicroController, Analog signals.

Analog Signals are the interface between a MCU/Computer, which works with discrete logical value, and the physical world, founded by multiple type of NaturalPhenomena. An analog signals will be created a continuous, time-varying electrical signal from a sensor and the MCU will convert it into discrete value that it can work with.

In this exercise we will try to learn to listen to an Analog Signal using a potentiometer and depending of the mesured value we will light N-LED.

Build a circuit using four LED aligned, and depending on the value measured by the potentiometer, the MCU will light on 0, 1, 2, 3 or 4 Leds.

*Function Definition:*
```C
void    Analog_convertor(t_led *leds, t_value *value);
```


## Exercise 7: Chenillard Ultimate

Alright you master the GPIO of the MCU, you can write some simple but essential program on a Developpment Board, you can interact physically with your controller with button and potentiometer, let's mix everything together as the final exercise of this chapter !

Let's build the ULTIMATE CHENILLARD OF DEATH !!!!

This Challenge will require to regroup everything you learned in this Chapter. You will have to: 
- Build a chenillard
- Change the speed of the chenillard using the Potentiometer
- Change the direction of the chenillard using the button

*Function Definition:*
```C
void    ultimate_chenillard(t_led *leds, t_button *button, t_speed *speed);
```

## Ressources

*Exercises Set written by RoiShigai/melschmi*
