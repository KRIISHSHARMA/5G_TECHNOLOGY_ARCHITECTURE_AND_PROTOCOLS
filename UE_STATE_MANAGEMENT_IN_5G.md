## UE state management
- 5G system needs to be able to keep track of each UEs
  - availability
  - reachability
- keeps track of 3 states of UE
  1. RRC radio resource control (between UE and gNB)
  2. CM connection management `(between UE and AMF) also called non access stratum connection(NAS)`
  3. RM registration management (between UE and AMF)

![Screenshot from 2023-11-17 11-57-31](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/1a5eac62-d5ec-4624-a1a8-9dffbbd04361)

## 1. RRC (radio resouce control) state
- status of RRC connection between UE and gNB
- RRC-idle : No RRC connection
  - UE monitors broadcast info(that it is recieving from the gNB)
  - cell selection/reselection
- RRC connection required for
  - registration
  - voice call etc
- RRC connected
  - UE location known to cell level

![Screenshot from 2023-11-17 12-06-23](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/1aa3b343-962d-4356-aa2c-2acdc7529e16)

- RRC-inactive : intermediate state introduced in 5G(saves battery power)
  - `RRC connection context (parameters) stored in UE and gNB`
  - RRC connection can be ativated with minimum signalling
  - decrease in signalling
  - suitable for massive IOT

## UE mobility in RRC_inactive state: RAN areas
- RAN area are very like TAs nut relevant to the RAN
- size of RAN area
  - min --> one cell of a TA
  - mac --> all the cells of a TA
- RAN areas do not overlap
- `each RAN area is identified using RAN area ID`

![Screenshot from 2023-11-17 12-13-31](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/ae4d4172-92d2-446c-be41-be6d05c927a0)

## UE mobility in RRC_inactive state: RAN-based notification areas(RNAs)
- `one or more RAN areas of same TA can be grouped as RNA(RAN-based notification areas)`
- the 5G RAN can assign a RNA to a UE
- in RRC_INACTIVE state,
  - the RAN knows the RNA in which mobile is in
  - RAN notifies the network if it moves to another RNA
  - to contact UE , RAN pages all the cells in a RNA
- reduced signaling : RNA updates instead of cell updates
- `in case of RRC_INACTIVE case the UE only notifies RAN about cell change if that cell belongs to a diff RNA this reduces load and save battery life of UE `

## 2. CM (connection management) state
- `whether an active NAS connection exists between UE and AMF or not`
- `also called N1 signalling link`
- CM-idle : no N1 connection between UE and AMF (`AMF knows ue registration area`)
- CM-connected used for (AMf knows UEs current gNB)
  - registration
  - data transfer
  - registration update

![Screenshot from 2023-11-17 12-33-30](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/fd472942-670d-46e7-b941-5fcddd3e7140)

**registraion area = UE TA list**

## 3. RM (registration management) state
- `RM state is used to indicate the status of registration of the Ue with 5G network`
- RM-deregisterd
  - swithed off or deregistered
- RM-registered
  - registered with %GC
  - served by an AMF
  - assigned a 5G-GUTI
  - registration update
    - UE enter another RA 

![Screenshot from 2023-11-17 12-38-30](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/b811b679-ef14-4571-86cb-83b422653ee6)

## combined state diagram 
![Screenshot from 2023-11-17 12-39-53](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/62c48303-ec9f-48a9-a6ab-7b3024a133d0)
![Screenshot from 2023-11-17 12-41-08](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/b5144c8a-b8fd-4467-a4c6-c61b06f84998)

