## PDU session attributes
- PDU session establishment not a part of the 5G registration procedure
  - `UE can be registered without a PDU session`
- PDU session attributes
  - PDU session ID
  - PDU session type ( ethernet , unstructured{`used when the network does not have any knowledge of what type of protocol is being used  at the application layer `} , IPv4 , IPv6 , IPv4v6 {`IP header size increases hence not very efficient for mMMt , uRLLC , solution is to use ethernet in which we do not use IP header , we use MAC address , source and destination addresses for tranfer  of data theough PDU session `})
  - data network name ( name of data network to which this PDU session is connecting )
  - network slice type  

![Screenshot from 2023-11-17 19-03-43](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/19f9653f-bdfa-47b1-bc55-eed7aee88264)

## QoS flows in PDU sessions
- one or more QoS flows per PDU session
- each QoS flow is characterised by the QoS rule
  - QFI (QoS flow identifier)
  - QoS rule identifier
    - unique within a PDU session
  - packet filter set (to identify packets)
  - QoS parameters 

## PDU session states
![Screenshot from 2023-11-18 10-49-37](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/e02b305a-c9f3-4970-8d40-cdd74201f912)

## acive PDU session
- a PDU session consists of 3 sub-bearers
  - data radio bearer (between UE and gNB)
  - N3 tunnel (between gNB and UPF)
  - N9 tunnel (between 3 UPFs)
- bearer context
  - `DRB-ID (data radio bearer ID)`
  - `TEID (tunnel endpoint ID) `
  - `UE IP address `
- this bearer context needs to stored UPF , AMF , gNB and UE for the activaton of PDU session

![Screenshot from 2023-11-18 10-51-56](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/79636c2c-10e0-4332-b99b-cf5fd9ee1ece)

## Inactive PDU session
- 5G PDU session may necome inactive
  - inactivity timer expiration
  - done to prolong battery life
- `DRB and N3 tinnel are released`
- `any further incoming data buffered in anchor UPF`
- `bearer context retained ( in UE , AMF , UPF and gNB inorder for faster reactivation )`
- can be reactivated by UE or AMF 

## 2 main types of QoS flows 
![Screenshot from 2023-11-18 11-04-00](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/c38509b8-a5e7-4d6d-92f0-0166608d75d3)

## QoS parameters (common in both GBR and non-GBR)
- `allocation and retention priority (ARP)`
- `5G QoS identifier (5QI)`

- GRB QoS flow
 - `guaranteed flow bit rate (GFBR)`
 - `maximum flow bit rate (MFBR)`
 - notification control

- non GBR QoS flow
  - `per session aggregate maximum bit rate ( session AMBR )`
  - `per UE aggregate maximum bit rate (UE-AMBR)`
  - `reflective QoS attribute (RQA)`

## ARP (allocation and retention priority)
- competition for resources during busy period
- 5GC will use ARP to
  - establish QoS flow with higher ARP
  - reject creation of QoS flow with lower ARP
- in overload, QoS flow with a low ARP will be produced
- ARP priority
  - ARP priority: 1-15
  - pre-emption capability: yes/no (whether other QoS flows that have a lower ARP priority they can be dropped in favour of this QoS flow or not)
  - pre-emption vunerability: yes/no ( defines whether this QoS flow can be dropped in favour of other QoS flows that have a higher ARP value )
    
![Screenshot from 2023-11-22 18-59-46](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/80eea8ef-99de-4461-b9b4-50630e5a4ecb)

- `ARP parameter values for a specific subscriber are stored in the UDM`
- `from the UDM given to SMF`
- `how these parameters are gonna be used  it is defined in the general ARP policy for network and this policy is defined the PCF`
- `SMF takes input from UDM and PCF and based upon this input the SMF would decide which QoS flows it is going to create`
- `in order to create a QoS flow SMf needs to coordinate with the AMF and UPF`

## 5G , Qos identifier(5QI)
- combination of 6 parameters
  1. **Resoure type**: GBR , delay critical GBr , or non-GBR
  2. **default priority value**: lower value --> higher priority (`different from ARP , this priority level is more concerned with how UPF handles a peritcular QoS flow and what priority UPF gives to this QoS flow`)
  3. **packet delay budget(PDB)** : 98% of packets in a QoS flow must have packet delay less than PDB
  4. **Packet error rate**: maximum packet error rate that is allowed in a QoS flow (`eg 10^-2 means 1 in 100 packets can be in error`)
  5. **Default maximum data burst volume**: amount of data that is transmitted through a QoS flow in the excess network during the duration of the PDB(`valid for PDB<20 ms , if it exceeds than this parameter is no longer valid`)
  6. **averaging window**: time duration over which the parameters of  GFBR and MFBR (both GBR) are calculated (`not a parameter for non-GBR`)

![Screenshot from 2023-11-22 20-08-56](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/52b428ba-9dea-474f-b344-02b93e64c7bd)

## GBR QoS flow specific parameters 
- GFBR(guaranteed flow bit rate)
  - `the minimum data rate that the QoS flow should maintain`
- MFBR(maximum flow bit rate)
  - `the maximum data rate that the QoS flow is allowed to use`
- notification control parameters
  - `indicates if the RAN should notify the SMF when the GFBR cannot be maintained `

## Non-GBR QoS flow parameter
- session-AMBR(per session aggregate maximum bit rate)
  - ` the maximum total data rate within a particular PDU session , from all the UE's non-GBR QoS flows`
- UE-AMBR (per UE aggregate maximum bit rate)
  - `the maximum total data rate for the UE , from all of its non-GBR QoS flows`
- RQA (reflective QoS attribute)
  - whether **reflective QoS**(first have to look at packet filters to understand) is enabled for a QoS flow 

## Packet filters 
- during the establishment of PDU session packet filters are installed in the UPF in the network side and in the UE on the UE side
- once a PDU session is established we know PDU session consisits of QoS flows and these flows are then mapped to the data radio bearers
- `the function of packet filters is to identify the incoming traffic that it belongs to which PDU session then these packet filters map that traffic to their corresponding QoS flows bu marking them with QoS flow ID's`
- packet filters identify these traffics by using
  - source and destination IP addresses
  - source and destination port numbers
  - layer 4 protocol used in these traffic whether it is TCP or UDP

![Screenshot from 2023-11-22 20-38-17](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/e3b84250-6096-4b9b-b1cc-846048998330)

## 5G reflective QoS (RQoS)
- purpose of RQoS is to reduce 5G signalling
- UE uses (mirrors) the same DL(downlink) QoS rules to send UL traffic( no signalling required in order to send UL QoS rule in UE)
- during PDU session establishment the
  - UE indicates if it supports reflective QoS
  - network sets the `RQA(RQoS attributes)` for this PDU session
    - also provides `RQ timer(reflective QoS timer) `

![Screenshot from 2023-11-22 20-46-15](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/7a0dab05-c3ec-4b59-8fb0-511be4d7b5ac)

- `in order to trigger RQoS for a particular QoS flow the SMF signals to the UPf `
- UPF labels the QoS flows DL packet with
  - new QoS flow indicator (QFI)
  - UPF also sets the reflective QoS indicator in these DL packets
- UE uses this info to 
  - create an uplink QoS rule based on DL rule for this QoS flow
  - it uses the same QFI for this flow 
- UE continues to send the UL packets for this newly created QoS , as long a it continues to receive DL packets with `RQI(RQoS idicator)` bit as set
- otherwise , it waits for a time equal to the RQoS timer
  - once the timer expires the UE deletes this newly created QoS flow in the UL

