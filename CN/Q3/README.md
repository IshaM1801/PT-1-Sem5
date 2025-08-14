OSI reference model was developed by the International Organization for Standardization (ISO) in 1984, and it is now considered as an architectural model for the inter-computer communications.

• The Open System Interconnection Reference Model (OSI Reference Model or OSI Model) is an abstract description for layered communications and computer network protocol design.
• It divides network architecture into seven layers which, from top to bottom, are the Application, Presentation, Session, Transport, Network, Data Link, and Physical Layers. It is therefore often referred to as the OSI Seven Layer Model.
• The benefits of the layered models are modularity and clear interfaces
• In reality, no data are directly transferred from layer n on one machine to layer n
on another machine.
• Instead, each layer passes data and control information to the layer immediately
below it, until the lowest layer is reached.
• Below layer 1 is the physical medium through which actual communication
occurs.
• Virtual communication is shown by dotted lines and physical communication by
solid lines.

The principles that were applied to arrive at the seven layers can be briefly
summarized as follows:

1. A layer should be created where a different abstraction is needed.
2. Each layer should perform a well-defined function.
3. The function of each layer should be chosen with an eye toward defining internationally
   standardized protocols.
4. The layer boundaries should be chosen to minimize the information flow across the interfaces.
5. The number of layers should be large enough that distinct functions need not be thrown together in
   the same layer out of necessity and small enough that the architecture does not become unwieldy.

------Fig 1-32 diagram

• Each layer adds (or encapsulates) some form of header or trailer. (Layer 2, the
Data Link layer, is responsible for adding a trailer) as the data flow from Device A
to Device B.
• When the end system receives the unstructured bit stream from the physical wire,
each layer removes the header information applicable to it until the application
receives the data.
• Eg: An email is sent from Device A to Device B 1. An application, such as an email program, creates data that will be sent by an end
user, such as an email message. The Application layer (layer 7) places a header
(encapsulation) field that contains information such as screen size and fonts,
and passes the data to the Presentation layer (layer 6).
How Data Flows through the OSI Layers 2. The Presentation layer places layer 6 header information(PH) and will then pass
the new data to the Session layer (layer 5). 3. The Session layer follows the same process by adding layer 5 header
information(SH).
4.The Transport layer places layer 4 information in the header(TH), and passes it to
the Network layer (layer 3). 5. The Network layer places layer 3 header information(NH), such as the source and
destination address so the Network layer can determine the best delivery path for
the packets, and passes this data to the Data Link layer (layer 2). 6. The Data Link layer places layer 2 header(DH) and trailer information(DT) such as a
Frame Check Sequence (FCS) to ensure that the information is not corrupt, and passes
this new data to the Physical layer (layer 1) for transmission across the media. 7. The bit stream is then transmitted as ones and zeros on the Physical layer. 8. Steps 1 through 7 occur in reverse order on the destination device. Device B collects the
raw bits from the physical wire and passes them up the Data Link layer. The Data Link
layer removes the headers and trailers and passes the remaining information to the
Network layer and so forth until data is received by the Application layer. Eventually,
Device B will receive an email notification displaying a message to indicate that a new
email message has been received.
-----diagram.png(attached in this folder)
