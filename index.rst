Becoming a Semahpore Network Host
=================================

**What Is A Semaphore Host?**

A Semaphore Host is an individual or entity that deploys nodes and radio hardware to help provide Semaphore Network decentralized internet service and "coverage" to end-users. 

**What are the Prerequisites to Become a Host?**
Hosts need to provide three basic types of physical world capital that host's provide to the network; this capital is utilized to provide dentralized internet services by network subscribers.

Physical Space
  You will need a place to put the radio units, host nodes can stay inside But generally radio untis will need to be placed 
  in an outdoor space high up and with the clearest Line-of-Sight to provide maximum efficienty to end-users. 
  ie. "Vertical Infrastructure"

Internet Access
  In order to access the "traditional" internet a host's will need a general outbound internet connection. IPFS only nodes and various other       
  mechanisms will not require this. 

Radio and Node Hardware
  Various combinations of radio and node hardware and deployments are left up to hosts. But the basic requirements are as follows;


**Hardware**
______________________

Node Hardware
  The node hardware will be capable of monitorinig the on-chain Semaphore Subscriber Registry as well as a fork of what's known in cellular as an EPC/CN [and for WiFi a fork of wpa_supplicant].
  *This can be accomplished on limited hardware such as a raspbery pi.*

Radio Hardware
  Semaphore Network suppots **both** COTS (common off the shelf) regardless of brand or manufacturer and FOSS (FPGA + SDR) radio frontends for 
  hosting network coverage. Semaphore is also band and region agnostic. 

Hardware Freedom
  You are free to choose what works best for your wallet, local DAO community and country's radio frequency regulations; up to and including running 
  a completely FOSS hardware stack.


Generally speaking any eNodeB hardware (cellular equivilant of an access point) is compatible with the Semaphore Network Cellular Protocol; [WiFi specs requires 802.11w and wpa_supplicant].


**We do not gatekeep across hardware, locality or RF frontend**

=======================================
List of Tested Radio Host Hardware (eNodeB)
=======================================



 ================== ============ ========== 
  Name               Band         Status    
 ================== ============ ========== 
  Baicells Nova227   CBRS         Working   
  Baicells Nova223   CBRS         Working   
  Blade RF xA9       Muilt (5G)   Working*  
  USRP/USRP Clones   Multi (5G)   Working*  
 ================== ============ ========== 



**Setup**
______________________

*Node Setup*
  Your host node will provide accounting, authorization and administration services that will let users connect to your decentralized radio.
  To setup your host node you must

* run the EPC/CN executable (forked from SRSRAN)
  <link>
* run the python middleware that will sync with the Semaphore Subscriber Registry on-chain
  <link> 

  After running these two components you are ready to have your radios attach to your host node. Note the IP address that your host node runs at as    you will need to configure your radio frontend with this address.  

Radio Hardware
  Semaphore Network suppots **both** COTS (common off the shelf) regardless of brand or manufacturer and FOSS (FPGA + SDR) radio frontends for 
  hosting network coverage. Semaphore is also band and region agnostic. 


See Physical Setup. 

Software and On-Chain Requisites.

Host's can use the srsRAN EPC fork to connect to their chosen eNodeB. They will need to register through the Host DApp and create a keypair to use when running the network (this can be changed out).    



Becoming a Semahpore Network User
=================================

You can use the Semaphore Network as a user on both cellular (LTE/5G) and WiFi (soon) protocols. 

Using the Semaphore Network Cellular Service:
To become a Semaphore network subscriber you will need to use the Subscriber DApp to 

Requirements:
Obtaining or creating a Semaphore Network ETHSim; this will serve as a hardware wallet and contains the authentication keys that will subscribers on the network

