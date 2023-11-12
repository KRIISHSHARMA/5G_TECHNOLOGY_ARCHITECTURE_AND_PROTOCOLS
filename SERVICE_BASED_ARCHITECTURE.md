## 5G sevice based architecture
- service based arch introduced to increase modularity
- a NETWORK FUNCTION provides one or more servicrs to other network functions in the network
- these services are made available over service based interfaces of network funtion interface 

![Screenshot from 2023-11-12 15-35-29](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/63471c27-926b-448f-856c-562a131ba2a6)

## main mechanisms for NF services
- request-reponse :
  - NF service consumer requests a service
  - NF service provider returns
    - information to the consumer
    - or performs an action , or both
  - subscribe-notify :
    - NF service consumer subscribes to provide service
    - provider notifies the consumer about
      - the occurrence of events or
      - periodic updates related to the service

![Screenshot from 2023-11-12 15-40-20](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/fbbdb362-b506-4166-a5c4-82aa42922d57)

## HTTP/2 for 5G core network
- HTTP/2 used for communication between NF's
- easy deployment in cloud environment
- HTTP/2 is already very widely deployed
  - well developed security mechanisms , third party applications
- easy integration of operatorand third-party applications

##  HTTP/2 on web vs HTTP/2 in 5G Core

![Screenshot from 2023-11-12 15-48-29](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/3889102b-d218-4ddc-829c-fe36d56a5522)

- in 5G core request-response data only in JSON format 

## JSON format
``` bash
{
     "empid":"SRAETS",  #name-value pair
     "personal":{
           "name":"smithjones",
           "gender":"male",
           "age":23,
           "address" :
     {
            "streetadd":A"efaeaegaegE",
            "city":"afae",
      }
  }
      "profile":{
           "designation":"aefaef".
          }
}
```

## concept of resource
- exmaple of reources
  - PDU session
    - context
    -   QoS policy
 - NF registration with NRF
- resources located and manipulated as URI(uniform resouce identifier)

![Screenshot from 2023-11-12 16-01-22](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/4948437d-e7d0-45a6-9a11-a5cff4b735f0)

## HTTP methods used in 5GC 
![Screenshot from 2023-11-12 16-03-08](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/504d08a0-cf68-4f68-8b6f-68b9b20a70b5)

## HTTP reponses in 5G 
![Screenshot from 2023-11-12 16-04-58](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/08e72f74-2f77-4ebf-9a09-e1e1d0368d35)

## naming scheme for NF services
![Screenshot from 2023-11-12 16-16-38](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/5f2e6393-30b6-4b78-8231-76f5f82e8ee1)

## REST applied to 5G sevices
- defines a set rules for design of distributed applications
- the 5GC service API implemented according to the REST "paradigm"
- in the context of 5GC rules of REST applied to HTTP protocol

## principles of RESTful design
- client/server : split of responsibilities between client and server
- stateless : each request from client must contain all the info necessary to understand the request
  - session state is therefore kept entireely on the client
- cacheable : clients get indication from servers whether the received information can be cached at client
- uniform interface : identification and manipulation of resources through URI's
- layered system : each component cannot "see" beyond the immediate layer with which they are interacting 

## Use case 1 : NF service registration
![Screenshot from 2023-11-12 16-30-30](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/bff18d36-8476-499f-af52-dfe2a33b4d24)
![Screenshot from 2023-11-12 16-31-37](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/8d0dcc72-3788-41ee-b337-b4f3fb9f3b31)
![Screenshot from 2023-11-12 16-34-17](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/30c75dc0-dcb1-40e6-b09f-9061beb0b636)

## Use case 2 : NF sevice discovery 
![Screenshot from 2023-11-12 16-37-36](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/7a18607f-7105-42c4-b5b9-6d7161268986)

