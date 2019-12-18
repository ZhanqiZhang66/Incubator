# Goal and Introduction
We will program and design an ioT egg incubator that uses temperatures feedback control to help the famer to incubate eggs without the hatching chicken.  The user will monitor and control the temperatures in the incubator and then make sure the eggs could be incubated successfully by creating a constant temperature environment inside the incubator. The user could also set up the type of the eggs on the apps or website so that we can provide optimized default incubating temperature. The incubator would also have a LED to provide light in the incubator. We can create an incubator out of plastic bottles and some electronic elements like wires and resistors. A fan is used to provide ventilation for the eggs and resistors are used to heat up the wind when needed.

The most costly elements would be the photon, so the product is cheap and easy-to-use. An embedded system is used so that we shall have sensors and actuators to feedbacks control the temperatures inside the incubator. An user-friendly website would offer the user graphical sliders and other information of the incubator.

The networking enables the user to monitor the temperatures and thus they could be able to control the temperature at a constant level and help eggs incubate.


We plan to meet twice a week to discuss the implementation and do the coding and wiring. We put the meeting time as the time after class every Monday and Wednesday and we are going to create a google doc to keep track of the work. In the first week we will buy the humidity sensor and setup all the hardware we need.

# Progress Made
We bought all the sensors and circulation fans we need for the project. We also soldered the resistors with an appropriate resistance to generate the heat. The resistors was then wired on the fans with a  led. Please refer to the picture below:

On the software side, we complete the basic structure of the websites with a home page and a control page.
![Fans](/docs/progress3.png "Fans we used")

![soldering](/docs/progress2.png "Soldering the resistor")

![Heater](/docs/progress1.png "The Heater we are building")
# Problems and potential concerns
We are a little concerned whether our resistor heater could generate enough heat. Because the photon has a build-in self-protection, we can't use a 2 Ohms (12*4.7Ohms) resistor which would trigger the self-protection of the photon and open-loop the circuit. However, we soldered another 4 Ohms resistor (12* 47Ohoms) and it could heat up without triggering the self-protection technique in the photon and works pretty good so far. We still need to test on the temperature of the hot wind coming from the fans and resistors to make sure it could generate enough heat.

# Priorities for the next week
We will wrap up the UI design and program the sensors for the incubator.
