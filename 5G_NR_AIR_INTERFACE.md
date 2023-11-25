## channel and trasmission bandwidths
- the radio bandwidth of the channel that is being used by an operator in a given gNB depends upon 2 factors
  1. how much total bandwidth has been assigned by the regulator to the operator
  2. second , out of that total bandwidth how much bandwidth has been used by the operator in this gNB , that bandwidth is called **channel bandwidth(MHz)**
 
- this channel bandwidth includes guardbands so that the transmission that are being made in this channel do not interfare with the adjacent frequency channels 
[look in to this](https://dsp.stackexchange.com/questions/78694/what-is-the-difference-between-a-guard-band-and-a-cyclic-prefix-in-ofdm#:~:text=In%20contrast%20the%20guard%20interval,generated%20in%20the%20modulation%20process.)


- when you remove gaurdbands from channel bandwidths you get **Transmission Bandwidth Configuration N<sub>RB</sub> (total number of available resource block that are there in a gNB that can be used for transmission) [RB]**
- out of that Transmission Bandwidth Configuration at a time there may be a subset of the resource block that are actually being used for the transmission
- these Active resouce blocks depend on time of day (more when more calls , less at night necause of less load)
  
![Screenshot from 2023-11-24 19-14-41](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/20f6c94b-68c2-435a-8d88-4e1754ad93dd)

## maximum transmission bandwidth configuration (FR1)
- channel bandwidth lies between 5 and 100 MHZ in frequency range 1
- and if we are using min bandwidth as the gaurdband so the maximum transmission bandwidth or in other word maximum number of resource blocks that are available for transmission they depend upon channel bandwidth

![Screenshot from 2023-11-24 19-21-52](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/3fa92aef-3742-418a-8983-8c604fefaca9)


- as we increase the bandwidth the resource blocks are increasing
- we cannot use the 15KHz with 60 MHZ bandwidth cause this is a very high bandwidth
- as we increase SCS from 15KHz to 30 KHz we see that we can now use 60MHz or more bandwidths but `they are less than the 15KHz SCS`
- in 60KHz spacing 5MHz is not available cause 5MHz channel bandwidth is small for this 60KHz SCS 

## maximum transmission bandwidth configuration (FR2)
- channel bandwidth is between 50 and 400 MHz in frequency range 2

![Screenshot from 2023-11-24 19-30-12](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/24361027-9063-4f02-be2b-529e03839529)


## Reference frequency (F<sub>ref</sub>)
- in individual channel there is a centre frequency of this channel which is called the Reference frequency (F<sub>ref</sub>)
- this reference frequency has an assosiated number which is called NR-Absolute Radio Frequency channel number (N<sub>ref</sub>)
- **NR-ARFCN** is used to identify this channel

![Screenshot from 2023-11-24 19-41-47](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/6a40533c-51c6-4376-993b-0b2326cb5ada)

- the operator may decide instead of using a channel in a gNB it wants to use another channel in that gNB only
- but in these 2 channels the bandwidth is the same but the frequencies are different as a result the center frequency or refernece frequency has changed
- therefore associated NR-ARFC will also changed

![Screenshot from 2023-11-24 19-45-44](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/62ef6f50-5c65-461a-b380-1d8c49f52a75)

## reference frequency calculation F<sub>ref</sub>
![Screenshot from 2023-11-24 19-47-28](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/e48cd536-6c5e-42f2-9935-e5a939341c92)

- global raster is the min distance in terms of frequency that can be there between reference frequencies
- channel raster is the minimum distance between center frequencies of two channels 

## Difference between global and channel Raster 
- above 3 GHz , every refernce frequency can act as the center frequency for the channel that means channel raster and global raster is same
- below 3 GHz , the global raster is 5KHz that means minimum distance between 2 between two reference frequenies is 5KHz but channel raster can be 15KHz or 100KHz

![Screenshot from 2023-11-24 21-12-46](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/d122dd44-b9eb-4c9d-ac4b-895b19b6e3ab)


## Bandwidth part (BWP)

- in LTE , UE's radio bandwidth usually same as eNB bandwidth
- in 5G , UE,s radio bandwidth can be less than gNB bandwidth
- BWP is a contiguous set of RBs
  - subset of the base stations transmission bandwidth configuration

![Screenshot from 2023-11-24 21-22-40](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/1c3d119d-b985-4efd-a94e-038434f2ba65)

- numerology = SCS 
- UE can be assigned
  - upto 4 BWPs in downlink
  - upto 4 BWPs in uplink
- at one time
  - only one BWP ative in uplink
  - and one BWP ative in downlink
- BWPs can overlap but active at different time 

![Screenshot from 2023-11-24 21-24-54](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/7ff3b5bb-a7fe-4043-a9e0-f34bd3cac8c6)

## Resource Grid 
- the total bandwidth that is there in a cell is divided into resouce blocks in frquency domain
- while in the time domain we have frames each frame is of 10ms and it has 10 subframes of 1ms each
- if we have SCS of 60 KHz we will have 4 slots per subframe (2^2)
- `the normal CP is 14 symbols per slot in time domain and 12 subcarriers in frequency domain`
- The 3GPP documents describes a resource block to be a group of resource elements spanning 12 consecutive subcarriers in the frequency domain and one slot in the time domain.

![Screenshot from 2023-11-24 21-37-03](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/12916721-710a-4bdf-868b-6a41079150e7)

- each cell/gNB can have multiple resouce grids (eg one resource grid for UL and one for DL)
- there is one resource grid for each combination of
  - direction(UL or DL)
  - antenna port in MIMO
  - SCS configuration

## 5G NR Model for Air interface channels 
- 3 channels
  - physical
  - transport
  - logical 

![Screenshot from 2023-11-24 21-51-53](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/6ab5dc7f-4fc6-4ce0-9f52-94a26c1f1f19)

## 5G NR logical channels 
- black arrow --> channels in DL direction
- red aarow --> channels in UL diretion 

![Screenshot from 2023-11-24 21-56-05](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/020732cb-1e6b-45a9-b14a-e486dae19033)
![Screenshot from 2023-11-24 21-56-23](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/95184bdb-f70d-4a9e-8d37-af305c6a17bf)

## Dedicated , Common and Broadcast Logical Channels
- Dedicated Channels(P2P channel)
  - channels reserved for a single user
    - **DTCH (dedicated trafiic channel)**(in case of call)
    - **DCCH (dedicated control channel)**(signalling to support this call would be carried on by DCCH)

- Common Channels
  - channel shared between users
  - no reserved channels
    - **PCCH (paging control channel)**(incoming call , gNB uses PCCH to page the UE)
    - **CCCH (common control channel)**(used by UE in order to initiate a call with the network)

- Broadcast Channels
  -  channels for broadcasting to user in a cell
    - **BCCH** (broadcasting control channel)(broadcast system info to UE that are there in the cell)

## 5G NR channels (Transport channels)
- PCCH is mapped by **PCH (paging channel)**  
- BCCH mapped by **BCH (broadcast channel)**
- CCCH , BCCH , DTCH and DCCH are multiplexed on the **DL-SCH(DL-shared channel)**
- in UL **UL-SCH(UL-shared channel)**  is being demultiplexed into CCCH,DCCH,DTCH

![Screenshot from 2023-11-24 22-20-54](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/5b3225a8-f30b-4c31-a591-21815fb7e751)

## 5G NR channels (Physical channels)
- uptill now info was being carried out in the form of bits
- in order to transmit that info over air interface we need to convert that info into EM signal
- a physical channel that has certain phyical layer procedures applied to it so that it can carry that info in form of EM signal
- for eg **PBCH (physical broadcast channel)** is taking info as bits from the BCH and it is then transmiting that info over air interface
- **PUSCH(physical UL shared channel)** receives info as EM signals and gives it to UL-SCH 

![Screenshot from 2023-11-24 22-47-06](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/bee62a00-aad2-47e6-a74b-2620cb0f7e09)

- yellow colured physicals channels called physical signals do not take any info from physical layer or any higher layer and sending on the air interface
- purple colured PC , these physical channels take info from 1st layer and transmit it as EM signals over air interface or vice versa
- orange coloured PC , these physical channels take info from 2nd layer or higher send info over air interface or vice versa  

- first looking at yellow coloured channels
  1. DM-RS(demodulation-reference signal) : almost all purple and orange coloured physical channels that are carrying some info have an associated DM-RS (exception : PRACH(physical random access channel)) therefore it is an important physical signal . DM-RS helps the receiver to demodulate the incoming signal .
 
  2. SRS (sounding refernce signal) : transmitted by the UE on differnet subcarrier frequencies in the UL towards the gNB , gNB makes quality measurement on those subcarriers , then gNB comes to know what are the subcarriers that are best for this UE for UL transmission . based on this gNODEB schudeles RB foe uplink transmssion and modulation scheme (256QAM {8 bits transmitted per RE/1 OFDM symbol} , 62QAM {6 bits transmitted per RE/1 OFDM symbol}, etc) . `helps the gNB receiver to determine which UL subcarriers are best for the UE`
 
  3. CSI-RS (channel state information-reference signal) : helps the UE receiver to determine the best downlink subcarriers , the best downlink modulation scheme . it is transmitted by the gNB towards the UE in the DL on different subcarrier frequencies and then UE makes quality measurments on these subcarriers , based on that the UE decides that which subcarriers or physical resource blocks are good for DL transmission and what is the best modulation scheme that can be used on those subcarriers and the UE sends this info back to gNB as UL-control inforamtion and based on that info gNB can decide what RBs it can use in the DL and modulation scheme on those RBs
 
  4. PT-RS (phase tracking reference signal) : helps the receiver to compensate for phase errors at high radio frequencies (mmwave) , and maintain phase synchronization 

## Procedures to Understand 5G channels 
1. cell aquisition
2. intial access
3. scheduling of data transmissions
4. paging

## 5G NR Cell acquistion procedure 
- this procedure is run by a UE when you power on your UE
- cell acquisition is procedure in which
  - UE discovers nearby cells
  - UE decodes the cell ID and other system info in those cells
  - in a cell this system info is being transmitted by the **BCCH**(logical channel) this logiacal channel is the mapped to the transport channel of **BCH** and this BCH is then mapped to the **PBCH** and associated with this PBCH you have **PSS**(primary synchronization sequence) and **SSS**(secondary synchronization sequence) and you have the physical signal **DM-RS**
  - togther all these physical channels are called as the **SSB** (syncronization signal block)
  - this SSB are transmitted on some specific frequencies and those are called **Global synchronization channel numbers**
  - once powered on UE tunes to those specific frequencies called **Global synchronization channel numbers**
  - UE then tries to detect synchronization signal block **SSB**

![Screenshot from 2023-11-25 09-52-19](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/68e83c3d-52e7-411c-be24-25c37b00895d)


## Cell Acquisition : BEAM SWEEPING
- in a cell you have different beems that are transmiited over different directions
- these SSB blocks are transitted one after the another called **SSB burst**
- this procedure of transmitting SSB blocks one after another on the beams in different directions is called beam sweeping procedure
- each SSB blocks in SSB burst has a unique SSB index
- no. of SSBs in burst (as frequency increases the beams become more sharp the number of beams in a cell increase hence no. of SSB blocks depend on frequency)
  - 4(below 3 GHz)
  - 8(3 to 6 GHz)
  - 64(6 to 52.6 GHz)

![Screenshot from 2023-11-25 10-06-33](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/a4e5abda-433c-423b-9370-4cff28ca0075)

## Cell Acquisition : SSB Block 
- SSB block is mapped on the resource grid like this

![Screenshot from 2023-11-25 10-14-35](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/a789d10c-6929-45c4-bd31-b0257b2b3e83)

- in the PBCH within each [BRB](https://www.telecomtrainer.com/brb-basic-resource-block/) DM-RS is being transmitted in every 4th subcarrier
- UE measure power of SSBs on DM-RS to determine which is the most powerfull beam
  - part of SSB index carried by DM-RS(& other by PBCH)
- this SSB block is modulated using **QPSK** modulation

![Screenshot from 2023-11-25 10-21-56](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/634b4a19-088c-4eff-8c3d-71db11013b3e)

## Cell Acquisition : physical cell ID (PCI)
- In the next step UE determines the **Physical cell ID(PCI)**
- inorder to determine PSI the UE needs to determine the **PSS** and the **SSS**
-  **PSS** consists of 3 possible sequences , numbered 0-2 , determined by the UE as NID(2)
-  **SSS** consists of 336 possible sequences , numbered 0-335 , determined by the UE as NID(1)
-  once the NID(1) and (2) are determined they are put into the formula and generate the **PCI**
-  in 5G PCI is a number that can lie between 0-1007 

![Screenshot from 2023-11-25 10-35-57](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/ef891376-7887-488c-8a02-79a0a2485ed0)

## Cell Acquisition : physical broadband channel (PBCH)
- UE decodes the PBCH to get **MIB**(master info block)
- **MIB**contains information about
  - cell barred or not ?
  - system frame number **SFN**
  - **DM-RS configuration for PDSCH for SIB1**
  - **configuration and location of PDCCH** (CORESET0) 

## Cell Search : control resource set (CORESETs)
![Screenshot from 2023-11-25 12-29-16](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/ce76acb5-9f65-4bbf-ba93-31a8aa09d2c1)

## Cell Acquisition : System information block 1 (SIB1)
- SIB1 contains the remaining minimum system information
- this SIB1 is carried on the **PDSCH**
- **PDSCH** location on resource grid is in the **DCI**(downlink control information) and this **DCI** is carried in the **PDCCH** that is on the CORESET0
- after decoding SIB1 , UE gets
  - parameters for cell access/connection
  - location of other SIBs
  - PLMN(identity of mobile network whom this cell belongs to) , TAC(tracking area code where the UE is currently located) etc

![Screenshot from 2023-11-25 12-41-28](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/d3e93911-9f9a-4646-bf39-64acbe97f62a)

## Initial Access (RACH Procedure) 
- once the UE has decided which gNB it wants to register then it initiates that process by RACH procedure 

![Screenshot from 2023-11-25 15-47-17](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/66b6e6f5-24cb-4ba2-b694-6dab17d0ea13)

- (msg1) At the start of the initial process UE sends a preamble to gNB using **PRACH** (physical random access channel) .

- (msg2) then the cell responds with **PDCCH** and using **PDCCH** the cell assigns a **PDSCH** in the DL
- and on this**PDSCH** there is the response of the cell to the preamble or `random access response` and in this response the cell assigns
  - A temp **C-RNTI**
  - A UL scheduling grant
  - Timing advance , will enable the UE to send its transmissions at a time that its UL transmission is synchronized with the UL transmissions of the other users

- (msg3) Once the UE receives this message the UE responds using the **PUSCH**
- In this response , the UE requests a RRC setup connection and this request will also contain the **UE ID** (no collision)

- (msg4) When msg3 is received by the cell , it will again use **PDCCH** to assign **PDSCH**
- In this **PDSCH** there will be **RRC** connection setup message , means **RRC**(radio resource connection) can now be set up

- UE then ACK it using **PUCCH**
- using **RRC** connection the UE registers itself with the cell 

## scheduling data transmission 
- for ex cell has some data or signalling that it needs to transit to the UE
- first the cell will use **PDCCH** to assign a **PDSCH** to this UE , using this **PDSCH** , the cell would then send the data or signalling to the UE
- Then the UE will respond using the **UCI**(UL control information) to the cell , if this UE needs/wants to the send some data or signalling to the cell , then it can make that request in the **UCI**
- As a result of this request the cell would then use **PDCCH** to assign **PUSCH**
- using this  **PUSCH** UE can send data or signalling to thr cell
- and then the cell can ACK this using the **PDCCH**

![Screenshot from 2023-11-25 18-24-49](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/a4c24555-c74f-412b-ab2f-9c0235ed5d2d)

![Screenshot from 2023-11-25 18-28-56](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/78fbe42e-5ecc-49cd-a3af-a4a624e15b51)

- gNB is using the **DCI**(DL control info) that is there in **PDCCH** to assign the **PDSCH**
- **PDSCH** carries data or signalling from gNB to UE
- the UE can then ACK using **UCI**
- similarly **DCI** on **PDCCH** assigns **PUSCH** using which UE can send data or signlling to gNB
- gNB can ACK this info using **DCI** `that would be ther in the next` **PDCCH** 

## DCI (Downlink Control Information) 
- DCI helps the base station and user devices coordinate when and how data should be transmitted and received.
- **DCI** used to schedule
- modulation scheme and Coding Rate
  - BPSK , QPSK , 16QAM , 64QAM , 256QAM(8bits/symbol)
  - indicates new transmission or re-transmission (In simple terms, DCI scheduling helps manage whether the communication system is sending something for the first time or if it's re-sending information that may not have been successfully received in earlier attempts.)

## UCI (UL control information)
- UCI
  - ACK/NAK for DL transmission
  - `Make UL sceduling request`
  - **CQI** (channel quality information) : feedback about DL subcarriers by the  UE to the cell using **UCI** , this feedaback is in form of **CQI**
- **UCI** is carried on **PUCCH** but can be arried by **PUSCH** too (if present) 

## Coreset (revisited) 
- we know that **PDCCH** is located in a region called as the **coreset** and the **PDCCH** only in DL which means **coreset** also exists in the DL

- `Max 3 CORESETs can be configured for an active downlink BWP`
- A UE can have 4 BWPs and each have 3 CORESET (total 12 CORESETs)
- CORESETs are active only when their associated BWP is active , **with the exception of CORESET 0(carriers minimum system info)** 

## Paging 
- whenever there is a incoming call for the UE , the gNB needs to page the UE , and for that paging **PCCH** (paging control channel) is used
- the **PCCH** is mapped on the **PCH**(paging channel) and  then mapped on **PDSCH**
- when there is an incoming call for UE and it is paged by the gNB the UE responds by the **RACH** procedure and establishes connection with the gNB to get connected with that call 

![Screenshot from 2023-11-25 20-48-15](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/477516e2-17c2-429d-a1d5-6767568d3d60)





