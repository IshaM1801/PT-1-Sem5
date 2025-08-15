OSI Layered Structure and Its Functions
The OSI (Open Systems Interconnection) reference model is a conceptual framework that standardizes the functions of a telecommunication or computing system into seven abstraction layers. It was developed by ISO to facilitate interoperability between heterogeneous systems without requiring changes to the underlying hardware and software.
The OSI model divides the whole network communication process into seven layers, each having its own specific functions and responsibilities. These layers are:

1. Physical Layer
   Deals with physical connection between devices.
   Functions:
   Transmission of raw bits over a physical medium.
   Defines characteristics such as voltage levels, timing of voltage changes, physical data rates, maximum transmission distances, and physical connectors.
   Concerned with bit representation, data rate, physical topology, and transmission mode.
2. Data Link Layer
   Responsible for node-to-node delivery of frames.
   Functions:
   Framing: Organizes raw bits from physical layer into frames.
   Physical addressing: Adds sender and receiver MAC addresses.
   Error detection and correction.
   Flow control.
   Access control for shared media.
3. Network Layer
   Responsible for source-to-destination delivery of packets, across multiple networks.
   Functions:
   Logical addressing (IP addresses).
   Routing: Determines the best path for data.
   Packet forwarding, fragmentation, and reassembly.
   Internetworking and congestion control.
4. Transport Layer
   Ensures process-to-process delivery of complete messages.
   Functions:
   Segmentation and reassembly of data.
   Error detection and recovery.
   Flow control.
   Connection establishment and release.
   Protocols: TCP (connection-oriented), UDP (connectionless).
5. Session Layer
   Manages and controls the dialog between two systems.
   Functions:
   Establishing, maintaining, and terminating sessions.
   Dialog control (half-duplex or full-duplex).
   Synchronization using checkpoints.
   Recovery from failures.
6. Presentation Layer
   Responsible for data translation, encryption, and compression.
   Functions:
   Translation between application and network formats.
   Data encryption and decryption for security.
   Data compression to reduce bandwidth usage.
7. Application Layer
   Closest to the end user; provides network services to applications.
   Functions:
   Network virtual terminal.
   File transfer, access, and management (FTP).
   Email services (SMTP).
   Directory services, remote login, and web services.
   Advantages of OSI Model:
   Standardization of networking functions.
   Interoperability between heterogeneous systems.
   Modular engineering – each layer is independent.
   Simplifies learning, troubleshooting, and development.
