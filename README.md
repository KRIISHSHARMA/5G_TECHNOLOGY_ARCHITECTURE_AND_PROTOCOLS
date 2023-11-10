# 5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS

## [ACRONYMS](ACRONYMS.md)

## INTRODUCTION [module 1](INTRO.md)

## standardization of 5G 
- ITR-R (international telecommunication union - radiocommunication) responsible to develop 5G requirements
- technical specification developped by 3GPP
- 3GPP is a consortium of major telecom vendors and operators
- ITU-R requirements ==> 3GPP techincal specifications ==> vendors take specifications to develop their equipments so thier equipments can operate with one one another in harmony 
![Screenshot from 2023-11-07 19-00-53](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/047e77e4-13fe-4e48-b2eb-f4547c6ba7a0)

## 5G vision 
![Screenshot from 2023-11-07 19-12-25](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/5f796bd2-5373-4c44-98cd-2a2d810a9318)

## USE CASES 
### eMBB [peak data rate , high speed , high spectral efficiency] 
- main driver for 5G development
- apllication { 3D video , UHD video streaming etc }
- support for high speed mobility

### mMTC/mIOT [power conservation , high connection density]
- large number of connected devices
- long better life
- high connection density
- operations over long range and in challenging coverage condition 
- application { IOT , smart home/city etc }

### uRLLC [low latency , high reliability , mobility]
- E2E low latency and ultra high reliability and availability
- application { industrial automation , remote surgery , mission critical}
![Screenshot from 2023-11-07 19-30-39](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/62def002-da9b-47f1-bd5a-1a165da087d6)

![Screenshot from 2023-11-07 19-37-22](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/a64d9f7b-3f8e-47ef-97b2-4ae868b72d86)

## MOVING FROM 4G TO 5G [module 2](MOVING_FROM_4G_TO_5G.md)

## 5G architecture 
- 3 main components :
  - UE
  - NG-RAN (next gen radio access network)
    - 1. uses 5G NR technology
    - 2. based on gNB ( next gen NodeB )
  - 5GC (5G core network)
  - all ip architecture 
![Screenshot from 2023-11-08 18-09-43](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/edf37f98-4f6a-4c1b-bb61-44021185ac60)

![Screenshot from 2023-10-30 18-49-47](https://github.com/KRIISHSHARMA/5G/assets/86760658/2753b533-1b8f-49d5-9cfd-84b547e90f76)

- importance of NSA in 5G architecture : cost effective , without fullfledged 5G deployment they can still get many benefits of 5G network in NAS by using gNB , faster deployment

## KEY TECHNOLOGIES OF 5G [module 3](KEY_TECH_OF_5G.md)
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

## CLOUD RAN 
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

## MASSIVE MIMO AND BEAMFORMING [MODULE4](mMIMO_AND_BEAMFORMING.md)
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

## 5G NETWORK ARCHITECTURE[module 5](5G_NETWORK_ARCHITECTURE.md)
## 5G architecture gNB
- radio transmission/reception
- digital signal processing(encryption,data comporession)
- process access stratum signaling(siganling between UE and gNB,processed by gNB)
- relay Non-access stratum signaling to core(signaling between UE and core)
- radio resource management (gNB has to decide what resource block allocated to these UE)
- communication with core network and nearby basestations(link between two gNB's called Xn , signaling needed b//w two gNB's over Xn interface for handover)

## PDU (protocol data unit) sessions
- 5G is an all IP system(all services(voice etc.) carried over ip packets)
- 5G provides data connectivity to UE as PDU sessions
- each PDU session may consist of one or more Qos flows
- Qos characterised by
  - datarate
    - guaranteed :  voice comm requires GBR so voice doesnt get disrupted
    - non guaranteed : used for busty traffic for ex browsing the net or downloading a file 
  - latency
  - priority
  - ex voice service compared to web surfing Qos are very different , quality of voice packet has to be higher
 - each Qos flow has its own Qos ID
 - a UE at a time can establish 1 PDU session per network slice
![Screenshot from 2023-11-10 09-52-06](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/d26ad501-14b9-461a-8642-5ab819bf58e7)

## contol and user plane seperation in 5G
- control plane function
  - authentication etc
  - connection management
  - Qos management
  - mobility manaagement
- user plane functions
  - data traffic forwarding {mobility anchor , policy enforcement . lawful interception} , provides interface to intent to make sure the devices does not exceed the amount of data that the user have in their subsciption
- advantage  : scalability(increase upf or decrease cpf (eMBB) etc according to need of service)
  - more nodes to hadle data traffic
![Screenshot from 2023-11-10 10-02-52](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/52150bae-ade8-4c95-acb6-3ec9b6c6fd0d)

## 5G CORE NETWORK[module 6](5G_CORE_NETWORK.md)
## AMF 
- manages UE registration
- initiates authenttication
- mobility management
- {mobility management , registration} , responsible for supporting the device to move between different radio cells , also responsible for establishing signaling encrypted connection to the device so the device can register itself and can get authenticated and ready to acess the internet
![Screenshot from 2023-11-10 10-22-19](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/e1f0ed12-f779-43b2-94f1-d840ec031674)

## AUSF (authentication server function) 
- AMF invokes the authentication
  - passes UE identity to AUSF
- AUSF retrieves authentication vector from UDM and passes it to AMF(authentication vector generated by UDM based on the secret key which is there with the UDM , this authentication vector passed to AMF)
- AMF challenges UE with a random number(random number in authentication vector)
- (UE generates a authentication response after recieving authentication number) AUSF checks if authentication response is valid
- {security} supports AMF with authentication related function during different procedures

## SMF 
- establishes and manages PDU session
- interacts with PCF for policy decisions about Qos(PCF decides under given network condtions wheather PDU session can be established or what Qos this PDU session needs)
- UPF selection (can be more than one so have to select one while moving)
- IP address allocation
- before the device transmits the data the network needs to establish a new session , give the device an IP address and release the sesssion when device has finished its activity . AMF forwardsall session related messages to SMF

## UPF
- point of contact with data network
  - data routing
- anchor point for NG-RAN mobility
- Qos enforcement on PDU flow(PCF decides Qos => decision taken by SMF => enforcement done by UPF)
- data traffic forwarding {mobility anchor , policy enforcement . lawful interception} , provides interface to intent to make sure the devices does not exceed the amount of data that the user have in their subsciption

## UDM (unified data management)
- access authorization
  - holds security keys
- tracking AMF of UE
- subscriber information
  - data network Qos profile
  - access restrictions
  - mobility permissions
  - roaming restrictions
- user subscription data is stored in user data repository (UDR) , UDM is the frontend for the user subscription data , the AMF dosnt contain user sub data , UMF supports AMF for registration of devices

## PCF (policy charging function)
- dynamic policy descisions
  - based upon network conditions
    - congestion
    - subscriber geo-location
- eg UE in bad channel conditions wants to make a video call
  - throttle its data
  - refuse the call
- mgmt of service areas
  - list of allowed and not allowed TA's(target areas)
- can interact with AMF and SMF
- decides how a flow is charged
- session mgmt policies , non-session policies , charging devices depending on usage of device

## AF (application function)
- AF is an external server
  - communicates with core network to request a new packet flow
- eg AF can be an IMS(IP MULTIMEDIA SUBSYSTEM , used to generate voice calls over IP) node
  - requesting voice call













