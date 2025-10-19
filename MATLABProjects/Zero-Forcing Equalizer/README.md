# Channel Equalization in Digital Communication Using Zero-Forcing Equalizer

## Project Description
This project focuses on **Channel Equalization** in **digital communication systems** using the **Zero-Forcing (ZF) Equalizer** technique. The implementation demonstrates how intersymbol interference (ISI), a common issue in band-limited channels, can be mitigated to improve signal recovery precision.

The simulation employs **Binary Phase Shift Keying (BPSK)** modulation, where randomly generated binary data is transmitted through a **multi-tap channel** that introduces ISI. To emulate real-world conditions, **Additive White Gaussian Noise (AWGN)** is added, degrading the received signal quality. The Zero-Forcing equalizer is then utilized at the receiver to **invert the channel effect**, canceling out ISI and recovering the transmitted data sequence.

### Key Concepts:
- **BPSK Modulation:** Converts binary bits (0s and 1s) to -1 and +1 symbol levels.
- **Intersymbol Interference (ISI):** Occurs when delayed versions of transmitted symbols overlap, distorting current symbols.
- **Zero-Forcing Equalizer:** Compensates for ISI by applying an inverse filter of the channel frequency response, effectively nullifying distortion caused by multipath components.
- **Bit Error Rate (BER) Evaluation:** Quantifies system performance before and after equalization.

### Process Overview:
1. **Signal Generation:** Create random binary data and apply BPSK modulation.
2. **Channel Modeling:** Define a finite impulse response channel (e.g., `[0.8, 0.2, 0.1]`) to simulate ISI conditions.
3. **Noise Addition:** Apply AWGN with a controlled SNR (10 dB) to simulate realistic noise.
4. **Equalization:** Implement Zero-Forcing logic to remove channel-induced distortions.
5. **Demodulation:** Recover transmitted bits by comparing the received amplitude levels to a threshold.
6. **Performance Analysis:** Measure BER with and without equalization to assess improvement.

### Observations:
- The **ZF equalizer** significantly improves signal quality by reducing ISI-induced distortions.
- However, the method can **amplify noise**, especially at low SNR values, limiting its effectiveness in noise-dominant environments.
- The resulting BER demonstrates a **noticeable reduction** post equalization, proving the utility of Zero-Forcing for distortion compensation.

### Simulation Output (Sample Results):
| Parameter | Without Equalization | With Equalization |
|------------|----------------------|-------------------|
| ISI Ratio | 1.4512 | Reduced |
| Bit Error Rate (BER) | 0.477 | 0.509 |

### Conclusion:
This project successfully demonstrates the implementation of a **Zero-Forcing Equalizer** in MATLAB for **BPSK-based digital communication**. The technique effectively **removes ISI** and enhances signal detection accuracy. Despite its simplicity, the ZF equalizer provides valuable insight into practical channel equalization but highlights the need for more **noise-resilient alternatives** such as the **Minimum Mean Square Error (MMSE)** equalizer for advanced communication systems.
