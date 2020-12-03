# mijia
Simple script to report temperature, humidity and battery level of Xiaomi
Mijia Bluetooth Temperature and Humidity Sensor. 
Requires gatttool,bc and xxd tools to be installed.

On Ubuntu 18.04 these packages can be installed with 
```apt install xxd bc bluez```

Temperatures returned are Celsius degrees.

You could add it in cron to do this repeatedly.

## Usage

```
./mijia_mqtt.sh -a [address] -n [sensor name]

Mandatory arguments:

-a  | --address           Bluetooth MAC address of sensor.
-n  | --name              Name of the sensor to use for MQTT.

Optional arguments:

-r  | --retries           Number of max retry attempts. Default 6 times.
-d  | --debug             Enable debug printouts.
-h  | --help
```
