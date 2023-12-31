# QUT Zone Substation Security Datasets (2023)

## Background
Zone Substations are used to transform sub-transmission voltages (typically 34.5 kV to 69 kV) to high-voltage distribution voltages (typically 11 kV to 22 kV) and to act as controlling points between different high-voltage networks. The figure below illustrates the overall architecture and process of common power girds.

<img src="PowerGrids.jpg" alt="" width="600" height="552" />

**Retrieved and edited from https://www.copper.org/environment/sustainable-energy/grid-infrastructure/**

The datasets were generated and collected from a software-based simulation testbed. The testbed simulates a small-scale smart zone substation, including the primary plant (physical process), the control devices (Intelligent electronic devices or IEDs), and the process bus communication networks. The figure below demonstrates the testbed architecture.

<img src="Testbed design.jpg" alt="" width="800" height="553" />

The datasets contain a wide variety of network and physical behaviours in an IEC-61850-compliant zone substation. The datasets are compatible with actual substation network traffic, including both Generic Object-Oriented Substation Event (GOOSE) and Sampled Value (SV) network packets. 

Generally, there are two different types of benign behaviours in substation operation: 1) fault-free operation when no unusual events happen; and 2) emergency operation when nonmalicious events (e.g., short-circuit faults) happen. Attacks can occur during both kinds of benign behaviours, which introduce two types of malicious behaviours: 3) attacks under faultfree operation to disrupt energy transmission, and 4) attacks under emergency operation to block protection mechanisms or trigger unnecessary protection measures.

All attack scenarios in our datasets are false data injection (FDI) attacks and replay attacks. We implemented all three forms of FDI attacks targeting both GOOSE and SV c including 1) deletion of data from the original message; 2) modification of data in the original message, and 3) addition of fake data or fake messages.
