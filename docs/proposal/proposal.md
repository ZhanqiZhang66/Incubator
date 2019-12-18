# 0. Bonus Points
- We would use the hardware not introduced in class: Adafruit S17021 temperature and humidity sensor.
- Interesting Designs: Our design of the incubator is very creative and we would include the actual mechanical design of a incubator(not just using led to represent the model).


# 1. Description
We will program and design an ioT egg incubator that uses feedback control to help the users to incubate eggs without any hatching chicken. The user will monitor and control the temperature and humidity in the incubator and then make sure the eggs could be incubated successfully by creating a constant and comfortable environment inside the incubator for the eggs. The user could also set up the type of the eggs on the apps or website so that we can provide optimized default incubating settings. The incubator would also have a LED to provide light in the incubator. We can create an incubator out of plastic bottles and some electronic elements like wires and resistors. A fan is used to provide ventilation for the eggs and resistors are used to heat up the wind when needed. The most costly elements would be the photon, so the product is cheap and easy-to-use. An embedded system is used so that we shall have sensors and actuators to feedbacks control the temperature inside the incubator. An user-friendly website would offer the user graphical sliders and other information of the incubator. Lastly, the networking infrastructure enables the user to monitor the incubator remotely and thus they could be able to control the temperature at a constant level and help eggs incubate.

The expected users would be people who are interested in hatching eggs and get cute little birdies at home or farm owners who want to have a cheap and intelligent incubator.

The problem that our product will assist with is to create an easy-to-use incubator that could be remotely controlled and monitored, and mostly importantly, could incubate eggs without the help from hatching chicken.

The use of ioT is beneficial because the product is simple and user-friendly compared with other similar product. As the same time, it costs very little money since the most expensive component would be the photon, which is still in an acceptable price.
# 2. Hardware and Cloud Infrastructure Needed

## Hardware:
1. Motors with gears(used as a fan)
2. LED.
3. Resistors,
4. wires
5. Adafruit S17021 temperature and humidity sensor
 (Description: ± 3% relative humidity measurements with a range of 0–80% RH
±0.4 °C temperature accuracy at a range of -10 to +85 °C
  Great for all of your environmental sensing projects   
  It uses I2C for data transfer so it works with a wide range of microcontrollers.)

## Cloud Infrastructure:
particle.io , if we have enough time we will also use slack with webhook to produce daily report of the eggs.
# 3. Unknowns and Challenges
We don't have the humidity sensor and we need to buy the Adafruit S17021 temperature and humidity sensor board online.
# 4. User Stories & Usage Scenarios
The user will monitor and control the temperatures in the incubator and then make sure the eggs could be incubated successfully by creating a constant temperature environment inside the incubator. The user could also set up the type of the eggs on the apps or website so that we can provide optimized default incubating temperature.
# 5. Paper Prototypes
Please see the picture uploaded
![paper prototypes](/docs/proposal/diagrams/paperPrototype.jpg "The Prototype")
The website has three stages:
1. welcome page with loading
2. egg mode selection to have different programed environment for the eggs
3. control and monitor the temperature and humidity of the egg.

The user is able to control the temperature and humidity from the website(see above). User could also choose the type of egg as the mode of the program. The temperature and the humidity readings would also show on the screen to give the user feedback.
# 6. Implementation: Sequence Diagrams
```
title Incubator Project
participant particle
participant cloud
participant UI
particle->cloud: detect temp and humidity

cloud->UI: Temp and humidity Response

UI->cloud:  set temp and humidity
cloud->ino: set temp and humidity
```
![Sequence Diagram](/docs/proposal/diagrams/IncubatorProject.png "The Sequence Diagram")

The data was transferred from the hardware to the cloud and then to the UI. The user will control and adjust the setting of the temperature from the feedback he received and send the command to the cloud and then to the hardware.
# 7. Plan and Schedule
We plan to meet twice a week to discuss the implementation and do the coding and wiring. We put the meeting time as the time after class every Monday and Wednesday and we are going to create a google doc to keep track of the work. In the first week we will buy the humidity sensor and setup all the hardware we need. In the second week we will start coding the UI(website) and the .ino file to read the data from the temperature and humidity sensors. We are planning to use the third week to handle any possible errors that happened during the process of implementation and optimize the code. In this week we will also have cloud Infrastructures implemented. The last week would be used to finalize the project and test edge cases.  
## Weekly Schedule / Progress

| Week End     | Deliverables & Accomplishments |
|:-------------|:-------------------------------|
| By Nov 16    |  plan: Hardware                              |
| By Nov. 23   |  plan: js and ino                              |
| By Nov. 30   |  plan: cloud                              |
| Dec. 3       |  Must do: Complete Project Due!         |

## Group Member Responsibilities (Groups only)

| Name         | Responsibilities |
|:-------------|:-----------------|
|   Victoria Zhang           |        Hardware js          |
|   Xingjue Liao           |       Hardware ino cloud          |

## Times Reserved for Project Work

Fill in a schedule of times reserved for the project.  If you can't set regular weekly times, create a schedule based on specific days.

| Week Day | Times | Who (if on a team) |
|:---------|:------|--------------------|
| Monday   |  4:00-5:30     |     Both               |
| Tuesday  |       |                    |
| Wednesday|  4:00-5:30     |     Both               |
| Thursday |       |                    |
| Friday   |  11:00-1:00     |       Both             |
| Saturday |       |                    |
| Sunday   |       |                    |
