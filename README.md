# LoRa-gateway

## Test Environment

**Module**: GL6509

**Platform**: Arduino

## Data Command
### Air Temperature & Humidity
空氣溫溼度
#### Payload
```
A1000{temperture}{humitdity}
```
#### Usage
**Data command**: *ATX+DTX=length*

**Temperature**: 25°C, length=2

**Humidity**: 50.99%, length=4

> String
```
AT+DTX=11,"A1000255099"
```
> Concatenate Code
```
String temperature="25";
String humidity="5099";
String command="AT+DTX=11,\"A1000"+temperature+humidity+"\"";
```

### Soil Temperature & Humidity
土壤溫溼度
#### Payload
```
S10{temperture}{humitdity}
```
#### Usage
**Data command**: *ATX+DTX=length*

**Temperature**: 25.88°C, length=4

**Humidity**: 50.99%, length=4

> String
```
AT+DTX=11,"S1025885099"
```
> Concatenate Code
```
String temperature="2588";
String humidity="5099";
String command="AT+DTX=11,\"S10"+temperature+humidity+"\"";
```
***If humidity data length=5 (Not Tested)***

Change `S10` to `F1`

### Battery Voltage
電池電壓
#### Payload
```
B10000{voltage}
```
#### Usage
**Data command**: *ATX+DTX=length*

**Voltage**: 12.50v, length=5 (12.50)

> String
```
AT+DTX=11,"B1000012.50"
```
> Concatenate Code
```
String voltage="12.50";
String command="AT+DTX=11,\"B10000"+voltage+"\"";
```

### Lux
光照度
***Not Finished***
### EC
土壤電導度
***Not Finished***
