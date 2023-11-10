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
