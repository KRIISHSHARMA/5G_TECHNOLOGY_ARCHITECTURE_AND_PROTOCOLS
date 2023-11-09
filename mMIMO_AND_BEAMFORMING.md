## beamforming and beam steering
- large number of antennas work together to improve both coverage and also increase data rate
- terms mMIMO and beamforming are often used interchangeably

![Screenshot from 2023-11-09 22-30-13](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/8b210441-2b33-4eb6-baa3-8ee438d56aef)

- mimo technique suitable for wireless channels with rich multipath and scattering

![Screenshot from 2023-11-09 22-31-15](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/268746df-07b8-4cb3-b968-7d89cf57747c)

- in a device some antennas used for mimo and another for beamforming (not exclusive to each other)

## antenna for mmWave(above 6GHz)
![Screenshot from 2023-11-09 22-36-45](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/d2e5327b-633d-435b-94ec-9985912cfb55)

- the 30GHz patch is much reduced if we use this in basestation for receiving/transmiting this antenna will capture much less energy so to solve this probliem we combine large number of antenna in an array 

### 3D beam formming
![Screenshot from 2023-11-09 22-48-08](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/122d0f2e-44bf-4893-813f-3f88bf852ae6)

- Digital beamforming
  - adjust amplitude and phase of RF signal fed into antenna array
  - directional beam by constructive interference of EMW
  - by varying the amplitude and phase of the input of these antenna elements we can steer this beam in any direnction in 3D plane
- increasing number of antenna in array increases gain and directivity (in mmWave we can have upto 512 antennas)

### beamforming and manassive MIMO 
- mMIMO technology uses antenna array on basestation
  - typically comprising of 16,32 or 64 or more array elements
- number of antennas array elements much larger than number of UE's
-  narrower beams can be directed at different UE's
-  improve SNR
-  less interference 
![Screenshot from 2023-11-09 23-14-41](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/e3452f02-bd39-4b71-9ae8-a1965f66d901)
