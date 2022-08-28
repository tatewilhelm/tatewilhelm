---
title: The Application and Use of 2 Joint Inverse Kinematics for General Robotics.
date: 2022-08-28T11:34:39-06:00
tags: [engineering, programming, research]
---

> This is an article version, hence equations won't look how they were originally written. The actual PDF version is available [here.](/archive/research/The%20Application%20and%20Use%20of%202%20Joint%20Inverse%20Kinematics%20for%20General%20Robotics.pdf)

## Background
Readers should have a basic understanding or background in the following concepts:
* Basic trigonometry
* How to work with angles
* Basic programming with angles

## Motivation
I have been building a bipedal robot over the summer of 2022. I have needed easy, simple, straight to the point resources on control concepts that are necessary to create walking gaits for the bipedal robot. One of the concepts necessary for these gaits, is inverse kinematics. Inverse Kinematics is in the valley of being easy enough for people who understand it easily to often not create easy resources, and being hard enough for the average person not being able to grasp the concept quickly. 

My goal with this resource is to create a easy way for people to understand the math behind Inverse Kinematics, and a way to easily implement it on their robotics project.

## Terminology
Inverse Kinematics – The mathematical equations to finding the angles needed for a arm to reach a certain position at the end of the arm.

Arm – Defined as a controllable double pendulum, generally controlled by a series of motors and a micro controller.

Joint – Defined as a single pendulum on a arm. Both must be the same length.

## Mathematical Definitions
***J*** is defined as the length of both joints.

***T*** is the target coordinate of the endpoint of the arm.

## Inverse Kinematics Equations

<img src="/ik.png" alt="Example" width="400"/>

You may notice how arms, at any position, will create two triangles back to back. We can use this to our advantage, because trigonometry is so easy to grasp.

First, we must find the Φ, which is the angle between the X axis, and the imaginary line that connects the endpoint of the arm and the origin.

The equation for Φ uses the inverse tangent function to find the angle from both the opposite and adjacent. The equation to find Φ is the following: 

**Φ = tan^-1 (Ty / Tx)**

Now that we have Φ, we need to find the length of the imaginary line connecting the origin and ***T***, we’ll call this variable ***B***, for base. We can find ***B*** by using this equation:

**B = Tx / (cos Φ)**

We only need one more variable to get the final angles of our arm. We need to find Θ, which is the angle from the imaginary base, from which we calculated length last step, to the first joint of the arm. We can do this by halving the base, because we’re trying to find the angle of single triangle, and using the joint length to find our angle between the base and the joint. The equation looks like this:

**Θ = cos^-1 (.5B / J)**

Now that we have our variables, we can finally get the angles to set each arms. The math here is pretty simple: to find the angle from the X axis to the first joint, we add Φ and Θ: **A1 = Φ + Θ**. To find the difference in angle from the first joints angle to the second joints angle we simply subtract:  **A2 = Φ - Θ**.

A complete calculation looks like this:

**Φ = tan^-1 (Ty / Tx)**

**B = Tx / (cos Φ)**

**Θ = cos^-1 (.5B / J)**

**A1 = Φ + Θ**

**A2 = Φ - Θ**

## Implementation

The following is a step by step way to implement inverse kinematics in a systematic environment, like computers and microprocessors.     

1. Get the Target X, and Y Position, ***Tx***  and ***Ty***, respectively
2. Get the Joint Length, ***J***
3. Calculate Φ via the equation **Φ = tan^-1 (Ty / Tx)**
4. Calculate the base length, ***B***, via the equation **B = Tx / (cos Φ)**
5.  Calculate Θ via the equation **Θ = cos^-1 (.5B / J)**
6.  Calculate the first angle, ***A1***, via the equation **A1 = Φ + Θ**
7.  Calculate the second angle, ***A2***, via the equation **A2 = Φ - Θ**
8. If necessary, adjust the first and second angles before setting the motors/servos to them. (IE: flipping angles, or adding 90° to second angle.) This is dependent on the motor/servo itself, and the controller used.

## Resources

The following resources have helped me immensely in creating this document. A massive thanks to all of these people and their works!

*Information*:

* https://youtu.be/Q-UeYEpwXXU – RoTechnic, “Easy inverse kinematics for robot arms”, January 23rd, 2022

* https://youtu.be/IN8tjTk8ExI – James Bruton, “How Robots Use Maths to Move”, March 2nd, 2021

*Tools used*:

* https://www.desmos.com/ - Desmos Studio

* https://www.libreoffice.org/ - The Document Foundation

