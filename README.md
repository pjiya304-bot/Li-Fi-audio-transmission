# Li-Fi-audio-transmission
A prototype wireless communication system that utilizes Visible Light to stream real-time audio through free space using an LED and a solar panel.

## Overview
Traditional wireless communication relies heavily on Radio Frequencies(RF), which suffer from electromagnetic interference, bandwidth congestion and security vulnerabilities. This project demonstrates an alternative approach: Li-Fi(Light Fidelity)
The system captures audio input, modulates it onto a visible light beam via an LED and receives it at a distance using solar panel detector and power amplifies. It serves as a practical, hands-on implementation of optical wireless communication, highlighting the potential of using light as a secure, high-bandwidth data medium.

## Components Used
**Transmitter Circuit**
1. **Power source:** 9V battery
2. **Voltage Regulation:** 7805 Voltage Regulator
3. **Signal Processing:** PAM8403 audio amplifier module
4. **Optical Emitter:** LED
5. **Circuit Protection:** Resistor

**Receiver Circuit**
1. **Power source:** 9V battery
2. **Voltage Regulation:** 7805 Voltage Regulator
3. **Optical Detector:** Solar Panel
4. **Signal Amplification:** PAM8403 audio amplifier
5. **Audio Output:** Woofer

# How it Works
1. Voltage: The Voltage from a 9V battery is converted to approx. 5V which is the suitable voltage for our components.
2. Audio Capture: Sound waves are picked up by the microphone module on the transmitter side, converting acoustic vibrations into a weak electrical analog signal.
3. Amplification and Modulation: The signal is processed and boosted using the PAM8403 audio amplifier. This signal is then fed into the LED(paired with a resistor to regulate current), causing the light intensity to fluctuate rapidly in synchronization with the audio waveform.
4. Wireless Transmission: The modulated light beam travels wirelessly through open space along a line-of-sight path.
5. Optical Detection: The solar panel on the receiver captures the varying light intensities and convert the optical energy back into a micro-electrical signal.
6. Output Reproduction: The weak electrical signal from the solar panel is boosted by the receiver's PAM8403 and sent to the woofer.

## Results and Observations
The system successfully demonstrated the core Li-Fi principle: audio-driven light modulation at the transmitter was detectable at the receiver through the solar panel, confirming that information was indeed being carried over the optical link.
However, the recovered output at the woofer was not clear, intelligible audio. Instead, it presented primarily as a shaking/vibrating response - indicating that while a signal was successfully recovered, it was not strong or clean enough to drive the woofer into accurate audio reproduction. This is a genuine limitation of the current prototype rather than a complete failure: it confirms the light based transmission and detection worked, while highlighting that the amplification and signal-conditioning stages need further refinement to reproduce usable audio.

## Limitation
1. Line-of-Sight Requirement: Because light cannot pass through opaque objects, any physical obstruction between the LED and the solar panel will interrupt the audio transmission.
2. Range Constraints: The operational range is limited by the brightness of the LED and the sensitivity of the solar panel, making it best suited for short-range indoor communication.
3. Ambient Light Interference: Strong external light sources(such as sunlight or fluorescent bulbs) can introduce noise or interference with the optical signal.
4. Signal Fidelity: As noted above, the recovered signal was insufficient to reproduce clear audio, likely due to insufficient gain at the receiver-side amplifier, noise introduced between the recovered signal strength and the woofer's driving requirements.

## Future Enhancements
1. Increased Range and Focus: Implement laser diodes or optical lenses to extend the transmission distance and improve directional focus.
2. Advanced Modulation Schemes: Incorporate digital modulation techniques(like OFDM or PWM) to increase data throughput and minimize ambient noise interference.
3. Improved Signal Fidelity: Investigate a dedicated amplification stage matched to the woofer's specifications or an alternative photodetector(such as photodiode) with response time to address the audio clarity issue observed in this prototype.

## Circuit Diagram


## Hardware Photos
Note: The physical hardware for this project is currently retained by the supervising faculty member as part of departmental project custody, so a photograph of the built system is not available. The circuit diagrams above illustrate the transmitter and receiver design.
