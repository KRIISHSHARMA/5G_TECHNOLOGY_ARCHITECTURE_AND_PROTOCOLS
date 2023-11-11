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

