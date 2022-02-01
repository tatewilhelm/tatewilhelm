---
title: Ultimate Goal was a weird season.
date: 2021-11-14T013:35:43-06:00
tags: [community, school, engineering, first-robotics, programming]
---

Last year, I had my first FTC competition. If you don't know what FTC is, FTC is a robotics program for middle and high schools.

My school offers a robotics elective from grades 7 - 12th, so I thought "Oh that'll be cool instead of keyboarding class, and I've done First Lego League I'll do it." That probably changed my life, but that's a story for another day. 

## The challenge
That years challenge was Ultimate Goal, in which the goal, (no pun intended,) was to shoot rings into a tower. And drop a wobbling pin into certain areas. That was the bare-bones explanation, I highly recommend you watch the [game animation on YouTube.](https://www.youtube.com/watch?v=k2pgPQgHQ28) 

## The engineering
Our robot design was relatively simple compared to others. 

Our drive base was a simple mecanum wheel train that could drive in any direction. We put control systems above everything on the robot as to provide a convenient way to access cables, and because it gave us a lot more room.

For shooting rings, we had an intake with surgical tubing attached, that would grab the ring by the hole, take it to an indexer made of an old yard sign, then a servo would push a ring out of the indexer into a 6000 RPM motor that would shoot the ring. The servo was also the perfect height to prevent 2 rings from coming out at the same time, similar to a vending machines mechanism.

We also made an arm that would grab the wobbling pin (called a wobble goal), lift it, and take it to said certain area. It was very basic, ran by chain drive and a small motor.

## The Programming
The programming this year was, eh. 

Look I didn't know Java then, and I barely knew C++. I have improved a considerable amount since then, but it still was eh.

We made a 4 stage TeleOp, it would:
1. Initialize the variables and Robot.
2. Get controller input.
3. Set motors according to input.
4. Send telemetry, in a pretty menu that took me 2 days to make.

We also made an autonomous using EasyOpenCV, that would get the ring starting stack position. ([Watch the game animation](https://www.youtube.com/watch?v=k2pgPQgHQ28) if you dont know what that means.) Then move according to that position, drop the pin, then park on a line.

Our programming project for this year was FTCTester. Too often would I have to take 10 minutes to write a program that would test motors or servos for our builders. So, FTC Tester was a solution to that problem by allowing people to move motors, or test servos on the fly.

All of our code from this year is available [here](https://github.com/ftc17191/ultimate-goal).

## Community Service

This year as our community service project, we raised money for our local SnakPak program. SnakPak is a local program dedicated to ending hunger in schools. Too may kids, the only meal they have, is at school. Which is geniuinely terrifying. Its scary to think about it.

We held a change drive and the grade out of the middle school that raised the most money, got an extra 30 minutes at lunch.

## Conclusion
This year was my first FTC year, it was really fun and a great experience.
