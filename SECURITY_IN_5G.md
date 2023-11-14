## 5G roaming architecture
![Screenshot from 2023-11-14 11-02-51](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/8af9470b-0f67-4018-8d37-d4e698b7123d)

- visiting UPF controlled by visting UPF , HOME UPF controlled SMF

## logical entities for network access security
- seperate logical entities for security defined to maintain a logical security architecture
- contaibed within 5GC NFs
- logical entities
  - ARPF (AUTHENTICATION CREDENTIAL REPOSITORY AND PROCESSING FUNCTION)
  - AUSF (AUTHENTICATION SERVER FUNCTION)
  - SEAF (SECURITY ANCHOR FUNCTION)
  - SIDF (SUBSCRIPTION IDENTIFIER DE-CONCEALING FUNCTION)

![Screenshot from 2023-11-14 11-09-06](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/6e850ea2-b4f4-416a-9e30-be6955aacc0c)

## SIDF(subscription identifier de-concealing funtion)
- the SIDF is a service offered by the UDM NF in the home network
- it is responsible for resolving the SUPI from the SUCI
- responsible to deconceal SUCI 

## AUSF(authentication server function)
- defined as a standalone NF in the 5GC architecture
- responsible for handling the authentication in the home network
  - based on information received from the UE and UDM/ARPF

## SEAF(seurity anchor function)
- it is functionality provided by the AMF
- responsible for handling the authentication in te serving(visited) network
  - based on info received from UE and AUSF
- `called a seruity anchor cause UE cannot directly communicate with the AUSF or AMF for its authentication`

## ARPF (AUTHENTICATION CREDENTIAL REPOSITORY AND PROCESSING FUNCTION)
- important
- ARPF contains the subscirbers security credentials
   - long-term/master key (K) 
     - uses of master key:authentication , derivation of ciphering and integrity protection keys
    - the subscription identifier SUPI
- ARPF services are provided via the UDM
   - no open interface defined between UDM and ARPF 

## network access securtiy 
- it comprises of all those functions that are related to the secure access of this UE to the network
- mutual authentication
  - UE and network confirm each other's identities 

![Screenshot from 2023-11-14 11-28-36](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/207a583c-1c9a-46f9-bb6b-1fb353417140)

- UE and network must support 2 authentication methods :
  - `5G AKA (5G autentication and key agreement)`
    - for 3GPP access (UE<==>gNB)
  - `EAP-AKA (extensivle authentication protocol - AKA)`
    - for non 3GPP access (WLAN device connected to WLAN access network)

- one the authentication procedure is complete the ciphering and integrity protection keys are generated (ex UE when connected to AMF)
- exceptions - emergency calls

## initiation of authentication
![Screenshot from 2023-11-14 16-54-51](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/2fda3f4e-b3be-49d1-9bf5-7811f4ede1f9)

- based on SUPI , ARPF which type of authentication to be used (AKA or EKA-AKA)

## concealement/deconcealement of SUPI 
- 5G-GUTI is sent if the UE has a valid 5G-GUTI from a previous registration
- if 5G-GUTI not available, SUPI needs to be used
- SUPI is never sent in clear text over the air
- a concealed version of SUPI called SUCI is used 

- SUCI is created by the UE based on publi key cryptography and a protection scheme
- `the HPLMN (UDM/SIDF) can derive the SUPI from the SUCI by using the home network private key` 

![Screenshot from 2023-11-14 17-04-28](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/40a61871-9cf9-4d19-aa9b-5a0dd596989a)

- MSIN (mobile subscriber identification number) is encrypted using home network public key 

## 5G AKA procedre 
![Screenshot from 2023-11-14 17-15-55](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/9835d5d3-cfed-400e-bd67-62e228b5fe06)

- once the authentication procedure has been initiated then UDM has the SUPI and based on the SUPI , UDM decides whether it has to use 5G AKA procedure or EAP-AKA procedure(we are looking at AKA)
- the ARPF generates the 5G home environment authentication vector cause (AUSF and UDM are in hone network)
- the expected response to the random number(XRES) is calculated using the MILENAGE FUNCTION and the input to the milenage function are sequence number , random number , Authentication manaegement field and the master key (K)
-  this milenage function has 5 subfunctions :- `MAC(generates message authentication code)` , XRES(response to random number) , IK , AK

![Screenshot from 2023-11-14 17-19-30](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/cb0f8115-0224-4812-9db3-d8f82ffde458)

- UDM derives XRES* as follows using HMAC-SHA-256 KDF function

![Screenshot from 2023-11-14 17-23-22](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/d575c440-f60f-4a19-b030-eb33b20293f7)

- UDM derives K_AUSF as follows using HMAC-SHA-256(K,S) `KDF(key derivation function)` as below 

![Screenshot from 2023-11-14 17-25-37](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/0e331afc-0f54-4ce0-86f9-451cd643bb51)

- AUSF derives K_SEAF from K_AUSF by passing K=K_AUSF and S= 0x6C || serving network name || length of serving network name to KDF function
- this K_SEAF for the time being is stored in the AUSF 

![Screenshot from 2023-11-14 17-27-52](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/60437617-72c2-4918-833d-b002802d7db9)

- AUSF uses the XRES* to calculate the HXRES*
- HXRES* calculation at AUSF : HXRES* is 128bit MSB of the output of SHA-256 hash, calculated by passing RAND||XRES* as input to SHA-256 algorithm 

![Screenshot from 2023-11-14 17-30-35](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/65a20eaa-302c-41c4-b129-7f8a0b9a4d9e)

