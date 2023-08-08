Becoming a Semahpore Network Host
=================================

**What Is A Semaphore Network Host?**

A Semaphore Network Host is an individual, DAO or entity that deploys host node and radio hardware to help provide Semaphore Network's decentralized internet services and Universal Basic Internet "coverage" to subscribers. 

**What are the Prerequisites to Become a Host?**

Hosts need to provide three basic types of capital that will be utilized to provide dentralized internet services to Semaphore Network Subscribers.

Physical Space
  Hosts will need a physical place to put the radio units. While host nodes can stay inside or even be hosted remotely;
  Generally, radio units will need to be placed in an outdoor space high up and with the clearest Line-of-Sight to provide maximum efficienty for Subscribers. Physically, a 3ft^3 area is enough with extra for a multi-kilometer deployment

Internet Access
  In order to access web2 internet services (traditional internet) a host will need to provide an outbound internet connection.
  The outbound connection can come from a variety of sources and providers.
Radio and Node Hardware
  Various combinations of radio and node hardware deployments are left up to hosts. But the basic requirements are as follows;


**Hardware**
______________________

Node Hardware
  The node hardware will be capable of monitorinig the on-chain Semaphore Subscriber Registry as well as a fork of what's known in cellular as an      EPC/CN [and for WiFi a fork of wpa_supplicant].
  *This can be accomplished on limited hardware such as a raspbery pi.*

Radio Hardware
  Semaphore Network suppots **both** COTS (common off the shelf) and FOSS (FPGA+SDR) radio frontends regardless of brand or manufacturer for hosting    network coverage. Semaphore is also band(frequency) and region agnostic. 

Hardware Freedom
  You are free to choose what works best for your wallet, local DAO community and country's radio frequency regulations; up to and including running 
  a completely FOSS hardware stack. Generally speaking any eNodeB hardware (cellular equivilant of an access point) is compatible with the Semaphore Network Cellular Protocol; 

[Future: WiFi spec requires openwrt/embedded Linux, 802.11w and hostapd].


**We do not gatekeep across hardware, locality or RF frontend**

=======================================
List of Tested Radio Host Hardware (eNodeB)
=======================================


 ================== ============ ========== ======= 
  Name               Band         Status     Type   
 ================== ============ ========== ======= 
  Baicells Nova227   CBRS         Working    COTS   
  Baicells Nova223   CBRS         Working    COTS   
  Blade RF xA9       Muilt (5G)   Working*   FOSS*  
  USRP/USRP Clones   Multi (5G)   Working*   FOSS*  
 ================== ============ ========== ======= 



**Setup**
______________________

*Node Setup*
  Your host node will consult the on-chain subscriber registry for decentralized accounting, authorization and administration services that will let   users connect through your decentralized radio.
  

  To setup your host node you must:

* Run the EPC/CN executable (forked from SRSRAN)
  <link>
* Run the python middleware that will sync with the Semaphore Subscriber Registry on-chain
  <link> 
* Get Public Key from middleware to register host on-chain

  After running these two software components you are ready to have your radios attach to your host node. Note the IP address, as well as the Public    Key output from your Host node as you will need to configure your radio unit and register on-chain.  

*Radio Unit Hardware Setup*
  Setup your radio in meatspace.

* Refer to your manufacturer's instructions for installation and mounting.
* Configure the radio unit's EPC/CN address to be that of the Host Node.


*Semaphore Host Registration*
  Using the public key output from the middleware in the previous step, register your host in the Semaphore Network Host DAO by using the DApp at
  
  https://app.semaphore.network/host



Becoming a Semahpore Network User
=================================

You can use the Semaphore Network as a user on both cellular (LTE/5G) and WiFi (soon) protocols. 

Using the Semaphore Network Cellular Service:
To become a Semaphore network subscriber you will need to use the Subscriber DApp to 

Requirements:
Obtaining or creating a Semaphore Network ETHSim; this will serve as a hardware wallet and contains the authentication keys that will subscribers on the network

