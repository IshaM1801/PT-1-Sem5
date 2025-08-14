**Explain the following layered structure along with its functions: TCP/IP**

---

**Ans:**

1. TCP/IP Stands for Transmission Control protocol (TCP) and the Internet Protocol (IP).
2. TCP/IP defines how the data should be processed, transmitted and received on a TCP/IP Network.
3. TCP/IP describe the movement of data between the host computers on Internet.
4. A system of related protocols, such as TCP/IP protocols is called as Protocol Suite.
5. There are four Layers in TCP/IP Protocol Suite.

---

**FEATURES OF TCP/IP:**

1. Logical Addressing.
2. Error Checking & Flow Checking.
3. Routing.
4. Application Support.

---

**TCP/IP PROTOCOL SUITE:**

**I) Host To Network Layer:**

> It is also called as Network Interface Layer.
> It is combination of Physical & Data Link Layer of OSI Model.
> TCP/IP Protocol Suite does not define any protocol at these layers.
> In this layer, hardware device reside and it provides support for standard protocols.

---

**II) Internet Layer:**

> IP is the primary protocol in network layer.
> The task of this layer is to deliver the datagram from source host to destination host.
> IP is unreliable and connectionless protocol.
> It provides best effort delivery service.
> It includes:

- **ICMP:**
  ♦ It stands for Internet Control Message Protocol.
  ♦ ICMP is a mechanism used by routers to send error or control message to other routers or hosts.

- **IGMP:**
  ♦ IGMP stands for Internet Group Message Protocol.
  ♦ It is used to manage IP Multicast data and enables transmission of messages to a group of recipient simultaneously.

- **ARP:**
  ♦ ARP stands for Address Resolution Protocol.
  ♦ It is used to convert logical (IP) address to physical address.

- **RARP:**
  ♦ ARP stands for Reverse Address Resolution Protocol.
  ♦ It is used to convert physical address to logical (IP) address.

---

**III) Transport Layer:**

> This is layer above the internet layer.
> Its functions are same as those of a transport layer in OSI Layer.
> It includes:

- **TCP:**
  ♦ It stand for Transmission Control Protocol.
  ♦ It is connection oriented and reliable protocol.
  ♦ It provides the function for reliable transmission of data across the network.
  ♦ It is used to handle error control & flow control.

- **UDP:**
  ♦ It stands for User Datagram Protocol.
  ♦ It is connection less and unreliable protocol.
  ♦ It takes the data from application layer then packages it into datagram and sends it to network layer.
  ♦ It does not provides error control and flow control.

- **SCTP:**
  ♦ It stands for Stream Control Transmission Protocol.
  ♦ It combines the good features of TCP & UDP.

---

**IV) Application Layer:**

> The layer on top of transport layer is called as Application Layer.
> The protocols related to this layer are all high level protocols.
> It includes:

- **SMTP:**
  ♦ It stands for Simple Mail Transfer Protocol.
  ♦ It is the protocol for sending E-Mail Message between servers.

- **SNMP:**
  ♦ It stands for Simple Network Management Protocol.
  ♦ It is the framework for managing the devices on the internet using TCP/IP Protocol Suite.

- **HTTP:**
  ♦ It stands for Hyper Text Transfer Protocol.
  ♦ It is used to access data on World Wide Web.

- **FTP:**
  ♦ It stands for File Transfer Protocol.
  ♦ It is used to exchange the files between computers on internet.

- **DNS:**
  ♦ Its stands for Domain Name System.
  ♦ It is used to identify the network and the computer on the network by some Domain Name instead of IP Address.

---
