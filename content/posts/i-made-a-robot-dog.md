---
title: I attempted to make a robot dog, and it was bad.
date: 2022-03-08T21:55:13-06:00
tags: [engineering, programming]
---

If you haven't seen a video of Boston Dynamic's Spot, [watch one](https://www.youtube.com/watch?v=wlkCQXHEgjA&ab_channel=BostonDynamics). It's so cool! Usually robots in the real world are just in factories, and not really like the fake old fasioned robots that can walk around and speak with that weird monotone voice. We may not be at the monotone voice part, (Good. That would be creepy.) but they are still extremely interesting. 

I thought making a robot dog would be a great project for learning arduino, and electronics a lot better. I did learn alot, but the project as a whole was a failure. Which is fine, I'm glad I learned compared to just failing and giving up.

The dog's name, Zeus, was named after [Space X's Spot, which is used to collect data from prototype rockets.](https://spaceexplored.com/2021/04/22/spacex-robot-dog-starship/)

## The inspiration

As I mentioned earlier, a lot of the inspiration for my robot was based off Boston Dynamics Spot. The colors of yellow and black looked really great, and so I ~~stole~~ took inspiration from the pretty parts of the design.

I took mechanical / electrical inspiration from [Good Boy](https://www.instructables.com/GoodBoy-3D-Printed-Arduino-Robot-Dog/), and arduino based robot dog. A lot of the electronics are based off of Good Boy.


## The design



{{< figure src="/back-view.png" title="Back View" height="250" >}}



{{< figure src="/right-view.png" title="Side View" height="500" >}}





I think I have 3 major flaws with the actual mechanical design of the robot. 

1. No screws were used, just super glue.

This was the worst flaw of the robot. I thought that super glue would make using screws in CAD easy, and make it alot more structural. It turns out super glue is not as strong as I thought. While it stuck, if it took more than a pound of pressure, it would just break.

2. The only support for the legs, were the servos. 

While, for the knee this wasn't much of a problem. It was a big problem for the shoulders. The shoulders had so much force on them that the broke a lot.

[If I were to do this again,](https://www.youtube.com/watch?v=x0f84YbjbXg) I would definitely integrate the shoulders inside of the robot, and have the other end of the shoulder attached to a free spiinning axis, for stabillity.

3. The servos power system had a power of about 0.5 amps, when they needed about 2 amps. 

I was really new to electrical engineering, so I though the servos would just be really weak, but it would still work. That is not what it did. It drew so much power that it broke the arduino's programmer. How? I still dont know. But good lesson learned there: _have a proper power supply._


## The electronics

Zeus used an Arduino Uno to control the servos, and used a sensor shield for easier connecting of wires. 

We had a a [Adafruit Powerboost 1000C](https://www.adafruit.com/product/2465) powering the arduino, which was great! The problem came when powering the servos. [I just used the power from the 5v pin.](https://www.youtube.com/watch?v=PcR_wdAMkOs&ab_channel=AHMEDYT)

[If I were to do this again,](https://www.youtube.com/watch?v=x0f84YbjbXg) I would definetly take a prototype PCB and make a positive and negative rail, and pwoer all the electronics like that.

## What I learned from this... experience.

A big lesson I learned was: PLAN EVERYTHING. Maybe not exactly everything to a tee, but you cant just go willy nilly into something expecting it to work. Zeus never worked! I'm still glad I did it, but it was failure!

But maybe thats ok, as I alluded to above, I plan to make another dog. So this was great to just try it out, dip my feet in, and come back stronger.






 