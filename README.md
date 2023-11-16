# 5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS

## [ACRONYMS](ACRONYMS.md)

## [INTRODUCTION](INTRO.md)

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

## [MOVING FROM 4G TO 5G](MOVING_FROM_4G_TO_5G.md)

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

## [KEY TECHNOLOGIES OF 5G](KEY_TECH_OF_5G.md)
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

## [MASSIVE MIMO AND BEAMFORMING](mMIMO_AND_BEAMFORMING.md)
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

## [5G NETWORK ARCHITECTURE](5G_NETWORK_ARCHITECTURE.md)
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

## [5G CORE NETWORK](5G_CORE_NETWORK.md)
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

## [NFV](NFV.md)
## network function virtualization(NFV)
- problem with traditional mobile networks
  - network nodes implemented as special purpose hardware
  - the hardware is expensive to produce install and maintain
  - the hardware eventually needs to be replaced
  - difficult for new hardware vendors to enter the market
  - difficult to upgrade the network to support new cases eg: mMTC
 
- **NFV approach**
  - networks functionalities is implemented in software
  - which runs on COTS(commercial off the shelf) hardware such as servers , storage and switches
- **NFV brings several advantages**
  - the costs of both hardware and software reduces
  - easier for new vendors to enter the market
  - far easier to upgrade the network by simply upgrading the software  

## NFV architecture by ETSI (european telecomm standard institute)
- **virtual network function** : software implementation of a network function
- **NFV infrastructure** : physical hardware resources , such as computing , storage and networking
- NFV management and orchestration encompasses the management of the
  - physial resources
  - virtual resources
  - and VNF

![Screenshot from 2023-11-10 15-56-22](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/842428b3-0785-4759-a4e1-8baabf3837d6)

- example

![Screenshot from 2023-11-10 15-58-48](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/7e676202-92c7-44fd-808a-19998b9384ff)

## advantages of NFV in 5G
- 5G is a collection of network functions
  - virtualized
  - run on a cloud infrastructure
- cost effective network based on COTS
  - no custom hardware
- ability to deploy new network functions quickly
- shared usage of resource
- scale up or scale down resources as per requirement
  - scale up AMF capacity in minutes using MANO

## 5G network slicing 
- 5G network slicing enables service providers to build virtual E2E networks tailored to application requirements
- NFV will enable network slicing
  - allows creation of multiple virtual networks on shared physical infrasturcture
- virtual networks are isolated in the control plane and user plane
- user experiences them as a physically seperate networks
- slicing crucial in 5G because of different Qos requirements for multitude of services
  - eg : low latency powerful mobile broadband
- capabilities of slice optimised for one use case
- on demand allocation of resources 
![Screenshot from 2023-11-10 17-43-25](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/4595722c-03d9-4238-a2ac-50e13de22891)

## [REMAINING FUNCTIONS](REMAINING_FUNCTIONS.md)

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

## [NETWORK IDENTIFIERS](IDENTIFIERS.md)

## 5G UE identifiers
- **PEI**(permanent equipment identity)(device identifier)
  - curently only supporeted format is IMEI
- **SUPI**(subscription permanent identifiers)(sim identifier)
   - can be either IMSI
   - NAI for non 3GPP access
- **SUCI**(subscription concealed identifiers)
  - SUPI encrypted by public key 
- **5G-S-TMSI**(5G S temporary MObile subscriber identity)
  - assigned by AMF
  - unique within AMF region
- **5G-GUTI**(5G global unique temporary identifier)
  - assigned by AMF
  - used when AMF region of UE is not known

## tracking areas in 5G 
- TA may contain min 1 cell 
- a mobile network divided into tracking areas
- tracking areas do not overlap
- in idle mode , TA of a UE is known
- in case of incoming call
  - all the UE's in the TA need to be paged with 5G-S-TMSI
  - TA update when a mobile enters a cell with different TA
- core network can assign UE specific TA's list
  - UE roams in those TA's w//o TA update 

