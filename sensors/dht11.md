# DHT11 Temperature and Humididy Sensor

You will need to download and install a library to work with this sensor. In the Arduino IDE go to the "Tools Menu - Managle Libraries". Search for and install "DFRobot_DHT11" 

The sensor defaults to Celsius. The code below includes a conversion to Fahrenheit.

![Arduino with DHT11 wired](images/Arduino_DHT11.png)

```
/*!
 * @file readDHT11.ino
 * @brief DHT11 is used to read the temperature and humidity of the current environment. 
 *
 * @copyright   Copyright (c) 2010 DFRobot Co.Ltd (http://www.dfrobot.com)
 * @license     The MIT License (MIT)
 * @author [Wuxiao](xiao.wu@dfrobot.com)
 * @version  V1.0
 * @date  2018-09-14
 * @url https://github.com/DFRobot/DFRobot_DHT11
 */

#include <DFRobot_DHT11.h>
DFRobot_DHT11 DHT;
#define DHT11_PIN 10
int temp;

void setup(){
  Serial.begin(115200);
}

void loop(){
  DHT.read(DHT11_PIN);
  temp = DHT.temperature;
  temp = temp*9/5+32;
  Serial.print("temp:");
  Serial.print(temp);
  Serial.print("  humi:");
  Serial.println(DHT.humidity);
  delay(1000);
}
```
## Play and Learn
- Is it accurate?
- How quickly does the temperature reading change?
- How quickly does the humidity reading change?
