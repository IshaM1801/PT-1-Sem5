# 🌐 Internet Protocols – Differentiation

---

## 🔹 What is a Protocol?

- A **protocol** is a detailed specification of how communication between two computers will be carried out.
- Defines both:

  - **High-level behavior** (software actions).
  - **Low-level details** (fields in a message, order, number of bits, interpretation).

- The Internet uses a **collection of protocols** that work together.
- Protocols differ in **scope, features, and reliability**.
- **Fundamental protocols**: IP, TCP, UDP.
- **Higher-level protocols** built on them: HTTP, FTP, SMTP, Telnet, DNS.

---

## 🖧 Internet Protocol (IP)

- Responsible for **delivering packets** from source to destination.
- Identifies systems using **IP addresses** (32-bit, e.g., `192.0.34.166`).
- Packages data into packets containing:

  - Source & destination addresses.
  - Data length.
  - Header information.

- If destination is **local** → sent directly.
- If **remote** → sent via one or more **gateways**.
- Provides **checksum** for error detection.
- **Unreliable and connectionless** → no guarantee of delivery.

---

## 🔗 Transmission Control Protocol (TCP)

- Works on top of IP to **add reliability**.
- Establishes **full-duplex connection** using a **three-way handshake**.
- Every packet is **acknowledged**.
- If acknowledgment not received → packet is **retransmitted**.
- Introduces the concept of **ports** (multiple apps can communicate independently).

  - Example: **SMTP uses port 25**.

- **Connection-oriented and reliable protocol**.

---

## 📦 User Datagram Protocol (UDP)

- Alternative to TCP, also works above IP.
- **No connection establishment**.
- **No guarantee of delivery** (unreliable).
- Retains the **port concept**.
- No acknowledgments or retransmissions → **faster communication**.
- Suitable for **small, quick exchanges** where occasional loss is tolerable.
- **Example:** DNS uses UDP because only two messages (request + reply) are needed.

---

## 🌍 Domain Name System (DNS)

- Not a **transport protocol** but an essential **Internet service**.
- Translates **human-readable names → IP addresses**.
- Can perform **reverse mapping** (IP → host name).
- Typically uses **UDP (port 53)** for efficiency.
- Uses **TCP for large data transfers**.
- **Distributed worldwide** → functions as the Internet’s **phonebook**.

---

## 📑 Higher-Level Protocols

- Built on top of TCP/UDP to provide services:

  - **HTTP (Hypertext Transfer Protocol)** → communication between browsers & servers (uses TCP).
  - **FTP (File Transfer Protocol)** → file transfer between systems (uses TCP).
  - **SMTP (Simple Mail Transfer Protocol)** → sending email between servers (uses TCP).
  - **Telnet** → remote login & command execution as if physically present (uses TCP).

---

## 📊 Comparison Table (Summary)

| Protocol   | Layer       | Features                                          | Reliability                   | Example Use             |
| ---------- | ----------- | ------------------------------------------------- | ----------------------------- | ----------------------- |
| **IP**     | Network     | Addressing & routing packets                      | Unreliable, connectionless    | Delivery of packets     |
| **TCP**    | Transport   | Connection, acknowledgment, retransmission, ports | Reliable, connection-oriented | HTTP, FTP, SMTP, Telnet |
| **UDP**    | Transport   | No connection, no acknowledgment, faster          | Unreliable, connectionless    | DNS, streaming          |
| **DNS**    | Application | Resolves hostnames ↔ IP addresses                 | Depends on UDP/TCP            | Web browsing            |
| **HTTP**   | Application | Browser–server communication                      | TCP-based                     | Websites                |
| **FTP**    | Application | File transfers                                    | TCP-based                     | Download/upload files   |
| **SMTP**   | Application | Email transfer                                    | TCP-based                     | Sending emails          |
| **Telnet** | Application | Remote login                                      | TCP-based                     | Remote server access    |

---