![Screenshot from 2023-11-11 15-23-10](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/feca8b3e-9ef3-4859-bac1-29e24fc3d67c)

## 5G network identifers
- **PLMN-ID**(public land mobile network identity)
  - PLMN-ID = mobile country code (MCC)and mobile network code(MNC) 
- **AMI**( AMF identifier )
- **GUAMI**(global unique AMF identifier)
  - GUAMI = MCC,MNC,AMI
- **TAI**(tracking area identity)
  - TAI = MCC,MNC,TAC(TA code)

## [PROCEDURES_IN_5GN_NETWORK](PROCEDURES_IN_5G_NETWORK.md)

## UE power on procedure
- in the acquisition pocedure , the UE discovers nearby cells by reading their PSS and SSS (primary/secondary synchronization sequences)
- if it is a primary cell
  - then the cell broadcast system information (on PBCH) which decribes cell configuration and PLMN-ID
- if no system info
  - cell is ignored 

![Screenshot from 2023-11-11 18-21-29](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/0a0bf7e8-0a27-4f3f-abef-50fd368e5b6e)
![Screenshot from 2023-11-11 18-21-50](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/f59a0ab3-5db8-44ed-8655-5be126a47264)
![Screenshot from 2023-11-11 18-22-20](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/6b710161-e0b4-4f35-868c-2b59c76544be)
![Screenshot from 2023-11-11 18-23-09](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/c1cee187-9f8e-4198-a137-710f865934eb)

- **establish securtiy**
  - security based on process termed 5G AKA (authentication and key agreement)
  - AKA relies on the shared secret key ; the
    - USIM stores one copy
    - the UDM stores the other
  - secret key used for mutual authenticaion
    - both the device and th network authenticate one another 

  - all signalling between the device and the network encrypted
    - UE and AMF
    - UE and gNB

![Screenshot from 2023-11-11 18-27-26](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/9b0d70fc-efd2-440f-ad64-6a8e5254b605)

- **UE context installation**
  - every valid subscriber has a subscriber profile stored in UDM
  - this profile defines
    - allowed Data network connection
    - Qos
    - Bandwidth
    - roaming
    - subscriber status 

![Screenshot from 2023-11-11 18-29-47](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/c3f88258-eeb5-40ec-ab7c-d230ac845e2f)

- **UE Policy check**
 - AMF performs a policy cjeck with the PCF
 - policy decisions influenced by
   - the time of day
   - location of the user
   - network congestion etc
  - policy check necessary
    - if subscriber can acess the network in these connection

![Screenshot from 2023-11-11 18-32-05](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/9673eb13-7790-43a2-9406-630f5ccbb13f)

- **5G-S-TMSI allocation**
  - finally temporary ID allocated to the subscriber
  - this 5G-S-TMSI is created by the AMF
  - used for until the device isallocated
    - potentially due to an AMF change 

![Screenshot from 2023-11-11 18-34-59](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/e8abba56-db60-4605-a600-0bbf92499128)

## UE idle and connected modes
- **idle mode**
  - UE location known to TA level(doesnt know exactly which cell)
  - UE is  camping on a cell
  - UE listens to paging(whenever there is an incomig call for this device , the network will page all the mobile in TA in which mobile is located)
  - UE paged using 5G-S-TMSI(the paging message will contain the TMSI of the device , device will respond to the network and the network will know the current cell of the device)

- **connected mode**
 - UE is actively exchanging voice or data with network
 - 5G-S-TMSI used for communication
 - UE location known to cell level

## PDU session establishment
- once the mobile has registered itself to the network then wants to avail some data service of network , this device will generate PDU session establishment request
- then AMF will notify SMF to perform policy check for this request
- PCF will then do a policy check
- PCF will determine whether the device can use the services or not
- if the check is positive the SMF will coordinates with AMF and UPF to establish user data PDU session 

![Screenshot from 2023-11-11 20-36-46](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/014d7405-c715-4574-aa14-7914d9a9563d)

