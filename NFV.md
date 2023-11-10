## network function virtualization(NFV)
- problem with traditional mobile networks
  - network nodes implemented as special purpose hardware
  - the hardware is expensive to produce install and maintain
  - the hardware eventually needs to be replaced
  - difficult for new hardware vendors to enter the market
  - difficult to upgrade the network to support new cases eg: mMTC
 
- **NFV approach**
  - networks functionalities is implemented in software
  - which runs on COTS(commercial off the shelf) hardware such as servers , storage and switches
- **NFV brings several advantages**
  - the costs of both hardware and software reduces
  - easier for new vendors to enter the market
  - far easier to upgrade the network by simply upgrading the software  

## NFV architecture by ETSI (european telecomm standard institute)
- **virtual network function** : software implementation of a network function
- **NFV infrastructure** : physical hardware resources , such as computing , storage and networking
- NFV management and orchestration encompasses the management of the
  - physial resources
  - virtual resources
  - and VNF

![Screenshot from 2023-11-10 15-56-22](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/842428b3-0785-4759-a4e1-8baabf3837d6)

- example

![Screenshot from 2023-11-10 15-58-48](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/7e676202-92c7-44fd-808a-19998b9384ff)

## advantages of NFV in 5G
- 5G is a collection of network functions
  - virtualized
  - run on a cloud infrastructure
- cost effective network based on COTS
  - no custom hardware
- ability to deploy new network functions quickly
- shared usage of resource
- scale up or scale down resources as per requirement
  - scale up AMF capacity in minutes using MANO

## 5G network slicing 
- 5G network slicing enables service providers to build virtual E2E networks tailored to application requirements
- NFV will enable network slicing
  - allows creation of multiple virtual networks on shared physical infrasturcture
- virtual networks are isolated in the control plane and user plane
- user experiences them as a physically seperate networks
- slicing crucial in 5G because of different Qos requirements for multitude of services
  - eg : low latency powerful mobile broadband
- capabilities of slice optimised for one use case
- on demand allocation of resources 
![Screenshot from 2023-11-10 17-43-25](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/4595722c-03d9-4238-a2ac-50e13de22891)
