Design Issues for the Layers
When designing the layers of a network architecture, certain issues must be addressed to ensure smooth, reliable, and efficient communication between devices. Each layer in the model has its own responsibilities, but there are some general design issues that apply to many or all layers.
The important design issues for the layers are as follows:

1. Addressing
   Each layer needs a way to identify both the sender and the receiver so that the data can be delivered correctly.
   At the physical and data link layers, this might be done using MAC addresses.
   At the network layer, IP addresses are used to uniquely identify devices.
   At higher layers, such as the transport layer, port numbers are used to identify specific processes or applications.
   Without proper addressing, there would be no way to ensure that information reaches the intended destination.
2. Data Transmission Direction
   A layer must know in which direction the data will flow between two communicating devices. This is referred to as data transmission mode, and it can be:
   Simplex: Data flows in only one direction.
   Half-Duplex: Data flows in both directions, but only one way at a time.
   Full-Duplex: Data flows in both directions simultaneously.
   The chosen mode affects the efficiency of communication and the design of protocols in that layer.
3. Error Control
   During transmission, data can be corrupted due to noise, interference, or other issues. Error control involves detecting and correcting such errors.
   Error detection ensures the receiver can identify if a packet is damaged.
   Error correction allows the receiver to reconstruct the original data.
   Protocols such as TCP include built-in error control mechanisms, while lower layers may use parity bits, checksums, or cyclic redundancy checks (CRC).
4. Flow Control
   If a sender is faster than the receiver, the receiver’s buffer can overflow, causing data loss. Flow control prevents this by matching the sender’s rate with the receiver’s processing capability.
   This can be implemented using sliding window protocols or acknowledgement schemes.
   Flow control ensures efficient data exchange without overloading network resources.
5. Sequencing of Data
   When large messages are divided into smaller packets, they may take different routes in the network and arrive out of order at the destination.
   Sequencing ensures that these packets are reassembled in the correct order.
   Protocols like TCP use sequence numbers to reorder data correctly before delivering it to the application.
6. Multiplexing and Demultiplexing
   A single physical link may carry data for multiple communication sessions.
   Multiplexing combines multiple signals for transmission over a single channel.
   Demultiplexing separates them at the receiving end so each application gets the correct data.
   This allows more efficient use of network resources and supports multiple applications at the same time.
7. Routing
   When data must travel across multiple networks, routing determines the best path from source to destination.
   Routing decisions may be based on shortest path, least congestion, or cost efficiency.
   Routing protocols, such as RIP, OSPF, and BGP, are responsible for maintaining routing tables and updating them dynamically.