## UE paging procedure 
![Screenshot from 2023-11-11 20-39-12](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/d9b60c50-7656-4cb3-82d9-54967d3897ba)

- this paging message will contain TMSI of the mobile whose call is incoming , this device will message and respond to this message after which
PDU session can be established for the downlink transfer of this data 

## tracking area update procedure

![Screenshot from 2023-11-11 20-43-59](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/8786ea12-eb04-4889-bccb-a74c792da282)

## handovers in 5G 
- handovers always take place when
  - UE is in a connected state during a call
- the network decides a device switched from one cell to the next
- two mechanisms of handover in 5G
  - Xn handover
  - N2 handover

## Xn handover
1. handover coordinattion : security info, PDU session info
2. device connected to new cell
3. AMF request to switch PDU session
4. AMF will then request SMF to generate this switch
5. SMF will ask UPF to change from souce gNB to target gNB 
6. new PDU session path established 

![Screenshot from 2023-11-11 20-49-16](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/293eb5e3-c6c7-43fa-b85d-7fcb052ec0a2)

## N2 handover ( no connection between source and target gNB directly only using AMF{AMF acts as middleman})
1. AMF starts handover coordination
2. device connected to new cell
3. AMF request to switch PDU session
4. AMF will then request SMF to generate this switch
5. SMF will ask UPF to change from souce gNB to target gNB 
6. new PDU session path established 

![Screenshot from 2023-11-11 20-54-32](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/b4c4cbe7-b376-4753-a6ef-ef310fe30127)

## [SERVICE_BASED_ARCHITECTURE](SERVICE_BASED_ARCHITECTURE.md)

## 5G sevice based architecture
- service based arch introduced to increase modularity
- a NETWORK FUNCTION provides one or more servicrs to other network functions in the network
- these services are made available over service based interfaces of network funtion interface 

![Screenshot from 2023-11-12 15-35-29](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/63471c27-926b-448f-856c-562a131ba2a6)

## main mechanisms for NF services
- request-reponse :
  - NF service consumer requests a service
  - NF service provider returns
    - information to the consumer
    - or performs an action , or both
  - subscribe-notify :
    - NF service consumer subscribes to provide service
    - provider notifies the consumer about
      - the occurrence of events or
      - periodic updates related to the service

![Screenshot from 2023-11-12 15-40-20](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/fbbdb362-b506-4166-a5c4-82aa42922d57)

## HTTP/2 for 5G core network
- HTTP/2 used for communication between NF's
- easy deployment in cloud environment
- HTTP/2 is already very widely deployed
  - well developed security mechanisms , third party applications
- easy integration of operatorand third-party applications

##  HTTP/2 on web vs HTTP/2 in 5G Core

![Screenshot from 2023-11-12 15-48-29](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/3889102b-d218-4ddc-829c-fe36d56a5522)

- in 5G core request-response data only in JSON format 

## JSON format
``` bash
{
     "empid":"SRAETS",  #name-value pair
     "personal":{
           "name":"smithjones",
           "gender":"male",
           "age":23,
           "address" :
     {
            "streetadd":A"efaeaegaegE",
            "city":"afae",
      }
  }
      "profile":{
           "designation":"aefaef".
          }
}
```

## concept of resource
- exmaple of reources
  - PDU session
    - context
    -   QoS policy
 - NF registration with NRF
- resources located and manipulated as URI(uniform resouce identifier)

![Screenshot from 2023-11-12 16-01-22](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/4948437d-e7d0-45a6-9a11-a5cff4b735f0)

## HTTP methods used in 5GC 
![Screenshot from 2023-11-12 16-03-08](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/504d08a0-cf68-4f68-8b6f-68b9b20a70b5)

## HTTP reponses in 5G 
![Screenshot from 2023-11-12 16-04-58](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/08e72f74-2f77-4ebf-9a09-e1e1d0368d35)

## naming scheme for NF services
![Screenshot from 2023-11-12 16-16-38](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/5f2e6393-30b6-4b78-8231-76f5f82e8ee1)

