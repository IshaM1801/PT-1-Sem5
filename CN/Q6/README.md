Network Topologies
Definition:
The term physical topology refers to the way in which a network is laid out physically. Two or more devices connect to a link; two or more links form a topology.
The pattern of interconnection of nodes in a network is called the TOPOLOGY.
Factors to be considered for selection of the choice of topology:
Cost – minimize installation cost.
Flexibility – allow easy reconfiguration of the network.
Reliability – help in fault location and isolation.
Ease of installation.
Ease of maintenance.
Cable fault tolerance.

1. Bus Topology
   Description: One long cable that links all nodes; tap, drop line, cable end.
   Limitations: Limit on the number of devices, distance between nodes.
   Advantages: Easy installation, cheap.
   Disadvantages: Difficult reconfiguration, no fault isolation, a fault or break in the bus stops all transmission.
   Advantages of the Linear Topology:
   Short cable length and simple wiring layout → decreases installation cost, easy maintenance.
   Easy to extend → additional nodes can be connected anywhere; segments can be added via repeaters.
   Disadvantages:
   Fault diagnosis is difficult.
   Fault isolation is difficult.
   Nodes must be intelligent to decide transmission timing.
   Main cable/bus break can disable the entire network.
2. Star Topology
   Description: Dedicated point-to-point link to a central controller (hub). Hub acts as an exchange; no direct traffic between devices.
   Advantages: Less expensive, robust.
   Disadvantages: Dependency on hub – if hub fails, network stops.
   Advantages of Star Topology:
   Ease of service and reconfiguration.
   One device per connection – failure affects only that device.
   Centralized control and easy fault diagnosis.
   Simple access protocols.
   Disadvantages:
   Long cable length required.
   Central node dependency – failure disables network.
3. Ring Topology
   Description: Each node connected to two neighbours; data travels in one direction around the ring and returns to sender.
   Advantages: Easy reconfiguration, fault isolation, short cable length.
   Disadvantages:
   Each packet must pass through all computers between source and destination → slower than star.
   Failure of one workstation or port affects the whole network.
4. Mesh Topology
   Description: Dedicated point-to-point link to every other node.
   Full Mesh: Each computer connected to all others.
   Partial Mesh: Some computers connected only to frequently used partners.
   Formula: Number of cables = (n\*(n-1))/2.
   Advantages:
   Reliable – link failure does not affect overall communication.
   Fast communication.
   Adding devices does not disrupt network.
   Disadvantages:
   Cost – many devices, cables, and ports required.
   Efficiency – redundant connections reduce efficiency.
5. Hybrid Topology
   Description: Combines two or more topologies.
   Example: Main star topology with branches connected in bus topology.
   Purpose: Share advantages from multiple topologies.
