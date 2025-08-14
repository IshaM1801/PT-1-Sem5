Stop-and-Wait Protocols
Flow control is one of the most important functions of the data link layer. The receiver has a limited speed at which it can process incoming data and a limited amount of memory in which to store incoming data. The receiver must inform the sender before the limits are reached and request the transmitter to send fewer frames or stop temporarily. Flow control coordinates the amount of data that can be sent before receiving acknowledgement.
The Stop-and-Wait mechanism is a basic flow control method. It is implemented in the following three types of protocols:

1. An Unrestricted Simplex Protocol (Utopia) [Protocol 1]
   Data are transmitted in one direction only (unidirectional).
   The transmitting (Tx) and receiving (Rx) hosts are always ready.
   Infinite buffer space is available.
   No errors occur – no damaged or lost frames (perfect channel).
   The sender is in an infinite loop, pumping data out onto the line as fast as possible.
   The receiver can never be overwhelmed with incoming frames.
   Working:
   The sender continuously fetches a packet from the network layer, constructs an outbound frame, and sends it. Only the info field of the frame is used because error and flow control are unnecessary here. The receiver simply waits for an undamaged frame, passes it to the network layer, and waits for the next one.
2. A Simplex Stop-and-Wait Protocol [Protocol 2]
   Data transmission in one direction only.
   No errors occur (perfect channel).
   The receiver can process data at a finite rate.
   Problem:
   The transmitter cannot send frames faster than the receiver can process them. Without control, the sender could flood the receiver.
   Solution:
   The receiver sends an acknowledgement (ACK) frame after processing each received frame. The sender must wait for this ACK before sending the next frame. This guarantees that the receiver is never overloaded.
   Advantages:
   Simple – each frame is checked and acknowledged before sending the next.
   Disadvantages:
   Inefficient – each frame must travel the entire link before the next is sent.
   Poor utilization of bandwidth – round trip time delays transmission.
3. A Simplex Protocol for a Noisy Channel [Protocol 3]
   The error-free assumption of Protocol 2 is dropped. Frames may be damaged or lost.
   Working:
   The sender transmits a frame.
   The receiver sends an ACK only if the frame is received correctly.
   If a frame is damaged, the receiver ignores it; the sender times out and retransmits it.
   Problem:
   If an ACK is lost or damaged, the sender retransmits the frame, and the receiver may accept it as new, creating duplicates.
   Solution:
   To distinguish new frames from retransmissions, the sender adds a sequence number in the frame header.
   Only a 1-bit sequence number is needed (0 or 1) to differentiate between new and duplicate frames.
   The receiver expects a specific sequence number; wrong ones are discarded.
   Correctly numbered frames are accepted, passed to the host, and the expected sequence number is toggled.
   Drawbacks of Stop-and-Wait (Protocols 2 and 3):
   Very inefficient – only one frame is in transit at any moment.
   The sender waits at least one round trip time before sending the next frame.
   Poor utilization of bandwidth.
   Poor performance in high-latency links.