## REST applied to 5G sevices
- defines a set rules for design of distributed applications
- the 5GC service API implemented according to the REST "paradigm"
- in the context of 5GC rules of REST applied to HTTP protocol

## principles of RESTful design
- client/server : split of responsibilities between client and server
- stateless : each request from client must contain all the info necessary to understand the request
  - session state is therefore kept entireely on the client
- cacheable : clients get indication from servers whether the received information can be cached at client
- uniform interface : identification and manipulation of resources through URI's
- layered system : each component cannot "see" beyond the immediate layer with which they are interacting 

## Use case 1 : NF service registration
![Screenshot from 2023-11-12 16-30-30](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/bff18d36-8476-499f-af52-dfe2a33b4d24)
![Screenshot from 2023-11-12 16-31-37](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/8d0dcc72-3788-41ee-b337-b4f3fb9f3b31)
![Screenshot from 2023-11-12 16-34-17](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/30c75dc0-dcb1-40e6-b09f-9061beb0b636)

## Use case 2 : NF sevice discovery 
![Screenshot from 2023-11-12 16-37-36](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/7a18607f-7105-42c4-b5b9-6d7161268986)

## [ESSENTIALS_OF_NETWORK_SLICING](ESSENTIALS_OF_NETWORK_SLICING.md)

## What is network slicing ?
- network slice is a logical network serving a defined customer consisting of all required network resources configured together 
 - complete network within a provider
 - resources optimized for one use case
 - isolated but may share resoures
 - user experience it is as a seperate network
 - on demand allocation of resources 

![Screenshot from 2023-11-13 20-54-13](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/72995930-ecbc-41ae-95fc-b42686c2f508)

## example of network slicing in 5G 

- slices using same AMF 
![Screenshot from 2023-11-13 20-54-13](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/aaebe01b-0311-4b8e-8b7d-dc192bbfd85a)

## S-NSSAI (single network slice selection assistance information)
- a `network slice instance` (NSI) is identified by S-NSSAI

![Screenshot from 2023-11-13 21-02-54](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/363d1994-8721-48da-99f3-68438e299474)
 - SD is optional
 - used to differentiate between different network slices used for different customers

![Screenshot from 2023-11-13 21-05-29](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/d8e113a3-94cc-40a3-bdf0-b49216e202d8)

- SST : can be 1,2,3,4,5-127,128-255
- SD :  example there are two different eMBB slices that are allocated to two different users SD differentiates between these two eMBB using SD part 

## NSSI (network slice subnet instance in 5G)
- NSI is further composed of NSSI

![Screenshot from 2023-11-13 21-11-49](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/3a0ce16a-ad8f-4a29-aa5d-e27fc3a24c58)

- A NSI is composed of one ore multiple network slice subnet instances (NSSIs)
- A NSSI may contain one or multiple virtualized network functions
- A NSSI may
  - consist NF(s) and other NSSI(s)
  - be shared by 2 or more NSIs
  - may contain core network functions or Access network functions or both 

## multiple slices support
- at one time , `maximum 8 slies` can be assigned to a single UE
  - this UE must support PDU sessions associated with these slices
- a common AMF instance supports all slices assigned to a UE
  - but these slices can have separate SMF/UPF instances
- a PDU session is assoiated with only one S-NSSAI and one DN(data betwork)

## NSI (network slice instance) life cycle
1. preparation  : decide what are the resources that are required for this network slice
2. instantaion configration and activation phase : assign all necessity resources for this network slice(NS), config this NS , activate this NF
3. run time : network slice is run
4. decommision : deactivate and release all resources that were given to this network slice

 - `NSMF ( network slice management function oversees the respective tasks of each phase` 

![Screenshot from 2023-11-13 21-27-08](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/2cdc744a-643d-4a20-a92b-1a983a5175fc)

