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


