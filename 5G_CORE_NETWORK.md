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
