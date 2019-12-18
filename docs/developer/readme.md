Arduino: Our design utilizes both Arduino and Photon because our temperature and humidity sensor, Adafruit Si7021, uses i2c output pins. While Arduino is implemented with the SCL and SDA pins, and already has an existing i2c library, we choose to collect the sensor data with Arduino. The Arduino Tx is collected with Photon Rx, so the data is transferred to Photon via serial communication. Notice this communication is 1 directional: only from Arduino to Photon.

Heater: We initially used a pin on Photon to control the on/off of the heating resistors, but as the pin could only supply a 3.3V output voltage, not enough heat is generated. We instead use a 9V battery to power the heater. In tests, the resistors were quite robust and could withstand high temperature for a long time, but the battery couldn’t hold for a long before overheating. The maximum temperature we can reach is around 34 degrees Celsius, so if you really want to incubate some chicks, we suggest you use a better power supply to reach a higher temperature. 

Fan: Because of bad thermal transport efficiency in the air, a fan is needed to transfer heat to the eggs. It is necessary, and we have experimented that without the pan switched on, the heater needed an extremely long period of time to increase the temperature at the bottom of the incubator. 

Humidity Control: A Good humidifier is needed to completely control the humidity level in the incubator, but that's too expensive. Considering eggs are tolerant to humidity, we just put a little water at the bottom of the incubator ,which can too keep the eggs healthy.

Temperature Control: The heater right now is connected to a 9V battery, so the temperature control is achieved by controlling the on/off of the fan. On the webpage, the user is able to set the desired temperature. The fan will automatically start working when the current temperature is 5 degrees lower than the desired temperature and stop working 5 degrees higher. It is also possible for the user to manually switches On/Off of the fan and the LED light.