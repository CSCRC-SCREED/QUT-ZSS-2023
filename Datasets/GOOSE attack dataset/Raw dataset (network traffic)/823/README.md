## Scenario 823
In this scenario, the malicious program modifies original GOOSE packets every minute during normal operation. Such an attack will mislead circuit breakers with fake opening signals to disrupt the power supply. The scenario contains a total of ${\color{red}eight}$ sub-scenarios, which are combinations of ${\color{red}four}$ attack targets and ${\color{red}two}$ attack configurations.

**QUTZS.pcapng is the primary data, QUTZS_Redundant.pcapng is for redundancy purpose.**

1. **${\color{red}Four}$ attack targets**:
   - **a**: disrupting the power supply through Feeder1
   - **b**: disrupting the power supply through Feeder2
   - **c**: disrupting the power supply through Feeder3
   - **d**: disrupting the power supply through Feeder4
2. **${\color{red}Two}$ attack configurations**:
   - **8231**: altering only the allData field of 10 packets; heartbeat, stNum, and sqNum remain unchanged
   - **8232**: altering relevant fields of 10 packets, including dynamic heartbeats (1, 4, 16, 64, 256, 1000, 1000, ..., 1000ms), stNum++, sqNum reset to 0<sup>*</sup>

> <sup>*</sup> The modifications of those three fields in attack configurations **8232** are followed by practical behaviours when a true short-circuit situation occurs.

<img src="https://github.com/CSCRC-SCREED/QUT-ZSS-2023/blob/main/PrimaryPlant.jpg" alt="" width="800" height="510"/>