## 1. preparation phase
- network slice "blueprint" or "template" lists necessary attributes of network slice
- if an existing network slice template meets the customer requirements
  - this template can be used as it is
  - or it can be scaled to meet customer requirements
- in this case the preparation phase can be excluded

![Screenshot from 2023-11-13 21-29-54](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/20396ca0-b147-40c1-96b1-07b40e51e77a)

- if no suitable network slice template
  - new one is designed using the customer requirements
- newly designed template can be added to a catalogue of network slice tmeplates
- so preparation phase is skipped/shortened for the next customer with similar requirements 

![Screenshot from 2023-11-13 21-31-51](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/23f792a0-46e4-4028-a244-649b4afebbd4)

## 2. instantiation , configuration and activation phase
- all resources shared/dedicated required by a NSI are created (instantiated) and configured
- actions to make NSI active , eg diverting traffic to it provisioning databases 

![Screenshot from 2023-11-13 21-35-12](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/ab5c8068-b639-46ba-95ab-c9f81f2c51d9)

## 3. run time phase
- NSI is capable of traffic handling
- performance monitoring using `key performance indicators (KPI) reporting`
- supervision : NSI may need to be modified
  - NSI reconfiguration , NSI capacity change , NSI topology change (how NFs are connected to one another), addition/deletion of NF's

![Screenshot from 2023-11-13 21-39-45](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/937d25fa-f512-42bd-aeaa-ac2643b7b0ad)

## 4. decommissioning phase
- the decommissioning phase includes deactivation
- the dedicated resources (eg NFs) assigned to this NSI are free
- shared/dependent resources are reconfigured
- after decommissioning the NSI does not exist anymore

![Screenshot from 2023-11-13 21-43-13](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/da0b942b-2cff-46c8-a175-3b1bccd48e26)

## network slicing management model 

![Screenshot from 2023-11-13 21-46-14](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/9c4d2845-7ca8-4ae2-8b8e-8fd7f492e3e2)

- CSMF (comm service management function) converts the customer requirements to the network slice related requirements
  - network type
  - network capacity
  - QoS requirements etc  

- CSMF provides network slice requirements to NSMF
- NSMF (network slice management function) manages the network slice instance
- NSMF converts the network slice related requirements to network slice subnet related requirements  

- the NSSMF manages the NSSIs based on the network slice subnet related requirements received from the NSMF

## radio access network slicing 
![Screenshot from 2023-11-13 21-52-54](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/de2fe869-6508-437b-be7c-00c17b942dbf)

## slice avaiability in the 5G network 
- `network slice selection assistance information (NSSAI)` is a set of S-NSSAIs
- NSSAIs are managed at the
  - TA level in the 5G RAN
  - registration area level in 5GC
- a given registration area (ie the list of tracking areas) shall support common set of slices 

## signaling related to slice availability 

![Screenshot from 2023-11-13 22-02-47](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/a832101f-932f-4cd9-bb49-24a30b2e3a33)

- using OMC(operations and managment center) ,the operator configures
  - the NSSF about where network slices are available in a 5G PLMN
  - the 5G gNBs about netwok slice availablity per TA level

![Screenshot from 2023-11-13 22-04-32](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/0e02b09b-f19c-41f4-af77-1e7bf3777c8e)

- **over N2 interface** : during N2, connection setup/updation during RAN/AMF configuration update :
  - gNB --> AMF about S-NSSAIs supported per TS
  - AMF --> gNB about S-NSSAIs per PLMN ID supported by AMF
  - **over Xn interface** : at Xn setup and 5G RAN node configuration update
    - gNBs exchange S-NSSAIs per TA
  
![Screenshot from 2023-11-13 22-08-32](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/e10ea398-30b4-4a75-b771-43e2c3d9188f)

- **over N22 interface** : a setup or change
  - AMF-->NSSF about S-NSSAIs per TA
  - NSSF-->AMF about restricted S-NSSAIs per TA

![Screenshot from 2023-11-13 22-10-28](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/3efcf61b-5a7e-48ff-9824-f9ddcf351a77)

