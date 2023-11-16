## intro
- 5G voice service will be provided based in `IMS (IP multimedia subsystem)`
- IMS was launched with 3G as voice over IP solution
  - used in VoLTE calls
  - 2G,3G used ckt switching 
- 2 major voice solutions in 5G
  1. voice over 5GS
  2. EPS fallback: if 5G coverage not available(handed over to LTE system)
- VoLTE supports
  - `SRVCC (single radio voice call continuity)`
    - active VoLTE call handed over to 2G/3G voice if no 4G coverage
  - `CSFB (ckt switched fallback)`
    - call is handed to 2G/3G before te call is connected
- with 5G core , no SRVCC or CSFB capability
  - ckt switched voice option lost 

## Vo5G Codecs
- codec is an algorithm that digitalizes and compresses the voice in the transmitter and decompresses the voice at the reciver end and gives it an analog wave form shape so that it can be heard by the person who is recieving this voice
- Vo5G must support 2 codecs
  1. `EVS (enhanced voice services)`
     - norrow band to wideband HD voice (128 Kbps)
     - backward compatible WB-AMR(LTE)
     - robustness to delay jitter and packet loss
  2. `IVAS (immersive voice and audio service)`
     - mono to stereo to fully immersive for VR
     - underdevelopement 

![Screenshot from 2023-11-16 11-40-43](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/177ce6e0-3d13-41a0-86f7-43a59ffe01ca)

- whether the voice is encoded using EVS or IVAS , this voice is carried in `RTP packets (real time protocol)` , these RTP packets are then carried to `UDP packets (user datagram protocol)` in the transport layer (L4) , these UDP packets then carried in the IP packets

## SIP(session initiation protocol)
- sip is an application layer signaling protocol
- used in IMS signalling
- simple,flexible protocol for creating , modifying and terminating sessions
- sometimes SIP packets carry `SDP(session description protocol)`
  - IP addresses and port numbers
  - codecs uses
  - bandwidth required

## IMS in 5G system 
- IMS architecture remains unchanged
- some IMS interfaces upgraded for 5G SBA(system based architecture)
- these services have the prefix of `Ncx_IMSxxx_xxx`

## CSCFs in IMS
- IMS uses SIP signalling to setup voice calls
- CSCFs (call session control function) are responsible for
  - analyzing and routing the SIP based messages 

![Screenshot from 2023-11-16 16-44-43](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/bcff32fc-0448-4439-afda-fa093649d1c4)

## P(PROXY)-CSCF in IMS
- `sits at the entry of the IMS function`
- routes messages to correct IMS node
- security (eg. flooding attacks)
- QoS for IMS
- forwards request to I-CSCF

## I(INTERROGATING)-CSCF
- `request for registration first comes to P-CSCF , which then is passed to I-CSCF , I-CSCF checks with the UDM whether the UE is already registered with IMS or not , if not then I-CSCF would assign S-CSCF to that user and the I-CSCF would pass that request to the corresponding S-CSCF`
- `similary when there is call coming from another IMS network for the user in this IMS network then that call will come to I-CSCF and the I-CSCF would check with the UDM which S-CSCF the call user is assigned and after that the I-CSCF would pass that SIP call to the corresponding S-CSCF which is assingned to the called user`
- S-CSCF ASSIGNMENT AND SESSION ROUTING
- routing SIP requests from other SIP networks
  - queries UDM to find S-CSCF of called sunscriber
  - routes call to that S-CSCF

## S(SERVING)-CSCF in IMS 
- `once the registration request of the user has reached S-CSCF , it will interact with the UDM in order to get the security info of the UE and then S-CSCF will use this security info to authenticate this user in order to prove whether this is a genuine user or not`
- `once authenticity is proven then S-CSCF will register the UE with itself and send this info to UDM`
- `similarly when this registered UE wants to make a  call , S-CSCF interats with other apllication servers(AS) in order to set up that call in case of voice call the S-CSCF may interact with the telephony application server(TAS) in order to set up the voice call`

## TAS(telephony application server) in IMS
- CSCF provide basic call processing/routing
- during call set up process S-CSCF interacts with the TAS in order to set up a voice call with the features : 
  - calling line ID hiding
  - call divert etc

![Screenshot from 2023-11-16 16-44-43](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/92529748-eac3-49f7-a1b1-5c6bb0ad03a4)


## IMS connectivity requirement
- in order to use IMS , UE needs to connect to IMS

![Screenshot from 2023-11-16 19-03-12](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/152efb0e-3e24-4280-930b-f9874f244929)
`PDN(public data network)`

## PDU Session for IMS connectivity 
- registration : one QoS flow ( used to regidter UE to IMS system)
- voice call : two QoS flow
  - QoS flow 1 (default rule) for IMS signalling(`to generate , maintain and establish the voice call`)
  - QoS flow 2 used as IMS media bearer(`actual packets of voice carried by this one`) , QoS parameter depends on voice call(std,high definition etc)

