# 5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS

## [ACRONYMS](ACRONYMS.md)

## INTRODUCTION [module 1]

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

## MOVING FROM 4G TO 5G [module 2]

### 5G architecture 
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

## [module 3]
## key features of NG RAN or 5G RAN
### Dual connectivity (DC)
- LTE  eNB connected to EPC
- enhanced eNB connected to 5G Core
- 5G gNB connected to 5G core
- master nodeB decides data and Qos a UE gets
- bearer splitting(some data to UE , some to another nodeB etc)  can take place at either of the nodeB's
 ![Screenshot from 2023-11-08 18-47-46](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/e313a7de-52e3-474c-9aca-67f38f7b9b14)

### small cells in 5G networks
- small cells directly related to DC
- have 5G air interface but limited coverage (10m - 2km)
- less channel impairments due to small coverage size 
- application
  - homes , stadiums , concerts and offices  to improve coverage
  - used in DC to increase user data rate
![Screenshot from 2023-11-08 18-50-34](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/31f4c3c0-4e72-447d-8e88-e4f11910f6b5)
 
### increased wireless spectrum 
- 5G NR can operate in 2 frequency ranges
  - FR1 450-6000MHZ
  - FR2 24250-52600MHz
- `Below 1 GHz` : excellent in building penetration `(great for large area cells)` , wide area coverage tens of km , limited spectrum availability 
- `1-6 GHz` : good coverage and good spectrum
- `6-100 GHZ (mmWave)` : low range (coverage inversely prop to frequency) , but a lot of bandwidth , effected by building penetration , `good for small cells` 


























































