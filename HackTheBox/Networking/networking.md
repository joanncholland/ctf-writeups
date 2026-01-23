# Key Networking Concepts

TCP vs UDP

Ports & services

Why scanning works

## Networking Structure

### Network Types

Four common network types:

| Network Type                         | Definition                                                                                                                                                    |
| ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Wide Area Network (WAN)              | A large number of LANs joined together i.e. the Internet                                                                                                      |
| Local Area Network (LAN)             | Internal networks (i.e. home or office)                                                                                                                       |
| Wireless Local Area Network (WLAN)   | Internal networks accessible over Wi-Fi                                                                                                                       |
| Virtual Private Network (VPN)        | Connects multiple network sites to one LAN                                                                                                                    |
| Global Area Network (GAN)            | Global network bigger than WANs, use glass fibers of WANs and interconnect them via international undersea cables or satellite transmission i.e. the Internet |
| Metropolitan Area Network (MAN)      | Regional network that connects several LANs in geographical proximity i.e. multiple LANs                                                                      |
| Wireless Pesonal Area Network (WPAN) | Personal network i.e. bluetooth                                                                                                                               |

There are three main types of VPN, but all three of the same goal of making the user feel as if they were plugged into a different network.

1. **Site-to-Site VPN** - both the client and the server are network devices, typically routers or firewalls, and share entire network ranges. i.e. joining company networks together over the Internet
2. **Remote Access VPN** - involves the client's computer creating a virtual interface that behaves as if it were on the client's network.
3. **SSL VPN** - a VPN that is done within our web browser, typically used for streaming applications or desktop sessions to the browser.

### Networking Topologies

We can divide the network topology area into three areas:

#### 1. Connections

| Wired connections    | Wireless connections |
| -------------------- | -------------------- |
| Coaxial cabling      | Wi-Fi                |
| Glass fiber cabling  | Cellular             |
| Twisted-pair cabling | Satellite            |
| and others           | and others           |

#### 2. Nodes - Network Interface Controller (NICs)

Network nodes are the transmission medium's connection points to transmitters and receivers of electrical, optical, or radio signals in the medium. A node may be connected to a computre, but certain types may have only one microcontroller on a node or may have no programmable device at all.

NICs typically consists of the following:

- Repeaters
- Hubs
- Bridges
- Switches
- Router/Modem
- Gateways
- Firewalls

#### 3. Classifications

These are the types of topologies and can be either physical or logical. Network topologies are divided into the following eight basic types:

1.  Point-to-point
2.  Star
3.  Mesh
4.  Hybrid
5.  Bus
6.  Ring
7.  Tree
8.  Daisy chain

More complex networks can be built as hybrids of two or more of the basic topologies mentioned above.

| Network topology | Description                                                                                                                                                                                                          | Example                                                                                                                                             |
| ---------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| Point-to-Point   | Simplest network topology with a dedicated connection between two hosts.                                                                                                                                             | ![Point-to-point topology showing two hosts connected](./Screenshots/point-to-point.png)                                                            |
| Bus              | All hosts are connected via a transmission medium, there is no central network component that controls processes on it.                                                                                              | ![Bus topology showing 6 hosts all interconnected](./Screenshots/bus.png)                                                                           |
| Star             | Each host is connected to the central network component via a separate link, usually a router, switch, or hub, that handle the forwarding fundtion for data packets                                                  | ![Star topology with four hosts connected to a router](./Screenshots/star.png)                                                                      |
| Ring             | Each host or node is connected to the ring with two cables: one for incoming signals and one for outgoing signals, transmitted in a predetermined direction                                                          | ![Ring topology with four hosts connected in a ring shape](./Screenshots/ring.png)                                                                  |
| Mesh             | There are two basic structures, fully meshed and partially meshed. Fully meshed networks are where every component or device is connected to each other and partially meshed is where only some are connected.       | ![Partial mesh topology with 4 hosts and 4 routers, some of which are connected](./Screenshots/mesh.png)                                            |
| Tree             | Extended star topology that has more extensive local networks, often used in larger company buildings.                                                                                                               | ![Tree topology showing one server, with two ethernet switches attached, and three hosts connected to each ethernet switch](./Screenshots/tree.png) |
| Hybrid           | Combines two or more topologies so that the resulting network does not represent any standard topologies, i.e. a tree network can represent a hybrid topology in which start networks are connected via bus networks | ![Hybrid topology with three routers interconnected, and two hosts connect to each router](./Screenshots/hybrid.png)                                |
| Daisy chain      | Multiple hosts are connected by placing a cable from one node to another, creating a chain of connections                                                                                                            | ![Daisy chain topology showing five hosts connected in a daisy chain](./Screenshots/daisy-chain.png)                                                |

### Proxies

