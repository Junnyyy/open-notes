# <u>Chapter 1</u>
### Overview: 
* What is the Internet?
* What is a protocol?
* **Network edge**: hosts, access network, physical media 
* **Network core**: packet/circuit switching, internet structure
* **Performance**: loss, delay, throughput
* Security
* Protocol layers, service models
* History

## <u>The Internet</u>
**The Internet** - billions of connected devices.
* **hosts** are end systems
* running network apps at internet edge
**Packet switches** - forward packets (chunk of data)
* router, switches
**Communication links**:
* fiber, copper, radio, satellite
* transmission rate: bandwidth
**Networks**: 
* collection of devices, routers and links that may be managed by an organization. 

Any time you have an app that knows how to *build a packet* and *send* it to an *electrical interface* which *transmits it* via any transmission medium (wired, wireless, 5G, etc). Then you have an **Internet capable program**

**The Internet** is the network of networks, it's the connection of various ISPs (Internet Service Providers). 

| The Nuts and Bolts View                                                                  | Services                                                 |
|------------------------------------------------------------------------------------------|----------------------------------------------------------|
| Internet is a network of networks.                                                       | Infrastructure that provides services.                   |
|  Protocols are ubiquitous, sending and receiving messages.                               | Programming Interfaces such as hooks and service options |
| Internet Standards: RFC -- Request for Comments  IETF -- Internet Engineering Task Force |                                                          |

###<u>What are Protocols</u>
![[Pasted image 20230125194231.png]]
##### **Protocols** are everywhere:
* control sending, receiving of messages
* HTTP, streaming services, VOIPs, wifi, ethernet
##### You can think of Human Protocols: 
* "What's the time"
* "I have a question"
* Introductions
##### Network Protocols:
* Computers (devices) rather than humans
* all communication activity in Internet governed by protocols
![[Pasted image 20230125194516.png]]
💡Protocols define the ***format***, ***order*** of messages sent and received among network   entities, and actions taken on message transmission receipt.

### <u>Network Edge:</u>
**Hosts:** clients and servers
**Servers** often in data centers

### <u>Access networks, physical media:</u>
Wired, wireless communication links.

### <u>Network Core:</u>
Interconnected routers
Network of networks

## <u>Access networks and physical media</u>
Residential access nets, institutional access networks, and mobile access networks (WiFi, 4G, 5G) are all examples of how to connect end systems to edge routers
#### <u>Cable-based access</u>
***frequency division multiplexing (FDM):*** different channels transmitted in different frequency bands.
***HFC: hybrid fiber coax:***
* Asymmetric: up to 40 Mbps -- 1.2 Gbs downstream transmission rate, 30-100 Mbps upstream transmission rate
***Network of cable:***
* fiber attaches buildings to ISP routers
* Homes share access network to cable headend.
![[Pasted image 20230125195211.png]]

***Digital Subscriber Line (DSL):***
* use ***existing*** telephone line to central office DSLAM.
* 24-52 Mbps dedicated downstream transmsision rate.
* 3.5-16 Mbps dedicated upstream transmission rate.
![[Pasted image 20230125195738.png]]

***Home Networks:***
* Wireless devices, routers, ethernet cables, DSL modem, WiFi

### Wireless Access Networks 
Shared ***wireless access network*** connects end system to router
* via base station aka "access point"
Wireless local area networks (WLANs):
* typically within or around building
* 802.11b/g/n (WiFi): 11, 54, 450 Mbps transmission rate

| Wireless Local Area Networks (WLANs)                   | Wide-Area Cellular Access Networks    |
|--------------------------------------------------------|---------------------------------------|
| typically within or around building                    | Provided by mobile network operators  |
| 802.11b/g/n (WiFi): 11, 54, 450 Mbps transmission rate | 10's Mbps, 4G, 5G                     |
|                                                        |                                       |

#### <u>Enterprise networks</u>
* Companies, Universities and other organizations
* Mix of wired, wireless link technologies, connecting a mix of switches and router
	* Ethernet: wired access at 100Mbps, 1 Gbps, 10 Gbps
	* WiFi: wireless access points at 11, 54, 450 Mbps

### Host: Send *Packets* of data
Host sending function:
* takes application message
* breaks into smaller blocks of data called ***packets***
* transmits packet into access network at transmission rate R
* link transmission rate or link capacity, or link bandwidth

![[Pasted image 20230125201212.png]]

### Links: Physical media
* ***bit***: propogates between transmitter/receiver pairs
* ***physical link***: what lies between transmitter & receiver
* ***guided media***: signals propagate in solid media
* ***unguided media***: signals propagate freely, e.g. radio
##### Twisted Pair (TP) 
* two insulated copper wires
	* Category 5: 100 Mbps, 1 Gbps Ethernet
	* Category 6: 10 Gbps Ethernet

### Links: Physical media
***Coaxial cable***:
* two concentric copper conductors
* bidirectional 
* broadband
	* multiple frequency channels on cable
	* 100's Mbps per channel
***Fiber Optic cable***:
* carries light pulses, each pulse is a bit
* high-speed point to point transmission
* low error rate:
	* repeaters spaced far apart
	* immune to electromagnetic noise
***Wireless radio***:
* signal carried in electromagnetic spectrum
* <b><u>no</u></b> phsyical wiring
* broadcast (sender to receiver)
* propagation environment effects:
	* reflection
	* obstructon by objects
	* interference
***Radio link types:***
* terrestrial microwave
	* Up to 45 Mbps channels
* Wireless LAN **(WiFi)**
	* Up to 100's Mbps
* Wide-area (e.g. cellular)
	* 4G cellular
* Satellite
	* Up to 45 Mbps per channel
	* 270 msec end-end delay
	* geosynchronous versus low-earth orbit
## The network core
Mesh of interconnected routers
***Packet-switching***: hosts break application-layer messages into packets
* forward packets from one router to the next, across links on path from source to destination.
* each packet transmitted at full link capacity.

### Packet-switching: store and forward
![[Pasted image 20230126093502.png]]![[Pasted image 20230126093524.png]]
***Transmission delay***: takes L/R seconds to transmit (push out) L-bit packet into link at R bps
***Store and forward***: entire packet must arrive at router before it can be transmitted on next link
***End-end delay***: 2L/R (above), assuming zero propagation delay (mroe on delay shortly)