## NSSF (network slice selecion function)
- provides services to other AMF and NSSFs

![Screenshot from 2023-11-13 22-12-39](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/9924f520-a08e-40d7-b5f5-454fc4e92c48)


## [SECURITY_IN_5G](SECURITY_IN_5G.md)

## 5G roaming architecture
![Screenshot from 2023-11-14 11-02-51](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/8af9470b-0f67-4018-8d37-d4e698b7123d)

- visiting UPF controlled by visting UPF , HOME UPF controlled SMF

## logical entities for network access security
- seperate logical entities for security defined to maintain a logical security architecture
- contaibed within 5GC NFs
- logical entities
  - ARPF (AUTHENTICATION CREDENTIAL REPOSITORY AND PROCESSING FUNCTION)
  - AUSF (AUTHENTICATION SERVER FUNCTION)
  - SEAF (SECURITY ANCHOR FUNCTION)
  - SIDF (SUBSCRIPTION IDENTIFIER DE-CONCEALING FUNCTION)

![Screenshot from 2023-11-14 11-09-06](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/6e850ea2-b4f4-416a-9e30-be6955aacc0c)

## SIDF(subscription identifier de-concealing funtion)
- the SIDF is a service offered by the UDM NF in the home network
- it is responsible for resolving the SUPI from the SUCI
- responsible to deconceal SUCI 

## AUSF(authentication server function)
- defined as a standalone NF in the 5GC architecture
- responsible for handling the authentication in the home network
  - based on information received from the UE and UDM/ARPF

## SEAF(seurity anchor function)
- it is functionality provided by the AMF
- responsible for handling the authentication in te serving(visited) network
  - based on info received from UE and AUSF
- `called a seruity anchor cause UE cannot directly communicate with the AUSF or AMF for its authentication`

## ARPF (AUTHENTICATION CREDENTIAL REPOSITORY AND PROCESSING FUNCTION)
- important
- ARPF contains the subscirbers security credentials
   - long-term/master key (K) 
     - uses of master key:authentication , derivation of ciphering and integrity protection keys
    - the subscription identifier SUPI
- ARPF services are provided via the UDM
   - no open interface defined between UDM and ARPF 

## network access securtiy 
- it comprises of all those functions that are related to the secure access of this UE to the network
- mutual authentication
  - UE and network confirm each other's identities 

![Screenshot from 2023-11-14 11-28-36](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/207a583c-1c9a-46f9-bb6b-1fb353417140)

- UE and network must support 2 authentication methods :
  - `5G AKA (5G autentication and key agreement)`
    - for 3GPP access (UE<==>gNB)
  - `EAP-AKA (extensivle authentication protocol - AKA)`
    - for non 3GPP access (WLAN device connected to WLAN access network)

- one the authentication procedure is complete the ciphering and integrity protection keys are generated (ex UE when connected to AMF)
- exceptions - emergency calls

## initiation of authentication
![Screenshot from 2023-11-14 16-54-51](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/2fda3f4e-b3be-49d1-9bf5-7811f4ede1f9)

- based on SUPI , ARPF which type of authentication to be used (AKA or EKA-AKA)

## concealement/deconcealement of SUPI 
- 5G-GUTI is sent if the UE has a valid 5G-GUTI from a previous registration
- if 5G-GUTI not available, SUPI needs to be used
- SUPI is never sent in clear text over the air
- a concealed version of SUPI called SUCI is used 

- SUCI is created by the UE based on publi key cryptography and a protection scheme
- `the HPLMN (UDM/SIDF) can derive the SUPI from the SUCI by using the home network private key` 

![Screenshot from 2023-11-14 17-04-28](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/40a61871-9cf9-4d19-aa9b-5a0dd596989a)

- MSIN (mobile subscriber identification number) is encrypted using home network public key 

## 5G AKA procedre 
![Screenshot from 2023-11-14 17-15-55](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/9835d5d3-cfed-400e-bd67-62e228b5fe06)

