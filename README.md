# CubeServer-api-circuitpython

[![Maintainability](https://api.codeclimate.com/v1/badges/0ed05bb07ca3c9678002/maintainability)](https://codeclimate.com/github/snorklerjoe/CubeServer-api-circuitpython/maintainability)

The CircuitPython version of the data API wrapper for a high-school STEM competition


# Example code:
``` Python
from server import CubeServer, Text

print("Connecting to the server...")
connection = CubeServer()
print("Connected!")

connection.post(Text("Test from CircuitPython!"))

print("Getting status:")
print(connection.get_status())
```
-------------------------------------------------------------------


### Testing Status:
| MCU         | Description |
| ----------- | ----------- |
| ESP32       | Works       |
| ESP8266     | Incompatible|
| Raspi Pico W| Untested    |

The ESP8266 is currently incompatible with this micropython library due to lack of memory resources for handling the TLS handshake.
To use the ESP8266, please use the Arduino C wrapper.