- AUSF sends the 5G SE AV (serving environment authentication vector) to the AMF (SE cause AMF is located in the serving network of the UE)
- SEAF(AMF) stores the HXRES* and send random number (RAND) and authentication token (AUTN) tothe ME (mobile equipment) which send it to USIM

- USIM verifies the AUTN and derives the RES and keys(CK,IK)

- UE uses milenage function to derive XMAC , RES , CK , IK as below

![Screenshot from 2023-11-14 17-36-38](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/bef02ddb-037a-4dbb-8e5f-39a2c0260696)

- if the XMAC and MAC are the same then it means its the genuine mobie network that this UE is connecting
- also verifies that sequence number(SQN) is in the correct range

- CK and IK are sent to ME and it calculates RES* and derive Kausf key , Kmac key , Kamf key
- then ME send RES* and MAC to the AMF(SEAF)

- SEAF(AMF) calculates the HRES* from RES* and compares it with HXRES* from the HXRES* it hase already stored if they are the same it means it is good
- AUSF compares RES* with XRES* (AUSF stores XRES*) if it is the same then authentication is successful 

## 5G security key hierarchy 
![Screenshot from 2023-11-14 18-17-09](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/d8a2a73e-f6c0-44bc-b451-c7113afd2e18)

- K<sub>NASint</sub> used for integrity protection of the link that is there between AMF and UE
- K<sub>gNB</sub> handed over to gNB from AMF used to derive the following
  -  K<sub>RRCint</sub> signaling between UE and gNB is called RRC k K<sub>RRCint</sub> does integrirty protection
  -  K<sub>RRCenc</sub> encryption of RRC
  -  K<sub>UPint</sub> integrity protection of data that is flowing from UE to gNB
  -  K<sub>RRCint</sub> encryption of the flowing data  

- `the AMF passes K_gNB to the master eNB/gNB`
  - `stored there till the UE is in the state of CM-CONNECTED`
- `the encryption and integrity keys are 256 bits long`
  - `but are truncated to 128 bits before use , future provision 256 bits`
- `ciphering/integrity keys called as low level keys as these keys are used just between OSI layer 1(physical layer) and layer 2(data link layer) `

## ciphering/integrity algo in 5G 
![Screenshot from 2023-11-14 18-34-22](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/41340453-dc58-4f99-9602-0ada7ebbd62a)

## 5G EAP-AKA for non-3GPP access architecture 
- used for authentication of non-3GPP devices if they want to connect to 5GCN 

![Screenshot from 2023-11-14 18-37-19](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/6495d156-a4af-42ec-b13d-de23ab74360d)

- instead of UE directly connecting to AMF it first connects to access point for WLAN  
- In order to connect to 5GC will need protocol converison which is provided by `N3IWWF`(non-3GPP access interworking function)

## 5G EAP-AKA(extensible authentication protocol - authentication and key agreement)
- defiend by IETF in RFC 3748 is a protocol framework for
  - authentication
  - typically between an end-user device and a network
- first introduced for the point to point (PPP)
- EAP is not an authentication method per se but rather
  - `a common authentication framework to impelement specific authentication methods`
- `EAP is therefore "extensible" as it enables support for different authentication methods`
- new authentication methods can be added
- these authentication methods are typically referred as EAP methods 

## 5G EAP-AKA' (subtype of 5G EAP-AKA)
- it is for performing authentication based on USIM cards
- UDM/ARPF will generate a transformed `authentication vector(AV')` and provide it ti the AUSF
- the AV' consists of 5 parameters
  - RAND (random number)
  - XRES (expected result)
  - AUTN (network authentication token)
  - CK' and IK' (keys)

![Screenshot from 2023-11-14 18-57-08](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/61e045d3-4bbf-4e76-b9f3-b060dba3c3cf)

- UDM generate AV'(RAND,XRES,AUTN,CK',IK') which is given to AUSF
- AUSF will keep XRES,CK'and IK' within itself and calculate the MAC(message authentication code) , generate K<sub>AUSF</sub> and from this will generate K<sub>SEAF</sub> and will keep  K<sub>SEAF</sub> in itself and forward RAND,AUTN,MAC to AMF
-  AMF will challenge the ME using RAND,MAC,AUTN , ME will kepp MAC and forward RAND , AUTN to USIM
-  USIM verifies the AUTN and derives the RES and keys(CK,IK) and forward it  to ME
-  ME/UE verifes the MAC and derives  K<sub>SEAF</sub>, K<sub>AUSF</sub>, K<sub>AMF</sub>
-  UE sends response to the challenge with RES , MAC '
-  AMF then forwards the RES , AC to AUSF (*AMF just forwarding messages not calculating any hashes or doing any comparison*)
-  AUSF compares RES with XRES and checks if ir is valid response if the value is correct it means its good , it also verifies MAC and finds them correct
-  AUSF then sends  K<sub>SEAF</sub> to the AMF and AMF will then derive the  K<sub>AMF</sub> based on  K<sub>SEAF</sub> and will keep  K<sub>AMF</sub> with itself
-  AMF then informs the UE that authenticaion was a success 

## 5G security key hierarchy for EAP-AKA (non-3GPP Access)

![Screenshot from 2023-11-14 19-26-02](https://github.com/KRIISHSHARMA/5G_TECHNOLOGY_ARCHITECTURE_AND_PROTOCOLS/assets/86760658/0e1dcc7e-0ca8-470b-a548-58e5ffcf69a2)