- once the authentication procedure has been initiated then UDM has the SUPI and based on the SUPI , UDM decides whether it has to use 5G AKA procedure or EAP-AKA procedure(we are looking at AKA)
- the ARPF generates the 5G home environment authentication vector cause (AUSF and UDM are in hone network)
- the expected response to the random number(XRES) is calculated using the MILENAGE FUNCTION and the input to the milenage function are sequence number , random number , Authentication manaegement field and the master key (K)
-  this milenage function has 5 subfunctions :- `MAC(generates message authentication code)` , XRES(response to random number) , IK , AK

![Screenshot from 2023-11-14 17-19-30](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/cb0f8115-0224-4812-9db3-d8f82ffde458)

- UDM derives XRES* as follows using HMAC-SHA-256 KDF function

![Screenshot from 2023-11-14 17-23-22](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/d575c440-f60f-4a19-b030-eb33b20293f7)

- UDM derives K_AUSF as follows using HMAC-SHA-256(K,S) `KDF(key derivation function)` as below 

![Screenshot from 2023-11-14 17-25-37](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/0e331afc-0f54-4ce0-86f9-451cd643bb51)

- AUSF derives K_SEAF from K_AUSF by passing K=K_AUSF and S= 0x6C || serving network name || length of serving network name to KDF function
- this K_SEAF for the time being is stored in the AUSF 

![Screenshot from 2023-11-14 17-27-52](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/60437617-72c2-4918-833d-b002802d7db9)

- AUSF uses the XRES* to calculate the HXRES*
- HXRES* calculation at AUSF : HXRES* is 128bit MSB of the output of SHA-256 hash, calculated by passing RAND||XRES* as input to SHA-256 algorithm 

![Screenshot from 2023-11-14 17-30-35](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/65a20eaa-302c-41c4-b129-7f8a0b9a4d9e)

- AUSF sends the 5G SE AV (serving environment authentication vector) to the AMF (SE cause AMF is located in the serving network of the UE)
- SEAF(AMF) stores the HXRES* and send random number (RAND) and authentication token (AUTN) tothe ME (mobile equipment) which send it to USIM

- USIM verifies the AUTN and derives the RES and keys(CK,IK)

- UE uses milenage function to derive XMAC , RES , CK , IK as below

![Screenshot from 2023-11-14 17-36-38](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/bef02ddb-037a-4dbb-8e5f-39a2c0260696)

- if the XMAC and MAC are the same then it means its the genuine mobie network that this UE is connecting
- also verifies that sequence number(SQN) is in the correct range

- CK and IK are sent to ME and it calculates RES* and derive Kausf key , Kmac key , Kamf key
- then ME send RES* and MAC to the AMF(SEAF)

- SEAF(AMF) calculates the HRES* from RES* and compares it with HXRES* from the HXRES* it hase already stored if they are the same it means it is good
- AUSF compares RES* with XRES* (AUSF stores XRES*) if it is the same then authentication is successful 

## 5G security key hierarchy 
![Screenshot from 2023-11-14 18-17-09](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/d8a2a73e-f6c0-44bc-b451-c7113afd2e18)

- K<sub>NASint</sub> used for integrity protection of the link that is there between AMF and UE
- K<sub>gNB</sub> handed over to gNB from AMF used to derive the following
  -  K<sub>RRCint</sub> signaling between UE and gNB is called RRC k K<sub>RRCint</sub> does integrirty protection
  -  K<sub>RRCenc</sub> encryption of RRC
  -  K<sub>UPint</sub> integrity protection of data that is flowing from UE to gNB
  -  K<sub>RRCint</sub> encryption of the flowing data  

- `the AMF passes K_gNB to the master eNB/gNB`
  - `stored there till the UE is in the state of CM-CONNECTED`
- `the encryption and integrity keys are 256 bits long`
  - `but are truncated to 128 bits before use , future provision 256 bits`
