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
