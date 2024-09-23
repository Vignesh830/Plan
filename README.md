In this Arduino IoT project, I have explained how to make IoT-based home automation using Arduino UNO and ESP8266 ESP-01 to control relays with Google Assistant, Alexa, IR remote, and manual switches. You can also control the appliances and monitor real-time feedback in the Google Home and Amazon Alexa App from anywhere in the world.
You can also control the relays from the IR remote and manual switches if there is no internet available.
Here Arduino saves the previous state in EEPROM, so after power cuts when the power comes back appliances will automatically turn on according to the previous state.
For this project, I have used all the FREE tools. So if you follow all steps, you can easily make this Smart Home System with Google Home and Amazon Alexa to control the appliances with voice commands.
And you don’t need any Google Nest or Amazon Echo Dot devices for this voice control home automation project.

REQUIRED COMPONENTS TO ARDUINO PROJECT.
Arduino UNO or Arduino Nano
ESP8266 ESP-01
1838 IR receiver (with metal case)
1k, 2k, 4.7k resistors (1/4 watt)
5-mm LED
1117 3.3V voltage regulator
4-channel 5V SPDT Relay Module
Switches or Push Buttons
FTDI232 USB to TTL
5V DC supply


Circuit of the Arduino IoT Project using ESP-01


The circuit is very simple, I have used D4, D5, D6 & D7 GPIO to control the 4-channel relay module.
And the GPIO D10, D11, D12 & D13 are connected with switches to control the relay module manually.
The output pin of the IR receiver is connected with A0.
For the serial communication with the ESP-01, I have used D2 as RX and D3 as TX with the SoftwareSerial library.
Here I have made a voltage divider using 2k and 4.7k resistors to drop down the 5V logic level to the 3.3V logic level for the serial communication with the ESP-01 WiFi module.
I have used the INPUT_PULLUP function in Arduino IDE instead of using the pull-up resistors with each switch.
As per the source code, when the control pins of the relay module receive the LOW signal the relay will turn on and the relay will turn off for the HIGH signal in the control pin.
I have used an 1117 3.3V voltage regulator to supply the ESP01. 
If you use Arduino UNO then you can use the 3.3V pin instead of the 1117 3.3V regulator but for Arduino Nano, you have to use the 1117 3.3V voltage regulator.



If you want to use push-button for manual control, then just connect pushbuttons instead of latched switches.

Please take the proper safety precautions while working with high voltage.

I have used a 5V 2Amp DC power supply for the circuit.

Sinric Pro FREE account setup
For this smart house project, I have used the Sinric Pro Free account. First, you have to add 3 devices to the Sinric Pro account.



