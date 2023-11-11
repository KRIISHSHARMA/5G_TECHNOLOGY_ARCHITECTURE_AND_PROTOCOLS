## NRF (network repository function)
- maintains profiles of network functions
- receives discovery request of NF
  - returns IP addresses/domain names of servers for that NF

![Screenshot from 2023-11-11 14-10-27](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/01c3db81-f7ad-4151-ba53-2a0f3bd0c208)

## NSSF (network slice selection function)
- invoked during registration
  - if need to reselect an AMF for a particular service
- NSSF returns
  - network slice
  - AMF for that service
- new to 5G 

## NEF(network exposure function)
- exposes the capabilities of 5G core network functions to an external AF
- ensures that the communications take place securely :
  - may authenticate and authorize AF throttle the rate of info transfer
- acts as middle man for info exchanged b//w 5GC and AF
- AF might notbe authorized to communicate with other NF's in 5GC 

![Screenshot from 2023-11-11 14-17-34](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/6e33a16b-4da0-4cca-8934-e153c5fc401e)