![Screenshot from 2023-11-16 19-09-48](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/9ce16a2a-0311-4646-a177-a6777014bc69)

## IMS registration : 1. P-CSCF discovery
- in order to communicate with the IMS network , a UE must know at least one IP address of the P-CSCF
- 3 ways
  - `assigned by SMF alongwith UE IP address`
  - `static configuration in UE`
  - `DHCP server can provide the P-CSCF IP/domain name(DNS)`
  - **Dynamic Host Configuration Protocol. The Dynamic Host Configuration Protocol is a network management protocol. It is used on Internet Protocol networks and automatically assigns an IP address to the devices connected to the network using a client-server architecture.**

![Screenshot from 2023-11-16 19-16-09](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/90ec3a6e-e237-47e9-aa54-6338cfcc1b72)

## IMS registration 
![Screenshot from 2023-11-16 19-33-01](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/fc65926d-0e42-4f2b-9235-3da9240b679e)

- in the first step UE sends a registration request to proxy-CSCF
- P-CSCF will then relay this meassage to INTEROGATING-CSCF , now I-CSCF will use `Ncx_IMSRegistration_Get` function to querry the UDM , wether this UE is already registered to the IMS system or not , if not I-CSCF will select a S-CSCF for the UE and send this request to S-CSCF
- now S-CSCF will use registraion service of the SBA(service based architechure)(`NCx_IMSRegistration_register`) in order to send the registration request to the UDM
- the UDM will temp store this UE againse this S-CSCF and smilarlly the S-CSCF will request the authetication information for this UE using `Ncx_IMSAuthentication_Get` service
- once S-CSCF gets this info , it will challenge the UE using this authentication info so that UE proves its genuiness
- UE gives response by sending authentication response
- if is successful then this service-CSCF tells UDM about this success
- UDM registers the UE against this S-CSCF then notifies S-CSCF that the registration is complete
- S-CSCF sends ok message to UE 

## 3<sup>rd</sup> party registration
- we know S-CSCF can offer only basic functions such as session routing or session management but if we want supplementary services we need to invlove AS(application servers)
- for Vo5G we need AS eg TAS
- 3<sup>rd</sup> party registration notifies ASs that user is now connected and ready to communicate

## SIP signalling for Vo5G
![Screenshot from 2023-11-16 20-49-17](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/b30ae951-0c40-40bc-b13f-c4f423304ea0)

- both UEs need to be registered , i.e both need to be assigned a S-CSCF in order to initiate a voice call
-  calling UE would send an INVITE(SDP{session desc protocol} offer) to called UE { what IP address for call , what port its gonna use , which codecs to be used }
-  called UE responds 183 session progress message(SDP answer){IP address , port number, codec}
-  calling UE responds with PRACK(progress acknowledgement)
-  called UE responds with 200 OK
-  IMS meadia bearer is establishment
-  SPD offer message sent from calling UE to called UE in order to indicate that the media bearer has been established
-  called UE sends 200 OK message with 180 ringing(called party is ringing)
-  once called UE picks up the phone 200 OK message is sent to calling UE
-  calling UE acknowledges
-  after this actual voice communication would take place in IMS meadia bearer that has already been established 

## IMS media bearer establishment
![Screenshot from 2023-11-16 21-03-05](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/31d2189f-85d2-4caf-95a6-b87f68497d12)
![Screenshot from 2023-11-16 21-03-27](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/21240c2a-87ea-489f-8cf0-6680f821166c)
![Screenshot from 2023-11-16 21-04-14](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/439a861b-b263-45ed-af6d-812084f36029)

## tearing down the call (ending a call)
- at SIP level
  - one user sends BYE
  - another responds with 200 OK
![Screenshot from 2023-11-16 21-06-32](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/5a6733a7-5699-433e-ba72-52e48a18ee9b)

- IMS media bearer tear down

![Screenshot from 2023-11-16 21-08-22](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/fdf696c3-69fd-4b4d-8642-e6dd87e71e23)
![Screenshot from 2023-11-16 21-08-43](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/c15b0c71-d688-4130-ad67-10963eb384f4)
![Screenshot from 2023-11-16 21-09-09](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/6d8252a9-6ac0-4f5b-800a-7cf523e57db0)

## EPS fallback 
- specially usefull in early phase of 5G deployment where NR coverage is not sufficient
- voice call is setup via NR and 5GC
- UE roams to an area w//o 5G coverage
- NR instructs triggers a handover or redirection to LTE network

![Screenshot from 2023-11-16 21-13-16](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/aa60e613-cced-485c-9317-f67b91954e3e)
