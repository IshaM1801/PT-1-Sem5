Sliding Window Protocols
The Sliding Window Protocol is a method of flow control in which a sender can transmit several frames before getting an acknowledgement. Multiple frames can be sent one after another, due to which the capacity of the communication channel can be utilized efficiently.
A sending window refers to the sequence numbers of frames that have been sent but not yet acknowledged. A receiving window refers to the sequence numbers of frames the receiver can accept.
When an acknowledgement (ACK) for a frame is received, the lower edge of the window advances by 1. When a new frame is sent, the upper edge advances by 1.
a) One-bit – Stop and Wait
Sender’s Window Size (Ws): 1
Receiver’s Window Size (Wr): 1
Sender transmits one frame and waits for its ACK before sending the next frame.
Window size is 1, hence this is also known as Stop-and-Wait.
Sequence numbers are modulo 2 (0 and 1).
Both ends act as sender and receiver.
The acknowledgement number indicates the last frame received without error.
Drawback: Inefficient – sender waits until an ACK arrives from the receiver, so only one frame is sent at a time.
b) Go-Back–N (GBN)
Sender’s Window Size (Ws): N
Receiver’s Window Size (Wr): 1
Sender can send multiple frames (up to N) without receiving an ACK.
Uses cumulative acknowledgements – an ACK for frame k means all frames up to k have been received correctly.
If a frame in the middle of the window is lost or damaged, the receiver discards it and all subsequent frames, sending no ACKs for them.
The sender must go back and retransmit that frame and all following unacknowledged frames.
Sequence Number Requirement: Minimum sequence number space is N+1 to avoid confusion between old and new frames.
Justification of Window Sizes:
Ws = N to enable pipelining and keep the channel busy.
Wr = 1 because receiver cannot accept out-of-order frames; ensures in-order delivery.
Efficiency Formula:
diag1
​
.
c) Selective Repeat (SR)
Sender’s Window Size (Ws): N
Receiver’s Window Size (Wr): N
Sender can transmit new packets as long as they are within the window of unacknowledged packets.
Receiver accepts and stores correct packets even if they arrive out of order, and delivers them in sequence to the higher layer.
Acknowledgements are sent for all correctly received packets, and only erroneous or lost frames are retransmitted.
Sequence Number Requirement:
Window size must be ≤ half the sequence number space (2^m / 2).
This prevents the receiver from mistaking new frames for retransmissions if an ACK is lost.
Justification of Window Sizes:
Ws = N, Wr = N allows for maximum efficiency while supporting out-of-order reception.
Buffering at the receiver ensures fewer retransmissions and better channel utilization.
Efficiency Formula: Same as GBN:
Efficiency
diag2
​
