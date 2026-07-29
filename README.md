# Li-Fi-audio-transmission
A prototype wireless communication system that utilizes Visible Light Communication to stream real-time audio through free space using an LED transmitter and a solar panel.

# Overview
Traditional wireless communication relies heavily on Radio Frequencies(RF), which suffer from electromagnetic interference, bandwidth congestion and security vulnerabilities. This project demonstrates an alternative approach: Li-Fi(Light Fidelity).
The system captures audio inputs, modulates them onto a visible light beam via an LED and successfully receives and reproduces the sound at a distance using a solar panel detector and power amplifiers. It serves as a practical, hands-on implementation of optical wireless communication, highlighting the potential of using light as a secure, high-bandwidth data medium.


# Components Used
**Transmitter Circuit**
1. **Power source:** 9V battery
2. **Voltage regulation:** 7805 Voltage Regulator(steps down voltage to a stable 5V DC)
3. **Audio Sources:** Microphone Module
4. **Signal Processing:** PAM8403 audio amplifier module
5. **Optical Emitter:** LED
6. **Circuit Protection:** Resistor

**Receiver Circuit**
1. **Power Source:** 9V battery
2. **Voltage Regulation:** 7805 Voltage Regulator
3. **Optical Detector:** Solar Panel(acting as a photodiode/photodetector)
4. **Signal Amplification:** PAM8403 audio amplifier
5. **Audio output:** Woofer

# How it Works
1. **Audio Capture:** Sound waves are picked up by the microphone module on the transmitter side, converting acoustic vibrations into a weak electrical analog signal.
2. **Amplification and Modulation:** The signal is processed and boosted using the PAM8403 audio amplifier. This signal is then fed into the LED(paired with resistor to regulate current), causing the light intensity to fluctuate rapidly in synchronization with the audio waveform.
3. **Wireless Transmission:** The modulated light beam travels wirelessly through open space along a line-of-sight path.
4. **Optical Detection:** The solar panel on the receiver captures the varying light intensities and convert the optical energy back into a micro-electrical element.
5. **Output Reproduction:** The weak electrical signal from the solar panel is boosted by the receiver's PAM8403 and sent directly to the woofer, successfully playing back the original audio.

# Limitations
1. **Line-of-Sight Requirement:** Because light cannot pass through opaque objects, any physical obstruction between the LED and the solar panel will interrupt the audio transmission.
2. **Range Constraints:** The operational range is limited by the brightness of the LED and the sensitivity of the solar panel, making it best suited for short-range indoor communication.
3. **Ambient Light Interference:** Strong external light sources(such as sunlight or fluorescent bulbs) can introduce noise or cause interference with the optical signal.

# Future Enhancements
1. **Digital Data Transmission:** Expand the system beyond analog audio to transmit digital data(such as text or files) using microcontroller(like Arduino or ESP32).
2. **Increased Range and Focus:** Implement laser diodes or optical lenses to extend the transmission distance and improve directional focus.
3. **Advanced Modulation Schemes:** incorporate digital modulation techniques(like OFDM or PWM) to increase data throughout and minimize ambient noise interference.
