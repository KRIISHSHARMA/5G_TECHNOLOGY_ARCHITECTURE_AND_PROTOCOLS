## Dual connectivity (DC)
- LTE  eNB connected to EPC
- enhanced eNB connected to 5G Core
- 5G gNB connected to 5G core
- master nodeB decides data and Qos a UE gets
- bearer splitting(some data to UE , some to another nodeB etc)  can take place at either of the nodeB's
 ![Screenshot from 2023-11-08 18-47-46](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/e313a7de-52e3-474c-9aca-67f38f7b9b14)

## small cells in 5G networks
- small cells directly related to DC
- have 5G air interface but limited coverage (10m - 2km)
- less channel impairments due to small coverage size 
- application
  - homes , stadiums , concerts and offices  to improve coverage
  - used in DC to increase user data rate
![Screenshot from 2023-11-08 18-50-34](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/31f4c3c0-4e72-447d-8e88-e4f11910f6b5)
 
## increased wireless spectrum 
- 5G NR can operate in 2 frequency ranges
  - FR1 450-6000MHZ
  - FR2 24250-52600MHz
- `Below 1 GHz` : excellent in building penetration `(great for large area cells)` , wide area coverage tens of km , limited spectrum availability 
- `1-6 GHz` : good coverage and good spectrum
- `6-100 GHZ (mmWave)` : low range (coverage inversely prop to frequency) , but a lot of bandwidth , effected by building penetration , `good for small cells` , smaller antennas (size of antennas inversely prop to frequency) , high directivity 

## OFDMA and flexible Numerology in 5G  
- 5G NR uses OFDMA as in 4G
- But 5G has a wide frequency range
- as frequency increases interfrequency interference due to doppler shift and phase error increases
- solution => use scalable carrier spacing
-  OFDM(Orthogonal Frequency Division Multiplexing) is an efficient modulation technique in which a wide frequency band is split into many small frequencies, known as subcarriers, and transmitted so that they overlap each other but do not influence other subcarriers. These subcarriers are orthogonal to each other which means the peak point of a sub-carrier occurs at the NULL point of others such that the resources can be used with maximum efficiency.
-  to overcome the problem of a symbol overlaping another , a time gap is introduced between every 2 symbols. But leaving the space empty like turning off the transmission, would cause problems for the amplifier. So, to encounter this, a CP(Cyclic Prefix) is introduced in the space.
- Cyclic Prefix is of 2 types -

  Normal CP - In Normal CP, the slot is divided into 14/7 symbols based on 
  slot configuration. The normal CP length is designed to support 
  propagation conditions with a delay spread up to 4.7 μs.

  Extended CP - The slot is divided into 12/6 OFDM symbols based on slot 
  configuration in the case of extended CP. This is intended to support 
  deployments where the delay spread is up to 16.7 μs. This is only 
  supported for the μ value 2 i.e. 60KHz SCS.



![Screenshot from 2023-11-09 09-53-01](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/a71b18fe-7509-4fec-a37c-d4c60dbdef0b)

![Screenshot from 2023-11-09 09-54-15](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/31a647a4-020f-4ab2-9248-7760e030ff10)

![Screenshot from 2023-11-09 09-55-05](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/d8107a4a-0020-4919-be12-29fd3b158b1d)

![Screenshot from 2023-11-09 09-58-24](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/216a6eda-eb84-47e2-9ab0-76628a21ebbc)

![Screenshot from 2023-11-09 10-00-40](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/213c6df5-ca0c-4dde-a71e-40c2460c9577)

![Screenshot from 2023-11-09 10-01-10](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/1d682ab6-f472-4b9c-8e30-ef0ca01098da)

- `14 OFDM symbols per slot (normal cp)`
- `12 OFDM symbols per slot  (normal cp)`

## RESOURCE BLOCK
- it is defined only for s frequency domain
- `a resource block is defined as 12 conseutive subcarriers in the frequency domain`
- LTE is defined in both freq and time domain
- resource block is only defined in freq domain cause in time domain as the scs is increased the duration of time slot is decreased
## RESOURCE ELEMENT
- smallest unit made up of
  - `one subcarrier in frequency domain and`
  - `one OFDM symbol in time domain` 
![Screenshot from 2023-11-09 19-09-59](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/8ada15e2-c3cb-46e4-ac5e-521f5294c883)

## MODULATION in 5G
- under favourible wireless channel (near base station)
  - 5G can use up to 256QAM (quadrature amplitude modulation)
  - `8 bits/symbol` {log2 (256)}
- lower modulation as the link detriorates
  - 64QAM (6bits/symbol) , 16QAM (4bits/symbol) etc

### CLOUD RAN 
- 2 main components
  - centralized unit (CU) : performs much of processing for large number of decentralizrd units
  - can be connected to multiple DU
  - typically resides in central office (edge computing)
    - handles computationally demanding tasks
      1. scheduling
      2. security
      3. power management
  - distributed unit (DU) : radio transmit/recive capability only
    - connected to one CU
    - near basestation 

![Screenshot from 2023-11-09 19-32-32](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/4511e3e4-5a58-45f8-a383-2a645482f7bb)
![Screenshot from 2023-11-09 19-34-05](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/0661b964-69f4-4cac-b972-437ee92ea4dd)
