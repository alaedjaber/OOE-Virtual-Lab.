Electromagnetic Side-Channel Attack: The Induced Leak
This project, titled "The Induced Leak," is a comprehensive research roadmap and simulation exploring electromagnetic side-channel attacks that exploit inductive coupling between parallel cables. It bridges fundamental physics with cybersecurity to demonstrate how data can be intercepted without physical contact.


🔬 Physics Foundations:
The attack mechanism is rooted in Maxwell's Equations and Faraday's Law of Induction.
    • Ampère-Maxwell Law: Current $I(t)$ flowing through a "victim" cable (e.g., Ethernet or USB) generates a varying magnetic field $\vec{B}$.
    • Faraday's Law: This varying magnetic flux induces an Electromotive Force (EMF) in a nearby "attacker" cable: 
      $$e = -M\frac{dI}{dt}$$
      Where $M$ is the Mutual Inductance between the cables.
    • Signal Reconstruction: By detecting rising and falling edges in the induced EMF, digital binary data ($0 \rightarrow 1$ or $1 \rightarrow 0$) can be reconstructed.


🛠️ Project Features:
    • Complete Attack Architecture: Covers everything from physical magnetic reception loops to protocol parsers for USB, Ethernet, and HDMI.
    • Signal Processing Pipeline: Includes stages for ADC acquisition, bandpass filtering, Z-score normalization, and Bit Error Rate (BER) calculation.
    • Original Innovations:
        ◦ Adaptive Threshold Algorithm: Uses local mean and standard deviation to detect edges in noisy environments.
        ◦ ICA Signal Separation: Mathematically separates signals when multiple cables are present.
        ◦ Metadata Analysis: Analyzes traffic patterns even when the data is encrypted.


How to Use the Simulation:
    1. Access the Live Demo: https://electromagentic-daul-channel-atack.netlify.app/
    2. Adjust Parameters:
        ◦ Distance ($d$): Observe how the signal decays as $1/r$.
        ◦ Data Rate ($f$): See why higher frequency signals (e.g., 10 Gbps) induce stronger, more vulnerable signals.
        ◦ Shielding ($S$): Test the effectiveness of EM shielding in decibels (dB).
    3. Observe Outputs: View real-time plots of the original binary signal, the induced EMF pulse, and the final reconstructed sequence.