A proxy is when a device or service sits in the middle of a connection and acts as a mediator. The mediator is the critical piece of information because it means he device in the middle must be able to inspect the contents of the traffic. VPNs are not the same as proxies.

Proxies almost always operate at Layer 7 of the OSI Model. There are many types of proxies, but key ones are:

- Dedicated proxy / forward proxy
- Reverse proxy
- Transparent proxy

#### Dedicated/Forward Proxy

A forward proxy is when a client makes a request to a computer and that computer carries out the request with the proxy in between. i.e. in a corporate network, sensitive computers may need to go through a proxy filter before reaching the Internet to defend against malware.

![Dedicated/forward proxy showing two hosts performing a HTTP request that goes through the forward proxy first before reaching the Internet](./Screenshots/dedicated-forward-proxy.png)

#### Reverse Proxy

Instead of filtering outgoing requests, it filters incoming requests. The most common goal with a reverse proxy is to listen on an address and forward it to a closed-off network. i.e. filtering the amount and type of traffic that gets sent to their webservers.

![Reverse proxy between the Internet and the webserver](./Screenshots/reverse-proxy.png)

#### (Non-)Transparent Proxy

All these proxy services act either transparently or non-transparently.

With a transparent proxy, the client doesn't know about its existence, it intercepts the client's communication requests to the Internet and acts as a substitute instance.

With a non-transparent proxy, we're informed about its existence.

## Networking Models

Two networking models describe the communication and transfer of data from one host to another, called ISO/OSI model and the TCP/IP model.

![Side-by-side diagram of the OSI/TCP models](./Screenshots/osi-tcp-model.png)

### The OSI Model

The OSI (Open Systems Interconnection) model is a reference model that can be used to describe and define the communication between systems, and has seven individual layers each with clearly separated tasks.

| Layer           | Description                                                                                                                                                                                          |
| --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 7. Application  | Among other things, thhis layer controls the input and output of data and provides the application functions.                                                                                        |
| 6. Presentation | Task is to transfer the system-dependent presentation of data into a form independent of the application.                                                                                            |
| 5. Session      | Controls the logical connection between two systems and prevents, for example, connection breakdowns or other problems.                                                                              |
| 4. Transport    | Used for end-to-end control of the transferred data, can detect and avoid congestion situations and segment data streams.                                                                            |
| 3. Network      | Connections are established in circuit-switched networs, and data packets are forwarded in packet-switched networks. Data is transmitted over the entire network from the sender to the receiver.    |
| 2. Data Link    | Central task is to enable reliable and error-free transmissions on the respective medium, for this purpose bitstreams from layer 1 are divided into blocks or frames.                                |
| 1. Physical     | Transmission techniques used are, for example, electrical signals, optical signals, or electromagnetic waves. Through layer 1, the transmission takes place on wired or wireless transmission lines. |

### The TCP/IP Model

TCP/IP (Transmission Control Protocol/Internet Protocol) is a generic term for many network protocols responsible for switching and transporting data packets on the Internet.

| Layer          | Description                                                                                                                                                                                                                    |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 4. Application | Allows applications to access the other layers' services and defines the protocols applciations use to exchange data.                                                                                                          |
| 3. Transport   | Responsible for providing (TCP) sessions and (UDP) diagram services for the Application Layer.                                                                                                                                 |
| 2. Internet    | Responsible for host addressing, packaging, and routing functions.                                                                                                                                                             |
| 1. Link        | Responsible for placing the TCP/IP packets on the network medium and receiving corresponding packets from the network medium. TCP/IP is designed to work independently of the network access method, frame format, and medium. |

The most important tasks of TCP/IP are:

- **Logical Addressing (IP protocol):** IP takes over logical addressing of networks and nodes. Data packets only reach the network where they are supposed to be, and the methods to do so are network classes, subnetting, and CIDR.
- **Routing (IP protocol):** For each data packet, the next node is determined in each node on the way from the sender to the receiver. This way, a data packet is routed to its receiver, even if its location is unknown to the sender.
- **Error & Control Flow (TCP protocol):** Sender and receiver are frequently in touch with each other via a virtual connection, therefore control messages are sent continuously to check if the connection is still established.
- **Application Support (TCP protocol):** TCP and UDP ports form a software abstraction to distinguish specific applciations and their communication links.
- **Name Resolution (DNS protocol):** Provides name resolution through Fully Qualified Domain Names (FQDN) in IP addresses, enabling us to reach the desired host with the specified name on the Internet.

### Packet Transfers

In a layered system, devices in a layer exchange data in a different format called a protocol data unit (PDU). Durig the transmission, each layer adds a header to the PDU from the upper layer, which controls and identifies the packet. This process is called encapsulation, and the header and the data together form the PDU for the next layer.

![Packet transfer at each layer](./Screenshots/packet-transfer.png)
