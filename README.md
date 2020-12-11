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

Optional arguments:

-n  | --name              Name of the sensor to use.
-r  | --retries           Number of max retry attempts. Default 6 times.
-d  | --debug             Enable debug printouts.
-h  | --help
```
## Find MJ_HT_V1
```
root@gen8:~/mijia# hcitool lescan
LE Scan ...
58:2D:34:3A:79:EB (unknown)
58:2D:34:3A:79:EB MJ_HT_V1
```
# Example
```
root@gen8:~/mijia# ./mijia.sh -a 58:2D:34:34:41:18

Temp:17.3
Humid:54.0
Batt:100
```
