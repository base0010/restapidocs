Hosting The Network
=================================

**What Is A Semaphore Network Host?**

A Semaphore Network Host is an individual, DAO or entity that deploys host node and radio hardware to help provide Semaphore Network's Universal Basic Internet "coverage" to subscribers. 

**What are the Prerequisites to Become a Host?**

Hosts need to provide three basic types of capital that will be utilized to provide dentralized internet services to Semaphore Network Subscribers.

Physical Space
  Hosts will need a physical place to put the radio units. While host nodes can stay inside or even be hosted remotely;
  Generally, radio units will need to be placed in an outdoor space high up and with the clearest Line-of-Sight to provide maximum efficienty for Subscribers. Physically, a 3ft^3 area is enough with extra for a multi-kilometer deployment.
Your physical space will also determine the legal requirements and regulations for radio emissions. Please comply with your local laws. 

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



Using The Network
=================================

This document will focus on how to subscribe the internet services provided by decentralized Semaphore Network Hosts. Subscribers will need two things to successfuly enjoy the network services. 

*User Equipment*
  Subscribers will need a device to use; users can bring their own COTS LTE/5G user equpiment; this can be any cellphone and modem user equipment      that supports LTE /5G

  * Currently the user equipment must have a physical [mini/nano] SIM-card slot to host the Semaphore USIM.
  * You should also confirm that your equipment has support for bands that local hosts provide service on.

*Semaphore USIM*
  Subscribers will also need to obtain or create their own Semaphore USIM to connect to the Network. You can buy one from us at                        https://shop.semaphore.network or bring your own compatible javacard and upload our CAP file.


**Setup**
______________________

*Phone/ User Equipment Setup*
  Generally speaking you shouldn't need to configure your phone or user equipment in any particular way as the majority of configuration details,       and authentication will be performed by the USIM 


*Semaphore USIM Setup*
  You can use an external card reader and the Subscriber Setup CLI to generate your Subscriber Authentication Keypair. The program will output the     result of this public key so that you can put it in the onchain registry. 

  In the future you can use the STK application inside your phone's menu to do this as well. 

*Registering Semaphore USIM On-Chain*
  The last step to subscribe to the network is to add your Subscriber Authentication Keypair to the on-chain registry. To do this visit

  * https://app.semaphore.network/subscribe


ETHSIM Security+
===============================

Semaphore Network leverages our unique ETHSIM wallet technology to enhance cellular radio link security and decentralize AAA (authentication, administration, and accounting) processes inside telco networks. Instead of relying on the traditional cellular network authentication system called MILENAGE, we introduce modern asymmetric PKI cryptography via ECDH with Ethereum-native cryptography (secp256k1 & altbn128).

Introduction
------------

Semaphore Network's approach to security and decentralization in telecommunications is rooted in addressing the limitations of the traditional AAA and MILENAGE framework. By implementing hardware wallet security and smart contracts, we ensure a secure, soverign and decentralized telecommunications environment, even on devices as simple as flip phones.

Challenges with Traditional Systems
------------------------------------

MILENAGE, the conventional cellular network authentication system, necessitates a carrier-owned centralized database where all private key material is stored. This centralized approach poses significant security risks, as it places the security of user data in the hands of a few large telecommunications companies, which are prone to exploitation.

Key Improvements
----------------

Semaphore Network addresses these challenges through several key improvements:

1. **Ownership of Private Keys**: We move the private key out of a centralized database and into a sovereign ETHSIM wallet owned by the user. This eliminates vulnerabilities associated with SIM swaps and eavesdropping.

2. **On-chain Subscriber Registry**: Subscriber public keys are stored on-chain in an immutable sovereign subscriber registry, similar to a telco HSS (Home Subscriber Server). This allows users to activate services, top-up their accounts with cryptocurrency, and perform other functions without the need for intermediaries, including potentially unreliable customer service.

3. **Global Roaming Subscribership**: By storing subscriber information on-chain, Semaphore Network ensures a truly global roaming subscribership, enhancing accessibility and connectivity for users worldwide.

Conclusion
----------

Semaphore Network's utilization of ETHSIM technology and innovative cryptographic techniques represents a significant advancement in the field of telecommunications security and decentralization. By addressing the limitations of traditional systems, we provide users with greater control over their data and a more secure telecommunications experience.

For more information, please refer to our `documentation <link_to_your_documentation_here>`_.

