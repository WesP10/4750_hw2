<!---
If you're new to markdown, check out this reference: https://www.markdownguide.org/basic-syntax/
-->

# Writeup

## Q0. Investigating Transforms in Foxglove (10 pts)

**Q0.1:**

It moves forward along the positive red x-axis. Both wheels spin in the positive counter-clockwise directions.

## Q1. Identifying a Kinematic Model (20 pts)

**Q1.1:** 

Each wheel sits a distance $\frac{b}{2}$ from the robot's center. Rotating at $\omega$ adds a tangential speed of $\omega \frac{b}{2}$ to each wheel on top of the forward speed $\upsilon$. With $\omega > 0$ for a counterclockwise (left) turn, the right wheel speeds up and the left wheel slows down:

$$\upsilon_l = \upsilon - \frac{\omega b}{2}$$

$$\upsilon_r = \upsilon + \frac{\omega b}{2}$$



<!---
You can use LaTeX syntax like so: $a_{example} = b_{example} + c_{example}$.
You can use $\upsilon$ for linear velocity and $\omega$ for angular velocity.

If you prefer to write out your work, you can include it in an image as follows:
![image description](./image_path.png)
-->

**Q1.2:**

A wheel rolling without slipping covers its radius $r = \frac{d}{2}$ for every radian it turns, so $\upsilon = \dot{\phi} \, r$. Solving for the spin rate:

$$\dot{\phi_l} = \frac{\upsilon_l}{d/2} = \frac{2\upsilon_l}{d}$$

$$\dot{\phi_r} = \frac{\upsilon_r}{d/2} = \frac{2\upsilon_r}{d}$$

Both wheel axes point along $+y$ of `base_link` (Q0.1), so a positive linear wheel velocity gives a positive spin rate for both wheels.

**Q1.3:** 

Inverting the Q1.1 equations, adding them cancels the $\omega$ terms and subtracting them cancels the $\upsilon$ terms:

$$\upsilon_l + \upsilon_r = 2\upsilon \quad\Rightarrow\quad \upsilon = \frac{\upsilon_r + \upsilon_l}{2}$$

$$\upsilon_r - \upsilon_l = \omega b \quad\Rightarrow\quad \omega = \frac{\upsilon_r - \upsilon_l}{b}$$

The linear velocity is the average of the two wheel speeds. The angular velocity is positive (counterclockwise, left turn) when the right wheel is faster than the left.

## Q2. Inverse Kinematics (20 pts)

**Q2.2:** 

**Q2.3:** 

## Q3. Forward Kinematics (20 pts)

**Q3.2:** 

## Q4. Calculating an Odometry Solution (30 pts)

**Q4.3:** 


## Feedback

**How much time did you spend on this assignment?** 

**Do you have any feedback for this assignment?**
