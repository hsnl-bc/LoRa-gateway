# LoRa-gateway

## Example's Environment
**Module**: GL6509

**Platform**: Arduino
## Data Formating Rules
### Air Temperature & Humidity
空氣溫溼度
#### Payload
```
A1000{temperture}{humitdity}
```
#### Example
**Data command**: *ATX+DTX=length*

**Temperature**: 25°C, length=2

**Humidity**: 50.99%, length=4

> String
```
AT+DTX=11,"A1000255099"
```
> Arduino Concat Code
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
#### Example
**Data command**: *ATX+DTX=length*

**Temperature**: 25.88°C, length=4

**Humidity**: 50.99%, length=4

> String
```
AT+DTX=11,"S1025885099"
```
> Arduino Concat Code
```
String temperature="2588";
String humidity="5099";
String command="AT+DTX=11,\"S10"+temperature+humidity+"\"";
```
***If data length=5 (Not Tested)***

Change `S10` to `F1`

### Battery Voltage
電池電壓
#### Payload
```
B10000{voltage}
```
#### Example
**Data command**: *ATX+DTX=length*

**Voltage**: 12.50°C, length=5 (01250)

> String
```
AT+DTX=11,"B1000001250"
```
> Arduino Concat Code
```
String voltage="01250";
String command="AT+DTX=11,\"B10000"+voltage+"\"";
```

### Lux
光照度

### EC
土壤電導度
