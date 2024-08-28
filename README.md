# traincontroller
Traincontroller is intended to expand the old way to control rail (and other) models using DCC.
It is expected to maitain, for a while at least, DCC compatibility. 
New controllers will expand the control and monitoring capabilities including:
- wifi bidirectional connection for control and feedback
- bluetooth connection for vehicle teaming
- onboard g sensor and compass to detect movement, position, direction
- NFC reader for truck localization and advanced control
- advanced sound control based on full situational awareness and control
- advanced motion control based on full situational awareness and control

## General requirements
- (GR001) DCC compatibility is considered only for a subset of function provided by the traincontroller module. The traincontroller modules will provide all their features but can be also controlled using regular DCC for basic function
- (GR002) All but additional sensor are supposed to be on the decoder board and not require any modification of the model.
- Additional sensors (NFC, etc.) may require some modification like to install antennas and connecting wires. Wireless sensor may also be developed in the future
- (GR003) The controller board use rail power to function and to provide power to engine and other services (lights, etc.) and to communication layer. A controller can operate on battery power if the model is operated on battery power (usually large scales)
- (GR004) The controller is connected to the model using the standard decoder connector
- (GR005) Development of first version is based on large controller size (PLUX22 / 21xxx ). Future version may be implemented for lower size decoder.
- (GR006) Main control and communication channel is the wireless connection.
- (GR007) Full IP stack is implemented and large bandwidth is available for control and services
- (GR008) The controller has its own local interface for configuration, setup, direct control
- (GR009) The controller onboard can interact with a remote control center to perform global automation and management. Remote control center is IP connected and can be local, remote or cloud based.

## Wifi requirements



## Advanced Motion Control
### Basic Requirements
- (AMC001) Granular power/speed management. Minimum level of step 1/100
- (AMC002) Possibility to command specific variation of power/speed (from x to y or from current to y)
- (AMC003) Test function to determine minimum power for movement of the model in standard condition (flat, strait). Result is stored on the controller permanent memory
- (AMC004) Test function to determine power for realistic speeds of the model (maximum speed of real in scale, specific speeds, etc.) Results are stored on the controller permanent memory with specific keywords
- (AMC005) Possibility to command specific memorized speeds as stored in controller permanent memory.
