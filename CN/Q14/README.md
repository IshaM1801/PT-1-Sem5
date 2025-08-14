Error Control Methods
Error control is a process in data communication that ensures the delivery of data from the source to the destination without any errors. Two important error detection methods are Cyclic Redundancy Check (CRC) and Checksum.
b. Cyclic Redundancy Check (CRC)
CRC or Cyclic Redundancy Check is a method of detecting errors in the communication channel.
Given a k-bit frame or message, the transmitter generates an n-bit sequence, known as the frame check sequence (FCS), so that the resulting frame consists of (k + n) bits.
Key Concepts:
Bit sequences are written as polynomials with coefficients 0 and 1.
A frame with k bits is considered as a polynomial of degree k−1.
The Data Link Layer protocol specifies a generator polynomial G(x), available on both sender and receiver side.
Degree of G(x) = n (number of bits in FCS).
Sender Side Steps:
Append n zeros to the end of the data (n = degree of G(x)).
Perform modulo-2 binary division of the augmented data by G(x).
Append the remainder to the original data to form the codeword and send it.
Receiver Side Steps:
Perform modulo-2 division of the received frame by G(x).
If the remainder is zero, there is no error; otherwise, an error is detected.
Example (Error-free):
Data = 100100, G(x) = 1101
Remainder = 000 → No error.
Example (Error detected):
Codeword sent: 100100001
Received: 100000001
Remainder ≠ 0 → Error detected.
Error Detection Capabilities:
Detects all single-bit errors.
Detects all double-bit errors.
Detects any odd number of errors.
Detects all burst errors of length ≤ degree of G(x).
A burst longer than r+1 bits is detected with probability
1-2^-r
Common Standards:
CRC-8, CRC-16, CRC-32, CRC-64.
c) Checksum
The Checksum method is another error detection scheme in which the data is divided into equal segments of n bits (often 16 or 32 bits).
Sender Side Steps:
Divide data into fixed-size segments.
Sum all segments using 1’s complement addition.
Take the 1’s complement of the sum; this becomes the checksum.
Send the data along with the checksum.
Receiver Side Steps:
Divide received data into segments.
Sum all segments including the checksum.
If the result is all 1’s, no error is detected; otherwise, error exists.
Example:
Data segments: 10101010, 11001100, 11110000
Sum = 1’s complement addition → checksum = 00101011
Receiver checks sum of all segments + checksum → should be all 1’s for no error.
Advantages:
Simple to implement.
Limitations:
Less powerful than CRC for detecting burst errors.
