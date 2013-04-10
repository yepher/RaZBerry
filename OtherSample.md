The following data is sent/receive on the RaZberry board.

This is some scratch data to try and manually decode what the binary packets actually mean.

_Table: Switch Multi Level Switch Off_

|Value |Meaning |
|---|---|
|01| SOC|
|0a| LEN|
|00| REQUEST|
|13| SendData|
|07| NodeID|
|03| ???|
|26| SWITCH MULTILEVEL|
|01| SET|
|00| off|
|25| ???|
|03| ???|
|e3| CHECKSUM|




_Table: First frame sent from controller_

|index|Direction|Value|Decode Information|
|---|---|---|---|
|1 |TX|0x01| SOF (see Preambles below)|
|2 |TX|0x03| Length |
|3 |TX|0x00| 0x00-Request|
|4 |TX|0x07| SerialGetCapabilities |
|5 |TX|0xfb| Checksum - see _Generating a checksum_ below|

_Table: Response_

|index|Direction|Value|Decode Information|
|---|---|---|---|---|
| |RX|0x06| ACK (see Preambles below)| |
| |RX|0x01| SOF (see Preambles below)| |
| |RX|0x2b| Length 43 Bytes | |
| |RX|0x01| 0x01-Response | |
| |RX|0x07| SerialGetCapabilities| |
| |RX|0x04| Version | |
| |RX|0x02| Revision | |
| |RX|0x01| Manufacture ID1 | |
| |RX|0x47| Manufacture ID1 | |
| |RX|0x00| Product Type 1| |
| |RX|0x02| Product Type 2| |
| |RX|0x00| Product ID 1| |
| |RX|0x03| Product ID 2| |
| |RX|0xfe| | |
| |RX|0x00| | |
| |RX|0x16| | |
| |RX|0x80| | |
| |RX|0x0c| | |
| |RX|0x00| | |
| |RX|0x00| | |
| |RX|0x00| | |
| |RX|0xe3| | |
| |RX|0x97| | |
| |RX|0x7d| | |
| |RX|0x80| | |
| |RX|0x07| | |
| |RX|0x00| | |
| |RX|0x00| | |
| |RX|0x80| | |
| |RX|0x00| | |
| |RX|0x00| | |
| |RX|0x00| | |
| |RX|0x00| | |
| |RX|0x00| | |
| |RX|0x00| | |
| |RX|0x00| | |
| |RX|0x00| | |
| |RX|0x00| | |
| |RX|0x00| | |
| |RX|0x02| | |
| |RX|0x00| | |
| |RX|0x00| | |
| |RX|0x80| | |
| |RX|0x07| | |
| |RX|0x00| | |
| |RX|0x7c| Checksum| | 


_Table: (Switch Binary Set)_

|index|Direction|Value|Decode Information|
|---|---|---|---|
|1  |TX|0x01| SOF (see Preambles below)|
|2  |TX|0x0a| Length |
|3  |TX|0x00| 0x00-Request|
|4  |TX|0x13| SendData |
|5  |TX|0x09| Node ID|
|6  |TX|0x03| 3-BinarySet (2-BinaryGet) |
|7  |TX|0x25| BINARY_SWITCH|
|8  |TX|0x01| Set value? (is this [SET, GET, REPORT]?)|
|9  |TX|0x00| 0x00-Switch off (0xff=ON) |
|10 |TX|0x25| |
|11 |TX|0x03| |
|12 |TX|0xee| Checksum - see _Generating a checksum_ below|

_Table: Random decodes_

|nodeId|  |  | |  |Description|
|---|---|---|---|---|---|
|18|2|30|2|5| Sensor Binary Get|
|9|3|25|1|ff 25| BINARY_SWITCH Set|
|9|2|25|2|25| BINARY_SWITCH Get|
|9|3|25|1|0 25| BINARY_SWITCH Set|
|9|2|25|2|25| BINARY_SWITCH Get|
|9|3|25|1|0 25| BINARY_SWITCH Set|
|9|2|25|2|25| BINARY_SWITCH Get|



Random Capture
===============

|Direction|Hex|Dec|Description|
|---|---|---|---|
|>| 0x01|1|
|>| 0x08|8|
|>| 0x00|0|
|>| 0x04|4|
|>| 0x00|0|
|>| 0x28|40|
|>| 0x02|2|
|>| 0x84|132|
|>| 0x07|7|
|>| 0x5a|90|
|<| 0x06|6|
|<| 0x01|1|
|<| 0x09|9|
|<| 0x00|0|
|<| 0x13|19|
|<| 0x28|40|
|<| 0x02|2|
|<| 0x84|132|
|<| 0x08|8|
|<| 0x05|5|
|<| 0x20|32|
|<| 0x66|102|
|>| 0x06|6|
|>| 0x01|1|
|>| 0x04|4|
|>| 0x01|1|
|>| 0x13|19|
|>| 0x01|1|
|>| 0xe8|232|
|<| 0x06|6|
|>| 0x01|1|
|>| 0x05|5|
|>| 0x00|0|
|>| 0x13|19|
|>| 0x20|32|
|>| 0x00|0|
|>| 0xc9|201|
|<| 0x06|6|
|>| 0x01|1|
|>| 0x0b|11|
|>| 0x00|0|
|>| 0x04|4|
|>| 0x00|0|
|>| 0x04|4|
|>| 0x05|5|
|>| 0x31|49|
|>| 0x05|5|
|>| 0x01|1|
|>| 0x09|9|
|>| 0x47|71|
|>| 0x8a|138|
|<| 0x06|6|
|>| 0x01|1|
|>| 0x09|9|
|>| 0x00|0|
|>| 0x04|4|
|>| 0x00|0|
|>| 0x04|4|
|>| 0x03|3|
|>| 0x42|66|
|>| 0x03|3|
|>| 0x00|0|
|>| 0xb4|180|
|<| 0x06|6|


