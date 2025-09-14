# Computer Network

# Introduction (Part 1)
## Contents
- [Computer Network](#computer-network)
- [Introduction (Part 1)](#introduction-part-1)
  - [Contents](#contents)
  - [Introduction](#introduction)
    - [Human protocol vs. Network protocol](#human-protocol-vs-network-protocol)
  - [Access Networks](#access-networks)
    - [Bandwidth of Access Network](#bandwidth-of-access-network)
    - [Home Residential Access](#home-residential-access)
      - [Via Modem](#via-modem)
      - [Digital Subscriber Line (DSL)](#digital-subscriber-line-dsl)
      - [Hybrid Fiber-Coaxial (HFC)](#hybrid-fiber-coaxial-hfc)
      - [Fiber To The Home (FTTH)](#fiber-to-the-home-ftth)
      - [Satellite](#satellite)
    - [Enterprise Access Network (Ethernet)](#enterprise-access-network-ethernet)
    - [Wireless Access Network](#wireless-access-network)
  - [Physical Media](#physical-media)
    - [Twisted Pair](#twisted-pair)
    - [Coaxial Cable](#coaxial-cable)
    - [Fiber Optic Cable](#fiber-optic-cable)
    - [Radio](#radio)
  - [The network core](#the-network-core)
    - [Mesh of interconnected routers/packet switches](#mesh-of-interconnected-routerspacket-switches)
    - [Circuit Switching](#circuit-switching)
    - [Packet Switching](#packet-switching)
    - [Host sending function](#host-sending-function)
    - [Packet Switching](#packet-switching-1)
      - [Packet Transmission Delay](#packet-transmission-delay)
      - [Store and forward delay](#store-and-forward-delay)
      - [Question](#question)
    - [Types of delay in packet-switched networks](#types-of-delay-in-packet-switched-networks)
    - [Queuing delay and loss](#queuing-delay-and-loss)
      - [Queuing delays](#queuing-delays)
    - [Two key network-core functions](#two-key-network-core-functions)
    - [Circuit Switching](#circuit-switching-1)
      - [Frequency Division Multiplexing (FDM) VS Time Division Multiplexing (TDM)](#frequency-division-multiplexing-fdm-vs-time-division-multiplexing-tdm)
      - [Example](#example)
      - [Problem](#problem)
    - [Packet Switching vs Circuit Switching](#packet-switching-vs-circuit-switching)
  - [Internet structure](#internet-structure)
      - [How all ISP connected together?](#how-all-isp-connected-together)
  - [Internet](#internet)
    - [Network delays](#network-delays)
      - [Queuing delay-revisited](#queuing-delay-revisited)
      - [Packet Loss](#packet-loss)
      - [End-to-end delay](#end-to-end-delay)
    - [Throughput](#throughput)
      - [Bandwidth vs Throughput](#bandwidth-vs-throughput)
      - [Bottleneck throughput case](#bottleneck-throughput-case)
      - [Transfer time](#transfer-time)
  - [Network protocols](#network-protocols)
    - [Internet protocol stack (TCP/IP Model)](#internet-protocol-stack-tcpip-model)
    - [ISO/OSI reference model](#isoosi-reference-model)

## Introduction

**Packet**: It is like an envelope of a letter, it contains **payload** (information) and **header** (address of sender and receiver) and sometimes **trailer** (extra info for error detection).

These packets are sent over the internet or network. First, it is sent to **ISP (Internet Service Provider)** and it travels through ISP before going to destination.

So here:  
- **Packets** → Letter  
- **ISP** → Post office  

There are various services provided by ISP:  
- **Dialup**  
- **Broadband** (cable/DSL)  
- **High speed LAN access**  
- **Wireless Access**  
- **Internet access to content providers** (connecting websites directly to the Internet)  

Now while sending/receiving these packets, certain rules and regulations are to be followed called as **protocols** e.g., TCP, IP, HTTP.

Currently, the Internet does not provide a service that makes promises about:  
- How long it will take to deliver the data from sender to receiver  

### Human protocol vs. Network protocol

![Protocol](/images/protocol.png)

**Definition of protocol**: A set of rules and standards that define how data is formatted, transmitted, and received across a network.  
It ensures that two devices (computers, routers, etc.), possibly built by different manufacturers, can understand each other and communicate correctly.

**Example:**  
- **HTTP** → rules for web communication  
- **TCP** → rules for breaking data into packets and reassembling them reliably  
- **IP** → rules for addressing and routing packets  

---

## Access Networks

It is the infrastructure that connects a user to ISP. 

Some common types of access networks:  
- **Wired** → DSL, Cable, Fiber-optic, Ethernet  
- **Wireless** → Wi-Fi, 4G/5G, Satellite, WiMAX  

Here, red lines are the access network:  

![access network](/images/accessnetwork.png)

### Bandwidth of Access Network

**Definition**: Bandwidth of an access network means the maximum rate at which data can be transferred between the end user and the ISP’s core network.  

- Measured in bits per second (bps) — like Mbps (megabits per second) or Gbps (gigabits per second).  
- If you have a **100 Mbps broadband plan**, that’s basically the bandwidth of your access network.  
- Depends on technology (fiber offers more than DSL, 5G more than 3G).  
- It defines the **capacity**, not the actual speed (affected by congestion, latency, etc.).  
- Access networks are often the **bottleneck**, since backbone networks usually have much higher bandwidth.  

**Capacity vs. Actual Speed** → Bandwidth shows the maximum capacity of the access network, but the real speed can be lower due to congestion, latency, or interference.  

**Bottleneck** → Access networks usually have much less bandwidth than backbone networks, so they often become the limiting factor in a user’s internet speed.  

---

### Home Residential Access

- Via **modem**  
- **Broadband** access technologies:  
  - DSL  
  - HFC  
  - FTTH  
- **Satellite**  

#### Via Modem

Old way of connecting to the internet using the telephone network.  

- A **modem (modulator–demodulator)** converts digital signals from your computer into analog tones that can travel over phone lines, and vice versa.  
- Typical speeds were **56 Kbps or less** — very slow compared to DSL, cable, or fiber.  
- Couldn’t use phone and internet at the same time (because the line was occupied).  

**In short:** Dial-up = access network using telephone lines + modem to convert signals, very low bandwidth.  

![Dialup](/images/dialup.png)

#### Digital Subscriber Line (DSL)

- Uses the existing **telephone lines (copper wires)** to provide internet.  
- Unlike dial-up, it **separates voice and data** → you can talk on the phone and use the internet at the same time.  
- Much faster than dial-up → speeds usually in **Mbps range** (though lower than fiber/cable).  
- Works best when you are close to the telephone company’s central office — farther distance = weaker signal = slower speed.  

**In short:** DSL = broadband internet over telephone lines, higher bandwidth than dial-up, but speed decreases with distance.  

![DSL](/images/DSL.png)

#### Hybrid Fiber-Coaxial (HFC)

- Uses **fiber-optic cables** for the main connection from the provider to local areas.  
- Then switches to **coaxial cables** to connect homes and businesses.  
- Common in cable TV networks, also provides internet.  
- Higher bandwidth than DSL, but performance can drop when many users in the same area are active (shared medium).  

**In short:** HFC = hybrid of fiber (to local area) and coaxial (to homes), used for cable TV + internet, higher bandwidth than DSL, but speed may reduce due to shared use.  

#### Fiber To The Home (FTTH)

- Uses **optical fiber** all the way from the provider to the user’s home or office.  
- Provides very high bandwidth (**hundreds of Mbps to Gbps**).  
- Not affected by distance like DSL (fiber signals don’t degrade as quickly).  
- More reliable, supports modern high-demand applications (HD/4K streaming, cloud, gaming, etc.).  
- More expensive to install compared to DSL or HFC.  

**In short:** FTTH = optical fiber directly to homes/offices, offers very high bandwidth, reliable performance, unaffected by distance, but costly to deploy.  

#### Satellite

- Connects users through a **satellite dish** that communicates with satellites in orbit (usually geostationary).  
- Provides access in remote or rural areas where DSL, HFC, or FTTH aren’t available.  
- Bandwidth is decent (**tens to hundreds of Mbps**, depending on the system).  
- **Main drawback:** very high latency (because signals travel thousands of kilometers to space and back).  
- Latency makes real-time apps like gaming or video calls less smooth.  
- More expensive and weather-sensitive compared to wired options.  

**In short:** Satellite = internet via orbiting satellites, useful in remote areas, reasonable bandwidth but high latency, costlier and weather-affected.  

---


### Enterprise Access Network (Ethernet)

A **wired LAN (Local Area Network)** technology that connects devices in homes, schools, and offices.  

- Typically used in companies, universities, etc.  
- Uses **twisted pair cables** (like Cat5e, Cat6) or sometimes fiber to connect devices to a switch/router.  
- Provides high bandwidth (**100 Mbps, 1 Gbps, even 10+ Gbps**).  
- Very reliable and has **low latency** compared to wireless.  
- Limited to shorter distances (usually within a building or campus).  

**In short:** Ethernet = wired LAN technology, high bandwidth and low latency, very reliable, used in homes/offices but limited to short distances.  

---

### Wireless Access Network

Connects users to the ISP without cables, using **radio waves**.  

**Examples:** Wi-Fi (home/office), Cellular networks (3G, 4G, 5G), WiMAX.  

- Provides flexibility and mobility — you can connect from anywhere within coverage.  
- Bandwidth is improving (**5G can rival wired**), but usually less stable than Ethernet/fiber due to interference, distance from towers/routers, and shared usage.  

**In short:** Wireless Access Network = connects users via radio waves (Wi-Fi, 4G/5G), offers mobility and convenience, good bandwidth but less stable than wired.  

---

## Physical Media

The actual path through which data (as signals) travels.  

**Examples:** copper wires, fiber optics, radio waves.  

- **Bit** → The smallest unit of data (0 or 1).  
  On the physical medium, a bit is represented by a signal (voltage, light pulse, or radio wave). Propagates between transmitter/receiver pairs.  

- **Physical Link** → The direct connection between two devices through physical media.  
  Example: the Ethernet cable between your laptop and router.  

- **Guided Media** → Signals travel through a solid medium.  
  **Examples:** twisted pair cable, coaxial cable, fiber-optic cable.  
  More reliable, less interference.  

- **Unguided Media** → Signals travel freely through air or space (no solid medium).  
  **Examples:** radio waves, microwaves, infrared, satellite.  
  More flexible, but more prone to interference.  

---

### Twisted Pair

- Least expensive, most commonly used, guided media.  
- Made of pairs of copper wires twisted together.  
- The twisting helps reduce electromagnetic interference from outside and from neighboring pairs.  
- Used in telephony, Ethernet LANs, DSL connections.  

Two main types:  
- **UTP (Unshielded Twisted Pair)** → cheaper, widely used in LANs.  
- **STP (Shielded Twisted Pair)** → has extra shielding for better noise protection.  

**Bandwidth:** varies (older Cat3 ~10 Mbps, modern Cat6/7 ~1–10 Gbps).  

**In short:** Twisted Pair (TP) = copper wires twisted in pairs, reduces interference, used in LANs/telephony/DSL. Types: UTP, STP. Bandwidth up to Gbps (Cat6/7).  

Unshielded Twisted Pair →  
![UTP](/images/UTP.png)  

Shielded Twisted Pair →  
![STP](/images/STP.png)  

---

### Coaxial Cable

- A type of guided media with a **central copper conductor**, an insulating layer, a metallic shield, and an outer jacket.  
- The shield helps protect the signal from electromagnetic interference.  
- Used in **cable TV networks, broadband internet (HFC), and some LANs**.  
- Supports higher bandwidth and longer distances than twisted pair.  

**In short:** Coaxial Cable = copper core + insulation + metallic shield + jacket, guided media, reduces interference, used in cable TV, broadband, LANs, higher bandwidth than twisted pair.  

![Coaxial cable](/images/coaxial.jpg)  

---

### Fiber Optic Cable

- A guided medium that carries data as **light pulses** instead of electrical signals.  
- Made of a **core (glass/plastic)** surrounded by **cladding** that reflects light back inside, plus protective layers.  
- **Immune to electromagnetic interference.**  
- Supports very high bandwidth (**up to Tbps**) and long distances (**tens to hundreds of kilometers**).  
- Widely used in **FTTH, backbone networks, submarine cables, data centers**.  
- More expensive and delicate to install than copper cables.  

**In short:** Fiber Optic Cable = uses light signals through glass/plastic core, very high bandwidth & long distance, immune to interference, used in FTTH/backbone, costlier than copper.  

---

### Radio

- Uses **electromagnetic radio waves** to transmit data without physical cables.  
- Widely used in **Wi-Fi, Bluetooth, AM/FM radio, mobile networks**.  
- Can cover short distances (**Bluetooth**) to very long distances (**satellite**).  
- Main issue: **interference and limited frequency spectrum**.  

**Types of Radio Communication:**  

1. **Terrestrial Radio**  
   - Signals travel from a ground transmitter to receivers on Earth.  
   - **Examples:** AM/FM radio, Wi-Fi, cellular networks.  
   - Coverage depends on transmitter power and obstacles (buildings, mountains).  

2. **Satellite Radio (and Communication)**  
   - Signals are sent from Earth → satellite in orbit → back to Earth.  
   - Provides wide coverage, often global.  
   - Used in **satellite TV, GPS, satellite phones, and some internet services.**  
   - Has higher latency because signals travel long distances to space.  

---


## The network core

### Mesh of interconnected routers/packet switches

---

### Circuit Switching

A dedicated path (circuit) is reserved between sender and receiver for the whole communication.

Like a phone call → once the circuit is set up, you get guaranteed bandwidth.

- **Advantage**: predictable, fixed performance.  
- **Disadvantage**: inefficient — the circuit sits idle if no data is being sent.

**In short**: Circuit Switching = dedicated path, guaranteed bandwidth, but wasteful if idle.

---

### Packet Switching

Data is broken into packets, and each packet is routed independently across the network.

Like sending letters through a postal system.

- **Advantage**: efficient use of network resources, supports many users at once.  
- **Disadvantage**: no guarantee of bandwidth → can face delay (congestion).

**In short:** Packet Switching = data split into packets, efficient sharing, but variable delays.

---

### Host sending function

- Takes an application message.  
- Breaks it into packets of length L bits.  
- Sends each packet into the access network at a rate R bps (the link’s transmission rate / capacity / bandwidth).

So the time to push 1 packet into the link = L/R

---

### Packet Switching

#### Packet Transmission Delay
```Packet Transmission Delay = L/R  ```

```Time needed to transmit L-bit packet into link = L(bits)/R (bits/sec)  ```

Where L is it and R is link transmission rate.

#### Store and forward delay
In packet-switched networks, routers receive the entire packet before forwarding it to the next link.  

If a router gets a packet of L bits and the outgoing link rate is R, the forwarding delay is also: L/R  

If a message is split into N packets, the first packet incurs this delay at each hop, and others follow in a pipeline fashion.

**In short:**  
Transmission delay = time to push packet bits onto the link = L/R  

Store-and-forward delay = each router must receive full packet (L bits) before forwarding, so adds delay L/R per hop.

---

#### Question
If a 2,000-bit packet is sent on a link of 1 Mbps, what’s the transmission delay?

![Solution](/images/solution.png)

End-End delay for N links = NL/R

---

### Types of delay in packet-switched networks

When a packet travels through a network router/switch, there are four main types of delay:

1. Processing delay – time to examine the packet header.  
2. Queuing delay – time waiting in the output buffer before transmission.  
3. Transmission delay – time to push the bits onto the link.  
4. Propagation delay – time for the signal to travel across the medium.

For detailed refer here- [Network delay](#network-delays)

---

### Queuing delay and loss

**Queuing delay:**  
Happens when the arrival rate of packets exceeds the service rate of the outgoing link.  

- If traffic is light, queuing delay is almost zero.  
- If the link is congested, the queue grows → packets wait longer.  
- In extreme congestion, delay can grow very large (approaches infinity in theory).

**Loss:**  
Each router has a finite buffer for queues.  
When the buffer is full and new packets arrive → those packets are dropped (lost).  

This is called packet loss due to buffer overflow.  

TCP reacts to this by retransmitting and reducing sending rate; UDP may just lose data.

Analogy: crowded ticket counter  
- If there are only 2–3 people, you get your ticket quickly (low queuing delay).  
- If 100 people arrive, you wait longer (high queuing delay).  
- If the room is too small to fit everyone, new arrivals are turned away (packet loss).

---

#### Queuing delays

Happens at a router or switch when multiple packets arrive at the same time but the outgoing link can only send one packet at a time.  

Packets wait in a buffer (queue) before being transmitted.

The delay depends on:  
- Traffic intensity (how busy the link is).  
- Packet arrival rate vs link transmission rate.  
- Queue size (if full, packets may be dropped).

---

### Two key network-core functions

At the heart of the Internet, the network core has two main jobs:

**Routing**  
Figuring out the path packets should take from the source to the destination.  
Think of it like Google Maps deciding which road to take.  
Uses algorithms and routing tables.

**Forwarding**  
Actually moving packets from a router’s input to the correct output link, based on the routing decision.  
Like a traffic cop at an intersection directing each car where to go.

So:  
- Routing = planning (the path).  
- Forwarding = action (the step-by-step movement along the path).

---

### Circuit Switching

**Recall**: like making a phone call. A fixed path with reserved resources is established end-to-end before communication.

#### Frequency Division Multiplexing (FDM) VS Time Division Multiplexing (TDM)

**1. Frequency Division Multiplexing (FDM)**  
The available bandwidth of the link is split into frequency bands.  
Each call/user gets its own frequency band for the entire duration.  

Example: like radio stations, each has its own channel.

**2. Time Division Multiplexing (TDM)**  
The link’s bandwidth is split into time slots.  
Each call/user gets the whole bandwidth, but only during its assigned time slot, repeating in cycles.  

Example: like people taking turns speaking in a meeting.

**Analogy:**  
FDM = each person sings on a different pitch (at the same time).  
TDM = each person takes turns singing (one after another, in rhythm for specific time).

Transmission rate of circuit = Frame rate × Number of bits in a slot.

![Circuit switching](/images/circuit-switching.png)

#### Example
- If the link transmits 8000 frames per second  
- Each slot consists of 8 bits  
- Transmission rate of a circuit = 8000 × 8 bps = 64000 bps = 64 Kbps

---

#### Problem
How long does it take to send a file of 640,000 bits from host A to host B over a circuit-switched network?  
All links in the network use TDM with 24 slots and have a bit rate of 1.536 Mbps.  
500 msec to establish end-to-end circuit  

**Solution:**  
![Solution](/images/solution2.png)

---

### Packet Switching vs Circuit Switching

**Circuit switching:** A dedicated communication path is established before data transfer.  
**Packet switching:** Data is broken into packets and sent independently over shared paths.

**Advantages**

Circuit switching  
- Guaranteed bandwidth & delay once circuit is established.  
- Simple and predictable performance.

Packet switching  
- Efficient use of network resources (no idle time if one user is silent).  
- Robust: packets can take alternate routes if a link fails.  
- Supports many users at once (statistical multiplexing).  
- Allocates link use on demand. Link transmission capacity will be shared on a packet-by-packet basis only among those users who have packets that need to be transmitted over the link.

**Disadvantages**

Circuit switching  
- Wasteful if users are silent (resources sit idle).  
- Call setup delay before communication starts.  
- Less scalable for bursty data traffic.  
- Preallocates use of the transmission link regardless of demand, with allocated but unneeded link time going unused.

Packet switching  
- Variable delay and possible congestion.  
- No guaranteed bandwidth or delivery time.

**Analogy:**  
Circuit switching = renting the whole road for your car.  
Packet switching = cars share the road, might face traffic but it’s flexible.

---

**"Less scalable for bursty data traffic."**  

Means: In circuit switching, when we set up a circuit, we reserve bandwidth for the entire session — whether we send data or stay idle.  

If we transmit data continuously, the reserved path is fully used.  

But for bursty traffic (common in computer networks, where we send a burst of data and then pause), the reserved circuit remains unused during silent periods.  

This means other users cannot use those resources, even though they are free at that moment.  

So, with many bursty users, the network quickly runs out of available circuits and scales poorly compared to packet switching, where resources are shared dynamically.

---

## Internet structure

Since we all are connected to ISPs (Internet Service Providers) and we all can have different ISP (e.g., Jio, BSNL, Airtel etc.). And such ISPs are more than thousands, then how these ISPs are connected together?

**Option 1** – Connect all ISPs together.

Problem:  
![ISP](/images/isp.png)

**Option 2** – Connect each access ISP to a global transit ISP.
Connection and provider ISP have economic aggrement.
![ISP](/images/isp2.png)

But if one global ISP is viable business, there will be competitors which also needs to be connected.

![ISP](/images/isp3.png)

**Internet Exchange Point (IXP)**

- An IXP is a physical location where multiple ISPs and networks connect and exchange traffic directly.

- Purpose: reduces cost and delay by avoiding sending data through higher-level ISPs unnecessarily.

- ISPs peer at IXPs so local traffic stays local.

Also regional networks may arise to connect access nets to
ISPS. And content provider networks (e.g., Google, Microsoft, Akamai ) may run their own network, to bring services, content close to end users.

![ISP](/images/isp4.png)

#### How all ISP connected together?

**Tier-1 ISPs**

- The biggest global ISPs (like AT&T, Tata, NTT).

- They interconnect with each other directly using peering agreements.

- They form the “backbone” of the internet.

**Tier-2 ISPs**

- Regional or national ISPs.

- They connect to Tier-1 ISPs to get global reach, and sometimes peer with each other.

**Tier-3 ISPs**

- Local ISPs (the ones we usually buy service from).

- They connect to Tier-2 ISPs for internet access.

**Content Provider Networks**

- Large companies (Google, Microsoft, Amazon, Netflix, etc.) build their own private global networks instead of relying only on ISPs.

- They connect their data centers and cache servers worldwide using high-speed fiber.

- These networks often connect directly to ISPs or to IXPs, bypassing Tier-1 ISPs.

---

## Internet

### Network delays
When a packet travels from source to destination, it has to endure certain delays like - (Refere here:-  [Delays](#types-of-delay-in-packet-switched-networks) )

1. Nodal processing delay
2. Queuing delay
3. Transmission delay
4. Propagation delay

![delay](/images/delay.png)

**Example:** Driving a car from City A to City B

**Nodal Processing Delay**

- At each checkpoint (like a toll booth), the guard checks your ticket and decides where you should go.

- That small inspection time = processing delay.

**Queuing Delay**
- If many cars are waiting at the toll booth, our car has to wait in line.

- That waiting time = queuing delay.

**Transmission Delay**

- Imagine cars crossing the toll gate one by one at a fixed rate.

- The time it takes for our whole car to pass through = transmission delay.

- In networking, this is how long it takes to push all the packet bits onto the link.

**Propagation Delay**

- After the car leaves the toll, it drives along the highway to the next city.

- The time it takes to travel the distance = propagation delay.

So ```total nodal delay (d) = processing delay + queueing delay + transmission delay + propagation delay```

#### Queuing delay-revisited

Assume queue is very big.
```
a = average packet arrival rate(packets/second)
R = transmission rate i.e link bandwidth (bps)
L = Packet length(bits)
```
```
The average rate at which bits arrive at the queue = La bits/sec
```

```
Traffic intensity = La/R
```

```markdown
# La/R > 1 : 
avg. queuing delays becomes large

# La/R ≤ 1 :
nature of arriving packets impacts the queuing delay

# La/R ~ 0 :
avg. queueing delay small

# La/R ~ 1 :
average queuing delay gets larger
```

#### Packet Loss
- queue (aka buffer) preceding link in buffer has finite capacity
- when packet arrives to full queue, packet is dropped (aka
lost)
- The fraction of lost packets increases as the traffic
intensity increases
- lost packet may be retransmitted by previous node, by
source end system, or not retransmitted at all

![Loss](/images/loss.png)

#### End-to-end delay

It is the total delay a packet experiences from the source host to the destination host.

$$
d_{\text{end-to-end}} = N \times (d_{\text{proc}} + d_{\text{queue}} + d_{\text{trans}} + d_{\text{prop}})
$$


**where** 

![Abreb](/images/abbreb.png)

### Throughput

The rate at which data is successfully delivered from sender to receiver, measured in bits per second (bps).

It is of two types-
1. **Instantaneous throughput** → the rate at a particular moment.

2. **Average throughput** → total data delivered ÷ total time. If the file consists of ``F bits``, transfer takes ``T secs`` for a Host to receive all F bits, 
``Average throughput = F/T bits per second``
   

**Car Analogy**

- Imagine we’re moving trucks of goods from City A to City B.

- Throughput = how many trucks full of goods actually arrive at City B per second.

- Even if the road is wide (high bandwidth), traffic jams (congestion) or slow tolls (processing/transmission limits) can reduce the actual throughput.

#### Bandwidth vs Throughput

**Bandwidth** = the maximum capacity of a link (like the width of a highway).

**Throughput** = the actual rate at which data is delivered end-to-end (like the number of cars that actually reach the destination per second).

🔹 **Key difference:**

- Bandwidth is a theoretical upper limit.

- Throughput depends on real conditions: congestion, queuing, protocol overhead, etc.

#### Bottleneck throughput case

![Throughput](/images/throughput.png)

#### Transfer time

**Transfer time**: Time taken to move a message from sender to receiver over a network link.It includes both transmission time and propagation time.

**Case 1: Link-level transfer time**

- Used when we are analyzing one link between two nodes.

- We care about both:

  - Transmission time (putting bits on the link).

  - Propagation delay (signal traveling in the medium).

- Example: LAN cable between two computers.

```Transfer Time = Transmission Time + Propagation Delay```

![Formula2](/images/formula2.png)

**where**

- **L :** file size or message size in bits 
- **R :** link bandwidth (in bps) or transmission rate (in bps)
- **D :** distance between sender and receiver (meters)
- **S :** propagation speed (m/s, close to speed of light in fiber)

**Case 2: End-to-end file transfer (client–server model)**
- Used when sending a whole file over a network.

- We care about the slowest rate between the sender and the network.

- Propagation delay is often tiny compared to file size, so it’s ignored here.

- Example: downloading a movie — bottleneck is our internet speed, not the distance to the server.
  

$$
T = \frac{F}{\min(R_s, R_c)}
$$


where:  
- $F$  = File size (in bits)  
- $R_s$ = Sender rate (bps)  
- $R_c$ = Channel rate / link capacity (bps)  


**Example**:  Downloading MP3 file of F=32 million bits Rs=2Mbps, Rc =1Mbps

Time needed to transfer the file = 32/1=32 secs

Suppose there are N links then the throughput will be:
Min(R1, R2,...,RN).

---

## Network protocols

### Internet protocol stack (TCP/IP Model)
When taken together, the protocols of various layers are called the protocol stack.

The Internet protocol stack (TCP/IP Model) has 4 layers that handle end-to-end communication over the Internet:

```markdown

                | TCP/IP Layers |
                |---------------|
                | Application   |
                | Transport     |
                | Internet      |
                | Link          |
                | Physical      |

```

**Application Layer**

- Provides services directly to applications.

- Combines OSI’s Application, Presentation, and Session layers.

- Examples: HTTP, FTP, SMTP, DNS.

**Transport Layer**

- Provides end-to-end communication between hosts.

- Ensures reliability if needed.

- Examples: TCP (reliable), UDP (unreliable).

**Internet Layer**

- Responsible for addressing and routing packets across networks.

- Example: IP (Internet Protocol), ICMP.

**Link Layer (Network Access Layer)**

- Handles node-to-node delivery over physical media.

- Combines OSI’s Data Link + Physical layers.

- Examples: Ethernet, Wi-Fi, PPP.

**Physical Layer**

- Transmits raw bits (0s and 1s) over a physical medium like copper wires, fiber optic cables, or wireless channels.

- Focus: How the signal travels — electrical, optical, or radio signals.

- No concern for: addressing, routing, or reliability.

**Quick Analogy:**

**Application** = Apps talking to each other (like sending emails or browsing).

**Transport** = Ensures your message reaches correctly (like a courier with a tracking number).

**Internet** = Decides the route across cities/countries (like GPS for data).

**Link** = Roads and vehicles between nearby locations (physical transmission).

**Physical layer** = the roads or cables that cars (data) travel on.
We don’t care about the destination or traffic rules here, just that the cars can move from point A to B.

### ISO/OSI reference model


| OSI Model Layers |
|-----------------|
| Application     |
| Presentation    |
| Session         |
| Transport       |
| Network         |
| Data Link       |
| Physical        |


**Presentation layer:**  allow applications to interpret meaning of data, e.g., encryption, compression, machine-specific conventions.

**Session layer:** synchronization, checkpointing, recovery of data
exchange.


**Comparison between OSI and TCP/IP model-**


| OSI Model Layer      | TCP/IP Layer      |
|---------------------|-----------------|
| Application         | Application     |
| Presentation        | Application     |
| Session             | Application     |
| Transport           | Transport       |
| Network             | Internet        |
| Data Link           | Link            |
| Physical            | Link / Physical |
