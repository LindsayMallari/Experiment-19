# Experiment 19: Direct Sequence Spread Spectrum (DSSS) Modulation and Demodulation

## Objectives
- Generate a DSSS signal by spreading a message with a PN sequence.  
- Observe similarities between DSSS and DSBSC modulation.  
- Recover the message using a synchronized product detector.  
- Study effects of incorrect PN synchronization.  
- Examine interference rejection capability of DSSS.

## Materials
- **Trainer:** Emona Telecoms-Trainer 101 + power-pack  
- **Oscilloscope:** Dual-channel 20MHz  
- **Modules:** Master Signals, Sequence Generator, Multipliers, Adder, Tuneable LPF, Speech Module, VCO  
- **Leads:** Oscilloscope and patch leads  

## Background
DSSS multiplies the message signal by a high-frequency Pseudo-Noise (PN) sequence, spreading its energy across a wide bandwidth. This reduces power density, making the signal appear noise-like. Recovery requires a receiver with an identical, synchronized PN sequence. Mismatched sequences yield noise, while DSSS offers interference resistance and security.

## Procedure
### Generating DSSS Signal
1. Connect a 2kHz sine message to a Multiplier input and PN sequence to the other input.  
2. Observe the DSSS signal alongside the original message on the oscilloscope.  
3. Replace the sine wave with the Speech Module output to generate a DSSS speech signal.  

### Recovering the Message
4. Feed the DSSS signal to a second Multiplier with the same PN sequence.  
5. Connect output to a Tuneable LPF to recover the message.  
6. Replace the receiver PN sequence with a different sequence and observe noise at the output.  

### Testing Interference Rejection
7. Add a VCO narrowband signal as a jammer via an Adder.  
8. Observe the combined signal and pass it through the product detector + LPF.  
9. Note that the message is recovered despite jamming.

## Observations
- Multiplier output resembles a DSBSC signal modulated by the PN sequence.  
- Correct PN synchronization recovers the original message; incorrect PN produces noise.  
- DSSS despreading rejects narrowband interference, demonstrating processing gain.  

## Q&A
- **DSBSC similarity:** PN transitions invert the signal, envelope follows message.  
- **Noise-like appearance:** Time-domain view exaggerates; real signal spreads power over wide bandwidth.  
- **No output when silent:** 0 × PN = 0.  
- **LPF output with correct PN:** Resembles original message.  
- **Wrong PN sequence:** Fails to despread, output appears as noise.  
- **Jamming effect:** Despreading restores message while rejecting interference.

## Summary
DSSS spreads a message using a high-speed PN sequence, producing a noise-like, wideband signal. Recovery requires a synchronized PN sequence. The experiment demonstrated DSSS’s robustness against interference, highlighting its advantages in secure and reliable wireless communications.
