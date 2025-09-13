# Computer Network

## Contents
- [Computer Network](#computer-network)
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
