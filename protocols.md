# Communication Protocols

## What are communication protocols?
- Communication protocols are the set of rules that allow two or more electronic devices to connect and exchange data with each other.

---

## RS-232 Communication Protocol
- Standard protocol used for serial communication.
- Uses the binary system to transmit data in ASCII format.
- Serial communication up to 50 feet (15.24 meters) with a rate of 1.492 kbps.
- Two-way communication.
- Similar to UART but supports longer cables.

### RS-232 Characteristics
- 2 devices.
- Short distance (<20m).
- More sensitive.
- Slow data rate (kbps).

### How does RS-232 work with Arduino?
- The Arduino Mega uses TTL UART (0V - 5V levels), but RS-232 uses ±12V signaling, which can damage the Arduino's pins.
- You need an RS-232 to TTL converter module.

### RS-232 Wiring
1. Connect Arduino TX (Pin 18 - TX1) to MAX232 TTL RX.
2. Connect Arduino RX (Pin 19 - RX1) to MAX232 TTL TX.
3. Connect MAX232 RS-232 TX to the external device's RS-232 RX.
4. Connect MAX232 RS-232 RX to the external device's RS-232 TX.
5. Power MAX232 from Arduino's 5V and GND.

---

## RS-485 Communication Protocol
- Duplex communication system in which multiple devices on the same bus can communicate in both directions.
- Multi-drop and two-wire type of communication that allows communication with multiple devices at the same time.
- At a time, 32 devices can be connected on the same line.
- Maximum distance: 1200 m.
- Many PLCs allow connections of up to 128 slave nodes.
- 2-wire or 4-wire network.
- The 4-wire network is bidirectional, and the 2-wire network is unidirectional.

### RS-485 Characteristics
- 32 devices.
- Long distance (1000m).
- Less sensitive.
- Fast data rate (Mbps).
- Two-wire (half-duplex) and four-wire (full-duplex) configuration.

### How does RS-485 work with Arduino?
- To use RS-485 with an Arduino, you need an RS-485 transceiver module.
- To convert TTL signals to RS-485 differential signals, use:
  - MAX485, SN75176, or an RS-485 shield.
### RS-485 wiring

![RS-485 wiring](<Screenshot 2025-03-22 122207.png>)
---------
TTL vs RS-232 vs RS-485
![TTL vs RS-232 vs RS-485](<Screenshot 2025-03-22 115327-1.png>)
# Refrences 
## RS-232
- [RS-232 Wikipedia](https://en.wikipedia.org/wiki/RS-232)
- [RS-232 Technical Info](https://www.arcelect.com/rs232.htm)
- [RS-232 Communication Video](https://youtu.be/B4zKVwu0RLo?si=fGwZjCr4p8cR6SSw)
- [Interfacing Arduino with RS-232](https://embeddedthere.com/how-to-interface-arduino-with-rs232-communication-protocol/)

## RS-485
- [Arduino RS-485 Guide](https://arduinogetstarted.com/tutorials/arduino-rs485)
- [RS-485 Explanation Video 1](https://youtu.be/h-7xYe9yS3k?si=5zCPH6m4ZuWTF3QN)
- [RS-485 Explanation Video 2](https://youtu.be/05XnE9ljgsU?si=oP_6vJMw-XHwmrkI)
