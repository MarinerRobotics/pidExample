Tuning Methods
Zeigler-Nichols tuning method works by increasing P until the system starts oscillating, and then using the period of the oscillation to calculate I and D.

Start by setting I and D to 0.
Increase P until the system starts oscillating for a period of Tu. You want the oscillation to be large enough that you can time it. This maximum P will be referred to as Ku.
Use the chart below to calculate different P, I, and D values.
Control Types	P	I	D
P	.5*Ku	-	-
PI	.45*Ku	.54*Ku/Tu	-
PID	.6*Ku	1.2*Ku/Tu	3*Ku*Tu/40
Note

The period of oscillation is one full ‘stroke’, there and back. Imagine a grandfather clock with a pendulum, when it is all the way to the right, swings to the left, and hits the right again, that is 1 period.

Which ones to use
Feedforward control is necessary on all but the absolute simplest of systems. It’s incredibly difficult to get a good response without a feedforward calculation.

P control is best used on slow moving parts that aren’t subject to overshooting, or parts of the robot that don’t need complete accuracy. Turning to a certain degree, for example, can be done with just P in some cases (but not all).

The most common control loop is PI. It combines simple P control with the fine tuning feature of an Integral gain. This is teams are most likely to use.

Complete PID may be overkill for an FRC robot, but if you find that PI isn’t working enough, feel free to add D gain
