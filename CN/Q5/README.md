## **Interconnection Networking Devices**

### **1. Repeater**

- **Layer**: Physical Layer
- **Working**: A repeater operates at the physical layer. Its job is to regenerate the signal over the same network before the signal becomes too weak or corrupted so as to extend the length to which the signal can be transmitted over the same network. Repeaters do not amplify the signal.

**Diagram:**

```
Device A ----(weak signal)----[Repeater]----(regenerated signal)---- Device B
```

---

### **2. Hub**

- **Layer**: Physical Layer (multiport repeater)
- **Working**: A hub is basically a multiport repeater. A signal received at any port on the hub is retransmitted on all other ports. It cannot filter data, and data packets are sent to all connected devices. No intelligence to find best path, leading to inefficiencies and wastage.
- **Types**: Active hub, Passive hub, Intelligent hub.

**Diagram:**

```
       [Hub]
      /  |  \
    PC1 PC2 PC3
```

---

### **3. Bridge**

- **Layer**: Data Link Layer
- **Working**: Connects two or more LAN segments of the same type. It reads the addresses of source and destination and filters content. Bridges learn device locations and forward traffic only where needed.
- **Types**: Transparent Bridge, Source Routing Bridge.

**Diagram:**

```
LAN1 --[Bridge]-- LAN2
```

---

### **4. Switch**

- **Layer**: Data Link Layer
- **Working**: Like a bridge but with multiple ports. Performs error checking before forwarding and sends data selectively to correct devices.
- **Types**: Store-and-forward, Cut-through.

**Diagram:**

```
     [Switch]
    /  |  |  \
 PC1 PC2 PC3 PC4
```

---

### **5. Router**

- **Layer**: Network Layer
- **Working**: Routes data packets based on IP addresses. Makes intelligent decisions about the best path for delivery. Connects LANs and WANs, maintains routing tables.
- **Types**: Static, Dynamic.

**Diagram:**

```
LAN --[Router]-- WAN
```

---

### **6. Brouter**

- **Layer**: Network Layer or Data Link Layer
- **Working**: Combines features of both bridge and router. Routes packets across networks or filters LAN traffic.

---

### **7. Gateway**

- **Layer**: All layers (depends on implementation)
- **Working**: Connects two networks using different protocols. Acts as a “gate” between networks.

---

### **8. Modem**

- **Layer**: Physical Layer (conversion function)
- **Working**: Converts analog signals from telephone/cable to digital data and vice versa.

---

### **9. Firewall**

- **Layer**: Can operate at multiple layers depending on type
- **Working**: Security device filtering traffic, blocking unauthorized access, protecting private data.

---

check diagrams from the ppt attached to the folder.
