# Smart Incubator

### Arduino: 
Our design utilizes both Arduino and Photon because our temperature and humidity sensor, Adafruit Si7021, uses i2c output pins. While Arduino is implemented with the SCL and SDA pins, and already has an existing i2c library, we choose to collect the sensor data with Arduino. The Arduino Tx is collected with Photon Rx, so the data is transferred to Photon via serial communication. Notice this communication is 1 directional: only from Arduino to Photon.

### Heater: 
We initially used a pin on Photon to control the on/off of the heating resistors, but as the pin could only supply a 3.3V output voltage, not enough heat is generated. We instead use a 9V battery to power the heater. In tests, the resistors were quite robust and could withstand high temperature for a long time, but the battery couldn’t hold for a long before overheating. The maximum temperature we can reach is around 34 degrees Celsius, so if you really want to incubate some chicks, we suggest you use a better power supply to reach a higher temperature. 

### Fan:
Because of bad thermal transport efficiency in the air, a fan is needed to transfer heat to the eggs. It is necessary, and we have experimented that without the pan switched on, the heater needed an extremely long period of time to increase the temperature at the bottom of the incubator. 

### Humidity Control: 
A Good humidifier is needed to completely control the humidity level in the incubator, but that's too expensive. Considering eggs are tolerant to humidity, we just put a little water at the bottom of the incubator ,which can too keep the eggs healthy.

### Temperature Control: 
The heater right now is connected to a 9V battery, so the temperature control is achieved by controlling the on/off of the fan. On the webpage, the user is able to set the desired temperature. The fan will automatically start working when the current temperature is 5 degrees lower than the desired temperature and stop working 5 degrees higher. It is also possible for the user to manually switches On/Off of the fan and the LED light.

## Get Started
In order to use our incubator to hatch some lovely chicks, here are some instructions to set up. 

1. Power the device, and connect the wires.
2. Put the photon under a WiFi environment.
3. You can see the current temperature and humidity level on our webpage.
4. If you are not happy with the temperature, you are able to set a desired temperature.
5. The fan should start working if your desired temperature is 5 degrees higher than the current temperature.
6. The heating resistor should be connected to a power supply with 9V or higher. 
7. If you are using a 9V battery, do not overheat the battery.
8. Put some water at the bottom of the incubator. Remember to change the water often.
9. You are good to go.
    
#### ```/src``` folder:  
This is the source folder that contains the .ino, .html, and .js files and other necessary files to support our UI.

#### ```/docs``` folder:  
This is the documentation folder that contains helpful documentations and figuers that future users and developers may find handy. 

#### ```project.properties``` file:
We are not using any external library for photon. The one wire is listed here if future deceloper wants to switch the sensor. 
