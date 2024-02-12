## Scenario 842
In this scenario, the malicious program modifies original GOOSE packets when a short-circuit fault happens. Such an attack will mislead circuit breakers with fake closing signals to disable safety protection. The scenario contains a total of ${\color{red}four}$ sub-scenarios, which are combinations of ${\color{red}two}$ attack targets and ${\color{red}two}$ attack configurations.

**QUTZS_GOOSE.csv extracts all GOOSE features of all GOOSE packets from the raw network traffic**

**QUTZS_SV.csv extracts all SV features of all SV packets from the raw network traffic**

**QUTZS_final.csv merges both GOOSE and SV features based on packet recieve timestamp, and most importantly labels each merged sample based on 55 types of behaviours**

1. **${\color{red}Two}$ attack targets**: 
   - **a**: disabling the safety protection when a short-circuit fault happens in Fault_22bus1
   - **b**: disabling the safety protection when a short-circuit fault happens in Fault_22bus2
2. **${\color{red}Two}$ attack configurations**:
   - **8421**: altering only the allData field of all packets when a short-circuit fault happens<sup>*</sup>
   - **8422**: altering only the allData field of the first 30 packets when a short-circuit fault happens

> <sup>*</sup> In practice, the *dynamic heartbeats*, *stNum++*, *reseting sqNum to 0* will happen either when a true short-circuit fault occurs or when power systems are recovered from a true short-circuit fault. Thus, to fake a recovery situation when a true short-circuit fault occurs, it is unnecessary to modify those three fields.

<img src="https://github.com/CSCRC-SCREED/QUT-ZSS-2023/blob/main/PrimaryPlant.jpg" alt="" width="800" height="510" />