- `ciphering/integrity keys called as low level keys as these keys are used just between OSI layer 1(physical layer) and layer 2(data link layer) `

## ciphering/integrity algo in 5G 
![Screenshot from 2023-11-14 18-34-22](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/41340453-dc58-4f99-9602-0ada7ebbd62a)

## 5G EAP-AKA for non-3GPP access architecture 
- used for authentication of non-3GPP devices if they want to connect to 5GCN 

![Screenshot from 2023-11-14 18-37-19](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/6495d156-a4af-42ec-b13d-de23ab74360d)

- instead of UE directly connecting to AMF it first connects to access point for WLAN  
- In order to connect to 5GC will need protocol converison which is provided by `N3IWWF`(non-3GPP access interworking function)

## 5G EAP-AKA(extensible authentication protocol - authentication and key agreement)
- defiend by IETF in RFC 3748 is a protocol framework for
  - authentication
  - typically between an end-user device and a network
- first introduced for the point to point (PPP)
- EAP is not an authentication method per se but rather
  - `a common authentication framework to impelement specific authentication methods`
- `EAP is therefore "extensible" as it enables support for different authentication methods`
- new authentication methods can be added
- these authentication methods are typically referred as EAP methods 

## 5G EAP-AKA' (subtype of 5G EAP-AKA)
- it is for performing authentication based on USIM cards
- UDM/ARPF will generate a transformed `authentication vector(AV')` and provide it ti the AUSF
- the AV' consists of 5 parameters
  - RAND (random number)
  - XRES (expected result)
  - AUTN (network authentication token)
  - CK' and IK' (keys)

![Screenshot from 2023-11-14 18-57-08](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/61e045d3-4bbf-4e76-b9f3-b060dba3c3cf)

- UDM generate AV'(RAND,XRES,AUTN,CK',IK') which is given to AUSF
- AUSF will keep XRES,CK'and IK' within itself and calculate the MAC(message authentication code) , generate K<sub>AUSF</sub> and from this will generate K<sub>SEAF</sub> and will keep  K<sub>SEAF</sub> in itself and forward RAND,AUTN,MAC to AMF
-  AMF will challenge the ME using RAND,MAC,AUTN , ME will kepp MAC and forward RAND , AUTN to USIM
-  USIM verifies the AUTN and derives the RES and keys(CK,IK) and forward it  to ME
-  ME/UE verifes the MAC and derives  K<sub>SEAF</sub>, K<sub>AUSF</sub>, K<sub>AMF</sub>
-  UE sends response to the challenge with RES , MAC '
-  AMF then forwards the RES , AC to AUSF (*AMF just forwarding messages not calculating any hashes or doing any comparison*)
-  AUSF compares RES with XRES and checks if ir is valid response if the value is correct it means its good , it also verifies MAC and finds them correct
-  AUSF then sends  K<sub>SEAF</sub> to the AMF and AMF will then derive the  K<sub>AMF</sub> based on  K<sub>SEAF</sub> and will keep  K<sub>AMF</sub> with itself
-  AMF then informs the UE that authenticaion was a success 

## 5G security key hierarchy for EAP-AKA (non-3GPP Access)

![Screenshot from 2023-11-14 19-26-02](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/0e1dcc7e-0ca8-470b-a548-58e5ffcf69a2)

## [VOICE_OVER_5G](

## intro
- 5G voice service will be provided based in `IMS (IP multimedia subsystem)`
- IMS was launched with 3G as voice over IP solution
  - used in VoLTE calls
  - 2G,3G used ckt switching 
- 2 major voice solutions in 5G
  1. voice over 5GS
  2. EPS fallback: if 5G coverage not available(handed over to LTE system)
- VoLTE supports
  - SRVCC (single radio voice call continuity)
    - active VoLTE call handed over to 2G/3G voice if no 4G coverage
  - CSFB (ckt switched fallback)
    - call is handed to 2G/3G before te call is connected
- with 5G core , no SRVCC or CSFB capability
  - ckt switched voice option lost 



































































































