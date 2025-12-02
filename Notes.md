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
      - [OSI model in brief:](#osi-model-in-brief)
- [Application Layer (Part-2)](#application-layer-part-2)
  - [Introduction](#introduction-1)
      - [Client-Server Model](#client-server-model)
      - [Peer- Peer architecture (P2P model)](#peer--peer-architecture-p2p-model)
      - [Process Communication](#process-communication)
      - [Sockets](#sockets)
      - [Addressing processes](#addressing-processes)
  - [Common Application Layer Protocols](#common-application-layer-protocols)
      - [HTTP (HyperText Transfer Protocol)](#http-hypertext-transfer-protocol)
      - [SMTP (Simple Mail Transfer Protocol)](#smtp-simple-mail-transfer-protocol)
      - [IMAP (Internet Message Access Protocol) / POP3 (Post Office Protocol)](#imap-internet-message-access-protocol--pop3-post-office-protocol)
      - [DNS (Domain Name System)](#dns-domain-name-system)
      - [FTP (File Transfer Protocol)](#ftp-file-transfer-protocol)
      - [DHCP (Dynamic Host Configuration Protocol)](#dhcp-dynamic-host-configuration-protocol)
      - [SNMP (Simple Network Management Protocol)](#snmp-simple-network-management-protocol)
      - [Telnet / SSH](#telnet--ssh)
  - [Connection-Oriented vs Connectionless Communication](#connection-oriented-vs-connectionless-communication)
  - [HTTP connection](#http-connection)
    - [Types of HTTP connection](#types-of-http-connection)
      - [Non-persistent HTTP](#non-persistent-http)
      - [Persistent HTTP](#persistent-http)
    - [Difference between Persistent and Non-Persistent HTTP](#difference-between-persistent-and-non-persistent-http)
    - [HTTP Response Time \& RTT](#http-response-time--rtt)
    - [HTTP request methods-](#http-request-methods-)
    - [Cookies](#cookies)
    - [Web Caches (Proxy Servers)](#web-caches-proxy-servers)
    - [HTTP 1 VS HTTP 2](#http-1-vs-http-2)
      - [HTTP 1.1](#http-11)
      - [HTTP/2 \[RFC 7540, 2015\]](#http2-rfc-7540-2015)
    - [HTTP 2 vs HTTP 3](#http-2-vs-http-3)
  - [Email](#email)
    - [SMTP- Simple Mail Transfer Protocol](#smtp--simple-mail-transfer-protocol)
      - [Key Points:](#key-points)
      - [Three phases of transfer-](#three-phases-of-transfer-)
      - [How it works (simple analogy):](#how-it-works-simple-analogy)
      - [How it works (More technically):](#how-it-works-more-technically)
      - [In short:](#in-short)
    - [Retrieving mails- Mail access protocols](#retrieving-mails--mail-access-protocols)
      - [**POP3 (Post Office Protocol version 3)**](#pop3-post-office-protocol-version-3)
      - [**IMAP (Internet Message Access Protocol)**](#imap-internet-message-access-protocol)
      - [Webmail (HTTP/HTTPS based)](#webmail-httphttps-based)
  - [DNS- Domain Name System](#dns--domain-name-system)
    - [DNS hierarchy](#dns-hierarchy)
      - [Types-](#types-)
    - [DNS name resoltuion](#dns-name-resoltuion)
      - [Iterated query](#iterated-query)
      - [Recursive query](#recursive-query)
  - [P2P (Peer-to-Peer) Architecture](#p2p-peer-to-peer-architecture)
    - [Types of P2P Networks:](#types-of-p2p-networks)
    - [How it works (simple analogy):](#how-it-works-simple-analogy-1)
    - [Advantages:](#advantages)
    - [Disadvantages:](#disadvantages)
    - [P2P File Distribution in BitTorrent](#p2p-file-distribution-in-bittorrent)
      - [Definition:](#definition)
      - [How it works (simple analogy):](#how-it-works-simple-analogy-2)
      - [Roles in BitTorrent:](#roles-in-bittorrent)
      - [Advantages:](#advantages-1)
    - [BitTorrent – Tit-for-Tat](#bittorrent--tit-for-tat)
      - [Key Points:](#key-points-1)
  - [Video Streaming and Content Delivery Networks (CDN)](#video-streaming-and-content-delivery-networks-cdn)
    - [Streaming Stored Video (VOD – Video on Demand)](#streaming-stored-video-vod--video-on-demand)
      - [Stored Video Streaming:](#stored-video-streaming)
      - [Challenges in Stored Video Streaming:](#challenges-in-stored-video-streaming)
      - [Client-Side Buffering and Playout Delay:](#client-side-buffering-and-playout-delay)
    - [Role of CDN in Video Streaming:](#role-of-cdn-in-video-streaming)
    - [In short:](#in-short-1)
    - [Streaming Multimedia: DASH (Dynamic Adaptive Streaming over HTTP)](#streaming-multimedia-dash-dynamic-adaptive-streaming-over-http)
      - [Benefits:](#benefits)
      - [In short:](#in-short-2)
  - [Socket](#socket)
      - [Simple Analogy:](#simple-analogy)
- [Transport Layer (Part- 3)](#transport-layer-part--3)
  - [Multiplexing \& Demultiplexing](#multiplexing--demultiplexing)
  - [Connectionless vs. Connection-oriented:](#connectionless-vs-connection-oriented)
    - [Connection-Oriented vs. Connectionless Demultiplexing](#connection-oriented-vs-connectionless-demultiplexing)
  - [UDP- User Datagram Protocol](#udp--user-datagram-protocol)
    - [UDP: Glance at transport layer](#udp-glance-at-transport-layer)
      - [UDP- Sender action](#udp--sender-action)
      - [UDP- Reciever action](#udp--reciever-action)
  - [Principles of Reliable Data Transfer (RDT)](#principles-of-reliable-data-transfer-rdt)
    - [Finite State Machines (FSMs)](#finite-state-machines-fsms)
    - [RDT 1.0- **Reliable transfer over a reliable channel**](#rdt-10--reliable-transfer-over-a-reliable-channel)
    - [RDT 2.0- **Channel with bit errors**](#rdt-20--channel-with-bit-errors)
      - [Recovery from errors](#recovery-from-errors)
      - [What if ack or nak are corrupted](#what-if-ack-or-nak-are-corrupted)
    - [RDT 3.0- **channels with errors and loss**](#rdt-30--channels-with-errors-and-loss)
    - [Go-Back-N (GBN) Sender](#go-back-n-gbn-sender)
      - [Analogy:](#analogy)
      - [FSM (Sender Simplified):](#fsm-sender-simplified)
    - [Selective Repeat (SR) ARQ](#selective-repeat-sr-arq)
      - [Example](#example-1)
      - [Comparison with Go-Back-N](#comparison-with-go-back-n)
      - [Analogy](#analogy-1)
  - [TCP - Transission Control Protocol](#tcp---transission-control-protocol)
    - [Sequence Number in TCP](#sequence-number-in-tcp)
      - [Simple Example:](#simple-example)
      - [Analogy:](#analogy-2)
    - [TCP steps-](#tcp-steps-)
    - [TCP Premature Timeout](#tcp-premature-timeout)
      - [Simple Analogy](#simple-analogy-1)
    - [TCP Flow Control](#tcp-flow-control)
      - [Simple Analogy](#simple-analogy-2)
    - [TCP Handshakes](#tcp-handshakes)
    - [3-Way Handshake (Standard TCP Connection Setup)](#3-way-handshake-standard-tcp-connection-setup)
      - [Analogy](#analogy-3)
    - [2-Way Handshake (Conceptual / Non-standard TCP)](#2-way-handshake-conceptual--non-standard-tcp)
  - [Congestion control](#congestion-control)
    - [Causes of Congestion](#causes-of-congestion)
    - [Costs of Congestion](#costs-of-congestion)
    - [Mechanisms of Congestion Control (TCP Example)](#mechanisms-of-congestion-control-tcp-example)
    - [Simple Analogy](#simple-analogy-3)
    - [TCP Congestion Control: AIMD](#tcp-congestion-control-aimd)
    - [Key Points](#key-points-2)
    - [How it works (Timeline Example)](#how-it-works-timeline-example)
    - [Why AIMD?](#why-aimd)
    - [Simple Analogy](#simple-analogy-4)
- [Network Layer (Part- 4)](#network-layer-part--4)
    - [Key Points](#key-points-3)
      - [Host Responsibilities (Sender \& Receiver):](#host-responsibilities-sender--receiver)
    - [Network Layer Protocols (Present in Every Device)](#network-layer-protocols-present-in-every-device)
    - [Router Responsibilities](#router-responsibilities)
    - [Main Network Layer Functions](#main-network-layer-functions)
      - [1. Forwarding](#1-forwarding)
      - [2. Routing](#2-routing)
    - [Simple Analogy](#simple-analogy-5)
    - [Data Plane vs Control Plane](#data-plane-vs-control-plane)
    - [Key Points](#key-points-4)
      - [Data Plane (Forwarding Plane)](#data-plane-forwarding-plane)
      - [Control Plane](#control-plane)
    - [Simple Analogy](#simple-analogy-6)
  - [Network service model](#network-service-model)
  - [Switching fabric](#switching-fabric)
    - [Types of  Switching Fabrics:](#types-of--switching-fabrics)
  - [Input port queueing](#input-port-queueing)
    - [Head-of-Line (HOL) Blocking](#head-of-line-hol-blocking)
  - [Output port queueing](#output-port-queueing)
    - [Buffer management](#buffer-management)
    - [Packet Scheduling](#packet-scheduling)
  - [The bigger picture of network layer- What ecactly happens](#the-bigger-picture-of-network-layer--what-ecactly-happens)
  - [IP Addressing](#ip-addressing)
    - [Subnet](#subnet)
    - [CIDR Notation](#cidr-notation)
      - [What does 10.0.0.0/8 mean?](#what-does-100008-mean)
      - [1. What is the meaning of 10.0.0.0?](#1-what-is-the-meaning-of-10000)
      - [2. What does /8 mean?](#2-what-does-8-mean)
      - [How big is the network 10.0.0.0/8?](#how-big-is-the-network-100008)
      - [Why do colleges or companies use 10.0.0.0/8?](#why-do-colleges-or-companies-use-100008)
      - [Subnetting the /8 block](#subnetting-the-8-block)
      - [Why these are /24 and not /8?](#why-these-are-24-and-not-8)
      - [Summary](#summary)
    - [**How does a host get an IP address within its network (host part)?**](#how-does-a-host-get-an-ip-address-within-its-network-host-part)
    - [**How does a network get its IP address (network part)?**](#how-does-a-network-get-its-ip-address-network-part)
    - [DHCP client server interaction](#dhcp-client-server-interaction)
    - [Network Address Translation (NAT)](#network-address-translation-nat)
  - [IPv6 and Tunneling](#ipv6-and-tunneling)
    - [Why IPv6?](#why-ipv6)
    - [What is IPv6?](#what-is-ipv6)
    - [IPv4 and IPv6 Compatibility Issue](#ipv4-and-ipv6-compatibility-issue)
    - [What is IPv6 Tunneling?](#what-is-ipv6-tunneling)
    - [Why Tunneling?](#why-tunneling)
    - [Types of Tunneling](#types-of-tunneling)
    - [How Tunneling Works (Simple)](#how-tunneling-works-simple)
  - [OpenFlow vs Flow Table Abstraction](#openflow-vs-flow-table-abstraction)
    - [Flow Table Abstraction (Concept)](#flow-table-abstraction-concept)
    - [What is OpenFlow?](#what-is-openflow)
    - [Key Differences](#key-differences)
    - [Simple Summary](#simple-summary)
  - [Routing Protocols: Distance Vector vs Link State](#routing-protocols-distance-vector-vs-link-state)
    - [1. Distance Vector Routing Protocols](#1-distance-vector-routing-protocols)
      - [**Idea**](#idea)
      - [**Algorithm**](#algorithm)
      - [**How It Works**](#how-it-works)
      - [**Examples**](#examples)
      - [**Advantages**](#advantages-2)
      - [**Disadvantages**](#disadvantages-1)
    - [2. Link State Routing Protocols](#2-link-state-routing-protocols)
      - [**Idea**](#idea-1)
      - [**Algorithm**](#algorithm-1)
      - [**How It Works**](#how-it-works-1)
      - [**Examples**](#examples-1)
      - [**Advantages**](#advantages-3)
      - [**Disadvantages**](#disadvantages-2)
    - [Difference Table](#difference-table)
    - [Summary](#summary-1)
  - [OSPF (Open Shortest Path First)](#ospf-open-shortest-path-first)
    - [Key Features](#key-features)
    - [How OSPF Works](#how-ospf-works)
    - [Advantages](#advantages-4)
    - [Disadvantages](#disadvantages-3)
    - [Summary](#summary-2)
- [Link Layer (Part- 5)](#link-layer-part--5)
  - [Feature](#feature)
    - [1. Framing](#1-framing)
    - [2. MAC Addressing](#2-mac-addressing)
    - [3. Error Detection](#3-error-detection)
    - [4. Error Correction (Optional)](#4-error-correction-optional)
    - [5. Flow Control (Optional)](#5-flow-control-optional)
    - [6. Medium Access Control (MAC Protocols)](#6-medium-access-control-mac-protocols)
    - [7. Hop-by-Hop Delivery](#7-hop-by-hop-delivery)
  - [Internet Checksum and Cyclic Redundancy Check (CRC)](#internet-checksum-and-cyclic-redundancy-check-crc)
    - [1. Internet Checksum](#1-internet-checksum)
      - [**Purpose**](#purpose)
      - [**How It Works**](#how-it-works-2)
      - [**Features**](#features)
      - [**Used In**](#used-in)
    - [2. Cyclic Redundancy Check (CRC)](#2-cyclic-redundancy-check-crc)
      - [**Purpose**](#purpose-1)
      - [**How It Works**](#how-it-works-3)
      - [**Features**](#features-1)
      - [**Used In**](#used-in-1)
    - [Internet Checksum vs CRC](#internet-checksum-vs-crc)
  - [Multiple Access Protocols: Point-to-Point and Broadcast](#multiple-access-protocols-point-to-point-and-broadcast)
    - [1. Point-to-Point Links](#1-point-to-point-links)
      - [**Definition**](#definition-1)
      - [**Examples**](#examples-2)
      - [**Features**](#features-2)
    - [2. Broadcast (Shared) Links](#2-broadcast-shared-links)
      - [**Definition**](#definition-2)
      - [**Examples**](#examples-3)
    - [Types of Broadcast Multiple Access Protocols](#types-of-broadcast-multiple-access-protocols)
      - [**A. Random Access Protocols**](#a-random-access-protocols)
      - [**B. Controlled Access Protocols**](#b-controlled-access-protocols)
      - [**C. Channelization Protocols or Channel partitioning**](#c-channelization-protocols-or-channel-partitioning)
    - [Point-to-Point vs Broadcast (Comparison)](#point-to-point-vs-broadcast-comparison)
    - [Summary](#summary-3)
  - [Channel partitioning protocols](#channel-partitioning-protocols)
    - [1. FDMA (Frequency Division Multiple Access)](#1-fdma-frequency-division-multiple-access)
      - [**Definition**](#definition-3)
      - [**How It Works**](#how-it-works-4)
      - [**Examples**](#examples-4)
      - [**Features**](#features-3)
    - [2. TDMA (Time Division Multiple Access)](#2-tdma-time-division-multiple-access)
      - [**Definition**](#definition-4)
      - [**How It Works**](#how-it-works-5)
      - [**Examples**](#examples-5)
      - [**Features**](#features-4)
    - [3. CDMA (Code Division Multiple Access)](#3-cdma-code-division-multiple-access)
      - [**Definition**](#definition-5)
      - [**How It Works**](#how-it-works-6)
      - [**Examples**](#examples-6)
      - [**Features**](#features-5)
    - [FDMA vs TDMA vs CDMA (Comparison)](#fdma-vs-tdma-vs-cdma-comparison)
    - [Summary](#summary-4)
  - [Random Access Protocols](#random-access-protocols)
    - [1. Pure ALOHA](#1-pure-aloha)
      - [**Definition**](#definition-6)
      - [**Collision Handling**](#collision-handling)
      - [**Efficiency**](#efficiency)
      - [**Features**](#features-6)
    - [2. Slotted ALOHA](#2-slotted-aloha)
      - [**Definition**](#definition-7)
      - [**Collision Handling**](#collision-handling-1)
      - [**Efficiency**](#efficiency-1)
      - [**Features**](#features-7)
    - [3. CSMA (Carrier Sense Multiple Access)](#3-csma-carrier-sense-multiple-access)
      - [**Definition**](#definition-8)
      - [**Features**](#features-8)
      - [**Types**](#types)
    - [4. CSMA/CD (Carrier Sense Multiple Access with Collision Detection)](#4-csmacd-carrier-sense-multiple-access-with-collision-detection)
      - [**Definition**](#definition-9)
      - [**Used In**](#used-in-2)
      - [**Features**](#features-9)
    - [5. CSMA/CA (Carrier Sense Multiple Access with Collision Avoidance)](#5-csmaca-carrier-sense-multiple-access-with-collision-avoidance)
      - [**Definition**](#definition-10)
      - [**Used In**](#used-in-3)
      - [**Features**](#features-10)
    - [Comparison of Random Access Protocols](#comparison-of-random-access-protocols)
    - [Summary](#summary-5)
  - [Controlled Access Protocols](#controlled-access-protocols)
    - [1. Token Ring](#1-token-ring)
      - [**Definition**](#definition-11)
      - [**How It Works**](#how-it-works-7)
      - [**Features**](#features-11)
    - [2. Token Bus](#2-token-bus)
      - [**Definition**](#definition-12)
      - [**How It Works**](#how-it-works-8)
      - [**Features**](#features-12)
    - [3. Polling (Master–Slave)](#3-polling-masterslave)
      - [**Definition**](#definition-13)
      - [**How It Works**](#how-it-works-9)
      - [**Features**](#features-13)
    - [Comparison of Controlled Access Protocols](#comparison-of-controlled-access-protocols)
    - [Summary](#summary-6)
  - [Summary of MAC (Medium Access Control) Protocols](#summary-of-mac-medium-access-control-protocols)
    - [1. Random Access Protocols](#1-random-access-protocols)
      - [**Examples**](#examples-7)
      - [**Key Idea**](#key-idea)
      - [**Pros**](#pros)
      - [**Cons**](#cons)
    - [2. Channel Partitioning Protocols (Channelization)](#2-channel-partitioning-protocols-channelization)
      - [**Examples**](#examples-8)
      - [**Key Idea**](#key-idea-1)
      - [**Pros**](#pros-1)
      - [**Cons**](#cons-1)
    - [3. Controlled Access Protocols (Taking Turns)](#3-controlled-access-protocols-taking-turns)
      - [**Examples**](#examples-9)
      - [**Key Idea**](#key-idea-2)
      - [**Pros**](#pros-2)
      - [**Cons**](#cons-2)
    - [**One-Line Summary**](#one-line-summary)
  - [DOCSIS (Data Over Cable Service Interface Specification)](#docsis-data-over-cable-service-interface-specification)
    - [Key Points](#key-points-5)
    - [DOCSIS Versions (Speeds)](#docsis-versions-speeds)
    - [Summary](#summary-7)
  - [Difference Between Switch and Router](#difference-between-switch-and-router)
  - [VLAN (Virtual Local Area Network)](#vlan-virtual-local-area-network)
    - [**Key Features**](#key-features-1)
    - [**How VLAN Works**](#how-vlan-works)
    - [**Summary**](#summary-8)
  - [MPLS (Multiprotocol Label Switching)](#mpls-multiprotocol-label-switching)
    - [**Key Features**](#key-features-2)
    - [**How MPLS Works**](#how-mpls-works)
    - [**Benefits**](#benefits-1)
    - [**Summary**](#summary-9)

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

#### OSI model in brief:

**Application layer:**
- It is the topmost layer. All protocol work here. (widely used- HTTP)
- Provides interface to access the network.
  
**Presentation layer:**
- Takes care of how data will be presented to reciever. Eg- Consider the case where sender knows english while reciever knows spanish.
- Technically, at the sender side, this layer translates the data format used by the application layer to the common format and at the reciever side, this layer translates the common format into the format used by the application layer at the reciever side.

**Session layer:**
- Its main role is to maintain a connection until sender sends the data and reciever recieves the data.
- It also reports about the error coming from the upper layers.
  
**Note**: Application layer, Presentation layer and Session layer are part of software.

**Transport layer:**
- It divides the data into segments.
- It has two protocols- 
  - **TCP**
    - It gives all info.
    - If we want to send data with proper acknowledgement that reciever has recieved the data.
  - **UDP**
    - We use this protocol when we want to send data faster. We won't be able to know whether the data has been sent or not.

**Network layer:**
- It divides data into packets.
- It stores the IP address of sender and reciever.
- Router is present at this layer.
- It also decides how the data should be sent so the reciever recieves fast.
Function: 
- Logical addressing
- Routing
- Packet forwarding
- Fragmentation
- Error handeling
  
**Datalink layer:**
- It maintains the speed of transfer and recieving of data between sender and reciever.
- It removes the error.
- It recieves the data from network layer and converts the data into data frames and then attach the physical address to these frames which are sent to physical layer.

**Physical layer:**
- Lowest layer
- Here the data gets converted to bits(0 and 1).
- Hubs, switch etc. are present here.
- It transmits data either in the form of electrical/optical or mechanical.

**Note**: Network layer, Datalink layer and physical lare are part of hardware.

![Osi model](/images/osi.jpg)

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

---

# Application Layer (Part-2)

## Introduction

**Recap**- It comprises of software.  All protocol works here. (widely used- HTTP). Provides interface to access the network.

**App like**-  Gmail, Web browsers, Emails etc.

#### Client-Server Model
| Client              | Server      |
|---------------------|-----------------|
| Communication with server         | Always on host     |
| Can have dynamic IP address        | Permanent IP address     |
| Do not communicate directly with each other             | May communicate with each other.     |

**Communication** 
- One-to-many relationship (server serves many clients).
- Clients depend on the server; if the server goes down, clients can’t access the service.

#### Peer- Peer architecture (P2P model)

In a peer-to-peer model, each device (peer) in the network acts as both a client and a server. Peers share resources (files, processing power, etc.) directly with each other without needing a centralized server.

- Each peer can request and provide services.

- Usually have dynamic IP addresses.

- No dedicated central server (though sometimes hybrid P2P has a small directory server).

**Communication**:

- Many-to-many relationship (peers talk directly).

- Scales well because each new peer can contribute resources.

- Reliability improves if multiple peers hold the same data.

**Examples**:

- File sharing (BitTorrent).

- Voice/video apps (Skype used hybrid P2P earlier).

- Blockchain and cryptocurrencies (Bitcoin, Ethereum).

#### Process Communication
Process communication means the exchange of data and information between two or more processes (programs in execution). This can happen within the same computer or across different computers in a network.

**Types**:

- **Inter-Process Communication (IPC)** – when processes communicate within the same machine.

  - Shared Memory: Processes share a common memory space to exchange information.

  - Message Passing: Processes send and receive messages via the OS.

- **Network Communication (Remote IPC)** – when processes communicate across different machines using protocols.

  - Uses sockets, RPC (Remote Procedure Call), or higher-level protocols (HTTP, gRPC, etc.).

**Key Points**:

- Synchronization is important (to avoid race conditions in shared memory).

- Message passing is safer but may be slower than shared memory.

- Used in client-server and P2P communication.

#### Sockets
A socket is an endpoint for communication between two processes over a network.

- One process writes to the socket, the other reads from it.

- Works like a door that lets data in and out of your computer over the network.

**Types of Sockets:**

- **Stream Sockets (TCP)**:

  - Connection-oriented (like a phone call).

  - Reliable → ensures data arrives in order, without loss.

  - Used in web browsing, email, file transfers.
  
  - Acknowledgement

- **Datagram Sockets (UDP)**:

  - Connectionless (like sending letters without confirmation).

  - Faster, but data may be lost or arrive out of order.

  - Used in video streaming, online gaming, VoIP.
  
  - No acknowledgement

- **Raw Sockets**:

  - Allow direct access to lower-layer protocols (like IP).

  - Mainly used for testing or building custom protocols.

Key Points:

- Each socket is identified by IP address + port number.

- Server sockets: listen for incoming connections.

- Client sockets: actively connect to a server.

#### Addressing processes
Addressing processes means identifying the sender and receiver in a network so data can be delivered correctly.
In the Internet, this requires two pieces of information:

- IP Address:  identifies the host (which computer).

- Port Number:  identifies the specific process (which application) on that host.

**Key Points:**

- IP address = "which machine" in the network.

- Port number = "which door/service" on that machine.

  - Together (IP, Port) = socket address.

- Example: 192.168.1.5:80 -

  - Host = computer with IP 192.168.1.5.

  - Process = web server (port 80 for HTTP).

## Common Application Layer Protocols

#### HTTP (HyperText Transfer Protocol)
- Used for web browsing (transfer of web pages).  
- Stateless (server maintains no information about past client requests ), request–response model.  
- Runs on port 80 (HTTPS on port 443 with encryption).  
- For detailed, refer here- [Http](#http)

#### SMTP (Simple Mail Transfer Protocol)
- Used for sending emails.  
- Works with IMAP/POP3 for receiving.  
- Runs on port 25.  

#### IMAP (Internet Message Access Protocol) / POP3 (Post Office Protocol)
- Used by mail clients to receive emails from mail servers.  
- IMAP (port 143) → keeps emails on server, sync across devices.  
- POP3 (port 110) → downloads emails, usually deletes from server.  

#### DNS (Domain Name System)
- Translates domain names (like google.com) into IP addresses.  
- Runs on port 53.  

#### FTP (File Transfer Protocol)
- Transfers files between client and server.  
- Uses port 21 (control) and 20 (data).  

#### DHCP (Dynamic Host Configuration Protocol)
- Assigns IP addresses automatically to devices.  
- Runs on ports 67 (server) and 68 (client).  

#### SNMP (Simple Network Management Protocol)
- Used to monitor and manage devices in a network (like routers, switches).  
- Runs on port 161.  

#### Telnet / SSH
- Remote login protocols.  
- Telnet (port 23) is insecure, SSH (port 22) is secure.  

## Connection-Oriented vs Connectionless Communication

**Definition:**  
- **Connection-Oriented:** A type of communication where a **dedicated connection** is established between sender and receiver before data is transmitted.  
- **Connectionless:** Communication where data is sent **without establishing a prior connection**. Each packet is independent.  

---

**Key Points:**  

| Feature | Connection-Oriented | Connectionless |
|---------|------------------|----------------|
| **Setup** | Connection must be established first | No setup required |
| **Reliability** | Reliable delivery (acknowledgements, retransmission) | Unreliable, may lose packets |
| **Order** | Guarantees order of data | No guarantee of order |
| **Overhead** | Higher (connection setup, teardown, acknowledgements) | Lower (no setup) |
| **Speed** | Slower due to overhead | Faster due to minimal overhead |
| **Examples** | TCP, FTP, HTTP | UDP, DNS, streaming |

---

**Analogy:**  

- **Connection-Oriented:** Like making a **phone call** — you dial, establish connection, talk, then hang up.  
- **Connectionless:** Like sending **letters/postcards** — you just send them, each one is independent, may get lost or arrive out of order.  

---

**In short:**  
- Connection-oriented = reliable, slower, needs setup (TCP).  
- Connectionless = fast, no setup, may be unreliable (UDP).  

## HTTP connection
- It is web's application layer protocol.
- Client-server model.
- HTTP use TCP (Transmission Control protocol)
  - Client initiates TCP connection **--->** server accepts TCP connection **--->** HTTP message gets exchanged between browser (HTTP client) and web browser (HTTP server) **--->** TCP connection is closed.

### Types of HTTP connection

#### Non-persistent HTTP
- TCP connection is opened
- At most one object (like image, script) can be sent over TCP connection.
- TCP connection is closed.
- Slower speed because of multiple hanshakes.

#### Persistent HTTP
- TCP connection is opened
- multiple objects can be sent over single TCP connection between client, and server.
- TCP connection is closed.
- Speed is fast because it avoids repeated handshakes.

### Difference between Persistent and Non-Persistent HTTP

| Feature | Non-Persistent HTTP | Persistent HTTP |
|---------|-------------------|----------------|
| **TCP Connection** | A new TCP connection is opened for each object | Single TCP connection is used for multiple objects |
| **Objects per Connection** | At most one object (like image, script) can be sent | Multiple objects can be sent over the same connection |
| **Connection Close** | TCP connection is closed after sending one object | TCP connection is closed only after all objects are sent |
| **Speed** | Slower due to multiple handshakes | Faster because repeated handshakes are avoided |
| **Overhead** | High, due to repeated TCP setup/teardown | Low, only one TCP setup/teardown for multiple objects |
| **RTT Requirement** | Multiple RTTs per object | Fewer RTTs since connection is reused |
| **Server Load** | Higher, more connections to handle | Lower, fewer connections to manage |
| **HTTP Version** | HTTP/1.0 typically | HTTP/1.1 and later |
| **Efficiency** | Less efficient for pages with many objects | More efficient for pages with many objects |


### HTTP Response Time & RTT

- **HTTP Response Time**: The total time taken from when a client sends an HTTP request until it receives the complete response from the server.

- **RTT (Round-Trip Time)**: The time it takes for a packet to travel from client → server and back → client.

**HTTP response time (per object):**
- one RTT to initiate TCP connection
- one RTT for HTTP request and first few bytes of HTTP response to return
- object/file transmission time

Non-persistent HTTP response time =  2RTT + file transmission time

![rtt](/images/rtt.png)

### HTTP request methods-
**1. GET**

- Definition: Requests data from the server without changing it.

- Used to retrieve information (e.g., a webpage, API data).

- Data sent in URL (query string), not in the body.

- Safe and idempotent (repeated calls don’t change anything).

- Example: Searching on Google.

**2. POST**

- Definition: Sends data to the server to create a new resource.

- Used to submit forms, upload files.

- Data is sent in request body.

- Not idempotent (calling twice may create duplicates).

- Example: Signing up for a new account.

**3. PUT**

- Definition: Updates/replaces an existing resource on the server.

- Entire resource is replaced with the new data.

- Idempotent (repeating the same request gives same result).

- Example: Updating your profile details.

**4. DELETE**

- Definition: Removes a resource from the server.

- Idempotent (deleting multiple times still results in “resource deleted”).

- Example: Deleting a post or file.

**5. HEAD**

- Definition: Same as GET, but only asks for the headers (not the body).

- Useful to check if a resource exists, or to get metadata (e.g., file size).

- Example: A browser checking if a file has changed before downloading.

### Cookies  

**Definition:**  
A **cookie** is a small piece of data that a web server stores on a user’s browser to maintain **state** (session info) across multiple HTTP requests, since HTTP is stateless.  

**How it works (4 components):**  
1. **Cookie in HTTP Response** → Server sends a cookie inside the HTTP response header (`Set-Cookie`).  
2. **Cookie in HTTP Request** → Browser automatically sends the cookie back to the server in the next request.  
3. **Cookie File on User’s Machine** → Browser stores cookies locally, often in a file.  
4. **Server Database** → Server links the cookie ID to stored session/user info.  


**Uses:**  
- Session management (logins, shopping carts).  
- Personalization (themes, user preferences).  
- Tracking (ads, analytics).  
- Authorization

**First party cookies-** track user behavior on a given website.

**Third party cookies-** track user behavior across multiple websites (third party cookies) without user ever choosing to visit tracker site.

### Web Caches (Proxy Servers)  

**Definition:**  
A **web cache** (or proxy server) is a network entity that stores copies of web content closer to users, so future requests for the same content can be served faster without always going to the origin server.  


**How it works:**  
1. Browser sends HTTP request to cache instead of origin server.  
2. If cache has a **fresh copy** → it serves directly (fast response).  
3. If not → cache forwards request to origin server, stores the response, then serves it to user.  


**Benefits:**  
- **Reduces response time** → faster browsing for users.  
- **Reduces traffic** → fewer requests to the origin server.  
- **Scalability** → helps servers handle more users without overload.  
- **Cost savings** → less bandwidth usage.  


### HTTP 1 VS HTTP 2

**Key goal:** Decreased delay in multi-object HTTP requests  

#### HTTP 1.1
- Introduced multiple, pipelined GETs over a single TCP connection.  
- Server responds **in-order** (FCFS: first-come-first-served) to GET requests.  
- **Head-of-line (HOL) blocking:** Small objects may wait behind large objects.  
- Loss recovery (retransmitting lost TCP segments) **stalls object transmission**.  

**Example:**  
Client requests 3 files in order:  
1. Video (5 GB)  
2. Image (4 KB)  
3. Audio (1 MB)  

- HTTP 1.1 serves **FCFS**, so small image/audio must wait until video is transmitted.  


#### HTTP/2 [RFC 7540, 2015]
- Increased flexibility at server in sending objects to client.  
- Methods, status codes, most header fields unchanged from HTTP 1.1.  
- Transmission order of requested objects based on **client-specified priority** (not FCFS).  
- Can **push unrequested objects** to client.  
- Divides objects into **frames** and schedules them to mitigate HOL blocking.  

**Example:**  
Same 3 files as above → objects are divided into frames, allowing **smaller objects to be delivered faster** even if requested after larger objects.  



### HTTP 2 vs HTTP 3

- HTTP/3 adds **security**, **per-object error handling**, and **congestion control over UDP**.  
- Eliminates HOL blocking at TCP level by using **QUIC protocol** over UDP.  
- Faster, more reliable performance in lossy networks compared to HTTP/2 over TCP.  

## Email
Three things-
1. User Agent (We, the users)
2. Mail servers (mailbox, message queue)
3. SMTP (Simple Mail Transfer Protocol)

### SMTP- Simple Mail Transfer Protocol

**SMTP** is the standard protocol used to send emails from a client to a mail server or between mail servers. It ensures that email messages are properly routed from the sender to the recipient’s server.

#### Key Points:

- **Works at the application layer** of the Internet protocol stack.
- **Usually uses TCP port 25** (for server-to-server) or 587/465 (for client-to-server with authentication/secure connection).
- **SMTP handles only sending emails**, not retrieving them (retrieval uses POP3 or IMAP).
- **Supports text-based commands** like `HELO`, `MAIL FROM`, `RCPT TO`, `DATA`, `QUIT`.
- **Can be combined with TLS/SSL** for secure email transmission.
- **Most email clients** (like Outlook, Gmail) use SMTP to send mail to their provider’s outgoing mail server.

#### Three phases of transfer-
- SMTP handshaking(greeting)
- SMTP transfer of messages
- SMTP closure

#### How it works (simple analogy):

Imagine sending a letter via postal service:

1. **You write a letter →** SMTP prepares the email with sender, recipient, and content.
2. **Go to local post office →** SMTP client connects to the mail server.
3. **Server checks the address →** Mail server validates the recipient address.
4. **Mail moves between post offices →** SMTP servers communicate to transfer the email to the recipient’s server.
5. **Delivered to recipient’s mailbox →** Recipient retrieves it using IMAP/POP3.

#### How it works (More technically):
1. A Person (lets say Pushpesh) uses user agent (say gmail), to compose an email and send it  to his friend `Oggy@gmail.com.`
2. Pushpesh sends message to his mail server (google in this case) using SMTP- The message gets placed in message queue.
3. Client side of SMTP (Pushpesh in this case) at mail server opens a TCP connection with Oggy's mail server.
4. Mail is sent to Oggy's server via TCP connection.
5. Oggy's mail server places the message in Oggy's mailbox.
6. Oggy then can read the mail from his mailbox using his user agent (Gmail, outlook) which retrieves it via **IMAP** or **POP3**.
  
SMTP and HTTP difference and similarities-

SMTP-
- Used to send emails from a client to a server or between servers
- Application layer
- Connection Type :Can be persistent but usually one-way from client to server
- State Stateful in sequence of commands (HELO → MAIL FROM → RCPT TO → DATA)

HTTP-
- Used to transfer web resources like HTML pages, images, or API data
- Application layer
- Can be persistent or non-persistent, supports request-response communication
- Stateless (each HTTP request is independent unless cookies/sessions used)


The SMTP design can be pictured as:

```
                    +----------+                +----------+
        +------+    |          |                |          |
        | User |<-->|          |      SMTP      |          |
        +------+    |  Client- |Commands/Replies| Server-  |
        +------+    |   SMTP   |<-------------->|    SMTP  |    +------+
        | File |<-->|          |    and Mail    |          |<-->| File |
        |System|    |          |                |          |    |System|
        +------+    +----------+                +----------+    +------+
                    SMTP client                SMTP server
```

When an SMTP client has a message to transmit, it establishes a two-
way transmission channel to an SMTP server.  The responsibility of an
SMTP client is to transfer mail messages to one or more SMTP servers,
or report its failure to do so.

#### In short:

**SMTP =** protocol to send emails, uses TCP, works with text commands, handles only outgoing mail, often combined with POP3/IMAP for receiving.

### Retrieving mails- Mail access protocols

Mail access protocols are used by email clients to retrieve messages from a mail server so users can read their emails. Unlike SMTP, which only sends emails, these protocols allow clients to download or view incoming mail.

**Common Mail Access Protocols:**

#### **POP3 (Post Office Protocol version 3)**

- Used to download emails from the server to your device.

- Works on TCP port 110 (non-secure) or 995 (secure/SSL).

- Default behavior: emails are deleted from the server after download (can be configured to keep a copy).

- Simple and lightweight, but not suitable for accessing mail from multiple devices.

**Analogy**: Like collecting letters from your mailbox and taking them home—once taken, the server doesn’t keep them by default.

#### **IMAP (Internet Message Access Protocol)**

- Allows viewing and managing emails directly on the server.

- Works on TCP port 143 (non-secure) or 993 (secure/SSL).

- Emails stay on the server, so you can access them from multiple devices.

- Supports folders, flags, search, and synchronization.

**Analogy**: Like reading letters at the post office without taking them home—available anytime, anywhere.

#### Webmail (HTTP/HTTPS based)
- Emails can be accessed via a web browser using HTTPS.

- Protocols like IMAP/POP3 run in the backend, but user sees a web interface.

- **Examples:** Gmail, Yahoo Mail, Outlook.com.

**Analogy**: Like visiting a digital post office online, reading and managing mail instantly.

**In short:**

**POP3** = download emails, simple, removes from server.

**IMAP** = access emails on server, multi-device friendly, syncs folders.

**Webmail** = browser-based email access, uses IMAP/POP3 in backend.

## DNS- Domain Name System

- Its an Application layer protocol

- DNS is the system that translates human-readable domain names (like www.google.com
) into IP addresses (like 142.250.190.14) that computers use to locate each other on the Internet.

**Key Points:**

- Works at the application layer.

- Like the Internet’s phonebook, mapping names to addresses.

- Helps users avoid remembering numeric IP addresses.

- Uses a hierarchical system:

- Root DNS servers → top-level domains (TLDs) → authoritative name servers → local resolver.

- Uses UDP (port 53) for most queries and TCP for larger transfers.

- Supports caching to speed up repeated queries.

**In short:**

DNS = Internet’s phonebook, translates domain names to IP addresses, uses hierarchical servers, works over UDP/TCP, caches responses for efficiency.

### DNS hierarchy
#### Types-
- Recursive Resolver: Queries other servers on your behalf.
- Root Server: Top of the hierarchy, points to TLD servers.
- TLD (Top level Domain) Server: Handles domains like .com, .org, .net.
- Authoritative Server: Provides the final IP for a domain.

![dns](/images/dns.png)

Note: ICANN (Internet Corporation for Assigned Names and Numbers) manages root DNS domain

### DNS name resoltuion
#### Iterated query
- Host contacts the server and contacted server either fullfills the request or gives the address of server to contact.
- It's like "I don’t know this name, but ask this server"

#### Recursive query
- Here the host asks the server and now the job remains on that server to find the address which then further asks another server and transfers the load. Heavy load at upper hierarchy.

## P2P (Peer-to-Peer) Architecture

**P2P architecture** is a networking model where each computer (peer) can act as both a client and a server, sharing resources like files, processing power, or bandwidth directly with other peers without a central server.

**Key Points:**

- **Decentralized:** No single server controls the network.
- Each peer can request and provide resources.
- Commonly used for file sharing, streaming, distributed computing, and blockchain networks.
- Reduces server bottlenecks because load is distributed.
- **Examples:** BitTorrent, Skype (original version), blockchain nodes.

### Types of P2P Networks:

**Pure P2P:**

- No central server at all.
- All peers are equal, share resources directly.
- **Example:** Early Gnutella network.

**Hybrid P2P:**

- Uses a central server to index resources or help peers find each other, but data is transferred directly between peers.
- **Example:** BitTorrent trackers, modern Skype.

### How it works (simple analogy):

Imagine a neighborhood of friends sharing books:

1. Everyone has some books at home.
2. You want a book → instead of going to a library, you ask your friends directly.
3. Each friend can lend books or borrow books from you.
4. No single library controls the flow; everyone contributes.

### Advantages:

- **Scalable →** Adding more peers adds more resources.
- **Fault-tolerant →** If one peer goes offline, others can still share data.
- **Efficient →** Reduces load on central servers.

### Disadvantages:

- Harder to secure → No central control.
- Resource availability depends on peers being online.
- Can be slower if peers have low bandwidth.

**In short:**
**P2P =** decentralized network where peers act as clients and servers, share resources directly, scalable and fault-tolerant, used in file sharing, streaming, and blockchain.

### P2P File Distribution in BitTorrent

#### Definition:
**BitTorrent** is a peer-to-peer (P2P) protocol for distributing large files efficiently. Instead of downloading a file from a single server, users (peers) download and upload pieces of the file from/to multiple peers simultaneously.

**Key Points:**
- The file is split into many small pieces (chunks).
- Peers download missing pieces from multiple sources at once, increasing speed.
- Each peer uploads pieces it already has to others — everyone contributes.
- Uses a tracker or DHT (Distributed Hash Table) to locate peers sharing the file.
- Ensures fairness using a “tit-for-tat” strategy — upload to peers who upload to you.
- Reduces server load, because the original seeder only needs to provide one copy.

#### How it works (simple analogy):

Imagine assembling a jigsaw puzzle with friends:

1. Each friend has some pieces of the puzzle.
2. You collect missing pieces from multiple friends at the same time.
3. As soon as you get pieces, you share them with others who need them.
4. The puzzle is completed faster because everyone contributes simultaneously.

#### Roles in BitTorrent:

- **Seeder:** Peer who has the complete file and shares pieces.
- **Leecher:** Peer who is downloading the file but may also upload pieces it already has.
- **Tracker:** Optional server that keeps a list of peers for coordination. Tracks peers participating in torrent.
- **Torrent:** Group of peers exchanging chunks of file. 

#### Advantages:

- Faster downloads as more peers join.
- Reduces server bandwidth cost.
- Highly scalable and efficient.

**In short:**

**BitTorrent =** P2P file-sharing protocol, splits files into chunks, peers while downloading, upload chunks to other peers simultaneously, uses tracker or DHT, faster and scalable than central server downloads.

### BitTorrent – Tit-for-Tat

Definition:

**Tit-for-tat** is BitTorrent’s peer selection strategy that encourages fairness. Peers prefer to upload data to those who are also uploading to them, creating a mutual exchange of file pieces.

#### Key Points:

- Encourages cooperation among peers.
- Prevents freeloaders (peers who only download but don’t upload).
- Each peer maintains a list of neighbors and ranks them based on upload speed.
- **Optimistic unchoking:** Occasionally allows uploading to a random peer to discover new high-speed partners.
- Works dynamically → peers constantly update who they upload to, based on who reciprocates.

**Benefits:**

- Promotes fairness and cooperation.
- Improves overall download speed.
- Discourages selfish peers from slowing the network.

**In short:**

**Tit-for-tat =** BitTorrent’s strategy where peers upload to those who upload to them, ensures fairness, prevents freeloading, and improves network efficiency.

## Video Streaming and Content Delivery Networks (CDN)

**Definition**:

**Video streaming** is the process of delivering video content over the Internet so users can watch it without downloading the entire file first.  
**CDNs (Content Delivery Networks)** are distributed networks of servers that deliver content to users from the closest or fastest server, reducing delay and congestion.


### Streaming Stored Video (VOD – Video on Demand)

#### Stored Video Streaming:

- The video is pre-recorded and stored on a server.
- Clients request the video and receive a continuous stream of data.
- **Examples:** YouTube, Netflix.

#### Challenges in Stored Video Streaming:

- **Network congestion:** Too many users can slow down delivery.
- **Variable bandwidth:** Users have different connection speeds.
- **Latency:** Delay between request and video playback.
- **Packet loss:** Can cause glitches or buffering.

#### Client-Side Buffering and Playout Delay:

- **Buffering:** Client stores a few seconds of video in advance to handle network variations.
- **Playout delay:** Delay introduced intentionally so that the buffer doesn’t empty, ensuring smooth playback.
- **Trade-off:** Larger buffer → smoother playback but longer startup delay.

### Role of CDN in Video Streaming:

- CDN servers are distributed globally.
- Serve video from a server closest to the user, reducing latency and congestion.
- Support high scalability by balancing load across multiple servers.
- **Example:** Watching Netflix in India may pull content from a server in Mumbai instead of the US.



### In short:

- **Video streaming:** Watch video without full download.  
- **Stored video (VOD):** Pre-recorded, streamed continuously.  
- **Challenges:** Congestion, bandwidth, latency, packet loss.  
- **Buffering:** Client stores data ahead; playout delay ensures smooth playback.  
- **CDN:** Distributed servers, reduce latency, handle high load, deliver faster.

### Streaming Multimedia: DASH (Dynamic Adaptive Streaming over HTTP)

**Definition**:
**DASH** is a video streaming technique that allows clients to adaptively adjust video quality based on current network conditions, ensuring smooth playback over HTTP.

**Key Points:**
- Works over standard HTTP, so no special streaming servers needed.
- Video is divided into small segments (chunks), each available in multiple bitrates.
- The client dynamically selects which segment bitrate to download depending on bandwidth.
- Adaptive streaming prevents buffering by lowering quality when the network is slow and increasing quality when bandwidth improves.
- Used by platforms like YouTube, Netflix, and Hulu.


#### Benefits:

- Smooth playback even under fluctuating network conditions.
- Efficient use of network resources.
- Works with existing HTTP/CDN infrastructure.
- Compatible with mobile devices and adaptive networks.

#### In short:
**DASH =** adaptive video streaming over HTTP, divides video into segments, client selects quality based on bandwidth, reduces buffering, widely used for online video services.

## Socket

**Definition**:

A **socket** is a communication endpoint that acts as a “door” between an application process and the end-to-end transport protocol (TCP or UDP). It allows programs to send and receive data over a network.

**Key Points:**

- Works at the transport layer interface for applications.
- Two main types of sockets:

**TCP Socket (Stream Socket):**

- Reliable, connection-oriented.
- Guarantees delivery, order, and error checking.
- **Example:** Web browsing, email (SMTP/IMAP), file transfer.

**UDP Socket (Datagram Socket):**

- Unreliable, connectionless.
- No guarantee of delivery or order, but faster and lightweight.
- **Example:** Video streaming, online gaming, VoIP.

- Socket programming allows applications to communicate over the network using IP addresses and port numbers.
- Every socket is identified by **IP address + port number**.

#### Simple Analogy:

Think of a socket as a door:

- **TCP socket =** a secure, guaranteed delivery courier — checks every packet.
- **UDP socket =** a fast messenger — delivers quickly but may lose some messages.

---

# Transport Layer (Part- 3)

**Recap**: 
- It divides the data into segments.
  - sender: breaks application messages into segments, passes to  network layer
  - receiver: reassembles segments into messages, passes to application layer
  
- It has two protocols-
  - TCP
    - It gives all info.
    - If we want to send data with proper acknowledgement that reciever has recieved the data.
  - UDP
    - We use this protocol when we want to send data faster. We won't be able to know whether the data has been sent or not.

## Multiplexing & Demultiplexing

**Definition**:

**Multiplexing and demultiplexing** are transport-layer services that allow multiple applications to share the network.  
- **Multiplexing:** gathers outgoing data from different apps into segments.  
- **Demultiplexing:** delivers incoming segments to the correct application process.  


**Key Points:**

**Multiplexing (Sender side):**
- Collects data from multiple application processes (e.g., browser, email, music app).
- Adds transport layer headers (with **source & destination port numbers**).
- Sends the segment down to the network layer for delivery.

**Demultiplexing (Receiver side):**
- Transport layer receives segments from the network layer (like a bag of letters).
- Transport layer looks at the destination port number (the “address”) (and sometimes full 4-tuple: source IP, source port, destination IP, destination port)
- Delivers data to the correct application (browser, mail client, etc.)..


## Connectionless vs. Connection-oriented:

- **UDP demux:**  
  Uses **only destination port number** (simpler, less reliable).  
  Example: DNS request on port 53.

- **TCP demux:**  
  Uses **(source IP, source port, destination IP, destination port)**.  
  This allows multiple simultaneous connections to the same port.  
  Example: Two browser tabs both connecting to a web server on port 80.


**Simple Analogy:**
Think of a **post office**:  
- **Multiplexing:** many people drop off letters at one post office → each letter gets an address label.  
- **Demultiplexing:** at the destination, the post office sorts le

### Connection-Oriented vs. Connectionless Demultiplexing

**Definition**:

**Demultiplexing** is how the transport layer delivers incoming segments to the correct application.  
The process differs depending on whether the protocol is **connection-oriented (TCP)** or **connectionless (UDP)**.  


**Key Points:**

**Connectionless Demultiplexing (UDP):**
- Each UDP segment has: **destination port # + source port #**.  
- At receiver: transport layer uses **only the destination port number** to deliver the data.  
- No concept of a “connection” — each segment is treated **independently**.  
- Two different senders can send data to the **same destination port**, and the app will just get them all.  
- **Less overhead, faster**, but no guarantee of **reliability or order**.  

**Connection-Oriented Demultiplexing (TCP):**
- Each TCP segment has: **source IP, source port, destination IP, destination port**.  
- At receiver: transport layer uses this **4-tuple** to identify the correct socket.  
- This allows **multiple connections to the same port**  
  (e.g., 2 browser tabs on port 80 → server distinguishes them using source IP/port).  
- Provides **reliable, ordered delivery** with **flow and congestion control**.  

---

**Simple Analogy:**

- **UDP (connectionless):** Like a **radio station** → anyone can tune in if they know the **frequency (port number)**. Doesn’t matter who sent it.  
- **TCP (connection-oriented):** Like a **phone call** → identified by both caller and receiver numbers (**IP + port**). Multiple people can call the same number, but each call is tracked separately.  

---

**In short:**
- **UDP demux:** Based on **destination port only**, simple but unreliable.  
- **TCP demux:** Based on **(src IP, src port, dest IP, dest port)**, more complex but supports multiple reliable connections.  


## UDP- User Datagram Protocol
- Connectionless
  - No handshaking between sender and reciever.
  - each UDP segment is handeled independently.
- Small header size
- No congestion control

![udp](/images/udp.png)

### UDP: Glance at transport layer

#### UDP- Sender action
- Is passed an application layer message
- Determines UDP segment header file
- Creates UDP segment
- Passes segment to IP

#### UDP- Reciever action
- Recieves segment from IP
- checks UDP checksum header value
- extracts application-layer message
- demultiplexes message up to application via socket

## Principles of Reliable Data Transfer (RDT)

**Definition**:

**Reliable Data Transfer (RDT)** refers to protocols that guarantee **correct, complete, and in-order delivery** of data across a potentially unreliable network.  

---

**Key Points:**

**Main Challenges:**
- Packets may be **lost**.  
- Packets may be **corrupted** (bit errors).  
- Packets may be **duplicated**.  
- Packets may arrive **out of order**.  

---

**Techniques to Ensure Reliability:**

- **Error Detection:**
  - Use **checksums** to detect corrupted data.  
  - Receiver discards or requests **retransmission** if error is detected.  

- **Acknowledgments (ACKs):**
  - Receiver confirms successful receipt of data.  

- **Negative Acknowledgments (NAKs):**
  - Receiver explicitly signals that a packet was **not received** or was **corrupted**.  

- **Retransmissions:**
  - Sender resends packets when **NAK** is received or **ACK** is missing after a **timeout**.  

- **Sequence Numbers:**
  - Every packet is labeled to **detect duplicates** and ensure correct ordering.  

- **Timers:**
  - If sender doesn’t receive **ACK within a certain time**, it retransmits (to handle lost packets).  

### Finite State Machines (FSMs)

**Definition:**

A **Finite State Machine (FSM)** is a mathematical model of a system that can be in one of a **finite number of states** at any given time.  
The system changes states based on **inputs/events** and performs certain **actions** during transitions.  

---

**Key Points:**

- **States:**  
  Possible conditions the system can be in (e.g., *waiting for data*, *waiting for ACK*).  

- **Events (Inputs):**  
  External triggers that cause a state change (e.g., *packet received*, *timeout expired*).  

- **Transitions:**  
  Rules for moving from one state to another, often with an associated action  
  (e.g., retransmit packet, send ACK).  

- **Actions:**  
  Operations performed during transitions (e.g., deliver data to app, resend packet).  


**Usage in Networking:**

- **Reliable Data Transfer protocols** (e.g., RDT 2.2, RDT 3.0) are specified using FSMs.  
- Sender and receiver each have their own FSM.  
- Helps visualize how the system behaves under **loss, corruption, or success**.  


**Simple Analogy:**

Think of FSM as a **traffic light system**:
- **States** = Red, Yellow, Green.  
- **Events** = Timer expires, pedestrian button pressed.  
- **Transitions** = Green → Yellow → Red.  
- **Actions** = “Stop cars,” “Allow crossing.”  

Only a few possible states, and transitions happen based on clear rules.  


**Networking Example (RDT Sender FSM):**

- **State:** “Wait for call from above.”  
  - **Event:** Application gives data → **Action:** Send packet, move to “Wait for ACK.”  

- **State:** “Wait for ACK.”  
  - **Event:** ACK received → **Action:** Deliver success, return to “Wait for call.”  
  - **Event:** Timeout → **Action:** Retransmit packet, stay in “Wait for ACK.”  


**In short:**
- **FSM = system model** with limited states, transitions based on inputs, and actions tied to transitions.  
- In networking → makes sender/receiver behavior clear in reliable data transfer.  

### RDT 1.0- **Reliable transfer over a reliable channel**

- Underlying channel is perfectly reliable
- No bit errors
- No packet loss
- Separate FSM for sender and reciever
  - Sender sebds data while reciever recieves data from underlying channel.

### RDT 2.0- **Channel with bit errors**
- Underlying channel may flip bits in packets.
  - checksum (e.g., Internet checksum) to detect bit errors

#### Recovery from errors
- **acknowledgements (ACKs):** receiver explicitly tells sender that pkt received OK
- **negative acknowledgements (NAKs):** receiver explicitly tells sender that pkt had errors
  - sender retransmits pkt on receipt of NAK

Sender sends one packet and then waits for reciever response.

#### What if ack or nak are corrupted
- Sender doesnt know what happened at reciever end.
- Sending packet again may result in duplication at reciever.

So to handle duplicates-
- sender retransmits current pkt if ACK/NAK corrupted
- sender adds sequence number to each pkt
- receiver discards (doesn’t deliver up) duplicate pkt

### RDT 3.0- **channels with errors and loss**

Underlying channel can also lose packets.

- sender waits “reasonable” amount of time for ACK 
- retransmits if no ACK received in this time
- if pkt (or ACK) just delayed (not lost):
  - retransmission will be  duplicate, but seq #s already handles this!
  - receiver must specify seq # of packet being ACKed
- use countdown timer to interrupt after “reasonable” amount of time

![rdta](/images/rdta.gif)
![rdtb](/images/rdtb.gif)
![rdtc](/images/rdtc.gif)
![rdtd](/images/rdtd.gif)
![rdt](/images/rdt.png)
![rdt2](/images/rdt2.png)

### Go-Back-N (GBN) Sender

**Definition:**

**Go-Back-N (GBN)** is a **sliding window protocol** for reliable data transfer.  
The sender can transmit multiple packets (up to **N**) without waiting for an ACK,  
but must **go back and retransmit** from a lost packet if any error/loss occurs.  

**Key Points (Sender Side):**

- **Sliding Window:**  
  - Window size = **N**.  
  - Sender can send packets with sequence numbers in the window.  
  - Must wait if the window is full.  

- **Sequence Numbers:**  
  - Each packet has a unique sequence number (modulo some max).  
  - Helps receiver maintain correct order.  

- **ACK Handling:**  
  - Receiver sends **cumulative ACKs** (ACK n = “I got everything up to n−1”).  
  - If packet *k* is lost → sender won’t get ACKs for *k+1, k+2…*  

- **Timeout:**  
  - Sender starts a timer when the **first unACKed packet** is sent.  
  - If timeout expires before ACK → retransmit **all unACKed packets** (not just the lost one).  

#### Analogy:
Like sending homework pages through a class monitor:  
- You can give up to **5 pages at once** (window size = 5).  
- If the **3rd page is lost**, teacher only acknowledges pages 1–2.  
- You must resend **page 3, 4, and 5** again → go back to the lost one.  

#### FSM (Sender Simplified):
- **State:** Ready to send if window not full.  
  - **Event:** App data → create packet with seq #, send, start timer if first in window.  

- **State:** Waiting for ACK.  
  - **Event:** Valid ACK received → slide window forward.  
  - **Event:** Timeout → retransmit all unACKed packets.  

**In short:**  
- **GBN Sender = sliding window protocol** where sender can send **N packets**,  
  but on loss must retransmit **all unACKed packets** starting from the lost one.  

![GBN](/images/GBN.gif)

### Selective Repeat (SR) ARQ

**Definition:**  
Selective Repeat is a **sliding window protocol** for reliable data transfer.  
Unlike Go-Back-N, the sender retransmits **only the lost/unacknowledged packet** instead of the whole window.

**Key Points**

**Sender Side:**  
- Maintains a window of size **N**.  
- Can send multiple packets without waiting for ACKs.  
- If a packet times out → only that packet is retransmitted.  

**Receiver Side:**  
- Accepts out-of-order packets and **buffers** them.  
- Sends an ACK for **every correctly received packet**.  
- Once missing packets arrive, buffered packets are delivered in order to the application.  

#### Example
Window size = 4, sender sends packets **0, 1, 2, 3**.  

- Receiver gets 0, 2, 3 (but **1** is lost).  
- Receiver ACKs 0, 2, 3 and buffers 2, 3.  
- Sender times out for packet 1 → retransmits **only packet 1**.  
- Once 1 arrives, receiver delivers **0,1,2,3** in order.  

#### Comparison with Go-Back-N

| Feature               | Go-Back-N                     | Selective Repeat              |
|------------------------|--------------------------------|--------------------------------|
| ACKs                  | **Cumulative** (ACK n → all ≤ n received) | **Individual** for each packet |
| Receiver              | **Discards** out-of-order packets | **Buffers** out-of-order packets |
| Sender Retransmission | Retransmits **all unACKed** packets after loss | Retransmits **only lost** packet |
| Efficiency            | **Lower** (wasteful retransmissions) | **Higher** (fewer retransmissions, more buffer use) |

#### Analogy
Think of mailing assignments:  

- In **GBN**, if page 2 is lost, you resend pages 2,3,4 again.  
- In **SR**, you resend **only page 2**, since the teacher already saved pages 3 and 4.  

![SR](/images/S.gif)

## TCP - Transission Control Protocol

- Connection oriented
  - Handshaking- initializes sender, receiver state before data exchange
- Point to point
  - One sender and one reciever
- bi-directional data flow in same connection


![tcp](/images/tcp.png)

### Sequence Number in TCP

**Definition:**

The **Sequence Number (seq #)** in TCP is a number assigned to each **byte of data** in a TCP connection.  
It tells the receiver the **order of bytes** and ensures **reliable, in-order delivery**.  

**Key Points:**

- Each byte of data has a unique number.  
- The **seq # field** in a TCP segment header = number of the **first byte** in that segment’s data.  
- Helps receiver reassemble data correctly, even if packets arrive out of order.  
- Used for detecting **lost or duplicate segments**.  
- Works with **ACK # (acknowledgment number)** → tells sender “I’ve received everything up to byte X.”  

#### Simple Example:
App wants to send: **“HELLO”** (5 bytes).  
Initial Sequence Number (ISN) chosen = **1000**.  

- **Segment 1:** “HEL” → Seq # = 1000 (covers bytes 1000–1002)  
- **Segment 2:** “LO” → Seq # = 1003 (covers bytes 1003–1004)  

Receiver uses sequence numbers to reorder correctly.  

#### Analogy:
Think of **sequence numbers like page numbers in a book**:  
- Each page has a number.  
- If pages get shuffled, you can still reorder them.  
- The reader can say, *“I’ve read up to page 50”* (like ACK).  

**In short:**  
- **Seq # = position of the first byte in the segment** → ensures **ordered, reliable delivery**.  


### TCP steps-
**Event**- data received from application layer
- Create segment with seq #
- start timer if not already running 

**Event**- Timeout
- retransmit segment that caused timeout
- Resart timer

**Event**- ACK recieved
- if ACK acknowledges previously unACKed segments
  - update what is known to be ACKed
  - start timer if there are  still unACKed segments

### TCP Premature Timeout

**Definition:**  
A **premature timeout** occurs when TCP’s retransmission timer expires **before the actual segment is lost**, causing the sender to retransmit unnecessarily.  

**Key Points**

**Cause:**  
- The estimated **RTT (Round-Trip Time)** is shorter than the actual RTT due to **network delays, congestion, or jitter**.  
- TCP thinks the packet is lost when it is actually still in transit.  

**Effect:**  
- Unnecessary retransmission of segments.  
- Can lead to **duplicate packets** at the receiver.  
- Causes **spurious congestion control**, slowing down the transmission rate.  

**How TCP Handles It:**  
- **Adaptive RTT Estimation:** TCP continuously updates **EstimatedRTT** and **TimeoutInterval** using **smoothed RTT (SRTT)** and deviation.  
- **Duplicate ACKs:** If the retransmission was unnecessary, the receiver’s ACKs prevent further retransmissions.  

#### Simple Analogy
Imagine sending a letter to a friend and expecting it in 3 days:  
- You think it’s lost and send another copy on day 3.  
- In reality, the first letter was just delayed and arrives on day 4.  
- That extra letter = **premature retransmission**.  

**In short:**  
- **TCP premature timeout = timer expires too early** → unnecessary retransmission → may reduce throughput.  
- Controlled by **smoothed RTT & adaptive timeout** to reduce false retransmissions.  

### TCP Flow Control

**Definition:**  
**Flow control** is a mechanism in TCP to ensure that the sender does not overwhelm the receiver.  
It regulates the rate at which the sender transmits data so that the **receiver’s socket buffer** does not overflow.  

**Scenario:**  
- Network layer delivers data faster than the **application layer** can read from the socket buffer.  
- Receiver’s buffer starts filling up.  

**What happens next:**  

**Receiver Advertises a Window Size:**  
- TCP header has a **receiver window (rwnd)** field indicating available buffer space.  

**Buffer Nearly Full → rwnd Shrinks:**  
- Receiver tells sender how much space is left.  
- If buffer is full → **rwnd = 0**.  

**Sender Stops Sending:**  
- Sender stops transmitting new data until it receives a **window update** from the receiver.  

**Resume Transmission:**  
- Once application reads data from buffer → buffer frees space → receiver advertises **new window** → sender resumes sending.  

#### Simple Analogy
Think of a **conveyor belt** delivering packages (network layer) to a **warehouse** (socket buffer):  
- If the workers (application layer) are slow in taking packages off the belt,  
  the belt will eventually **stop accepting more packages** until workers catch up.  

**In short:**  
- If network delivers data faster than the app reads it → TCP **slows down the sender using flow control** → avoids buffer overflow → ensures reliable data delivery.  

### TCP Handshakes

**Definition:**  
A **handshake** is a process used to establish a **TCP connection** between a sender and a receiver before actual data transfer.  
TCP uses a **3-way handshake** for reliable connections.  
Sometimes, a **2-way handshake** is mentioned conceptually, but TCP standard is **3-way**.  

---

### 3-Way Handshake (Standard TCP Connection Setup)

**Key Points:**

**SYN (Synchronize):**  
- **Client → Server**  
- Client sends a segment with **SYN = 1** and **initial sequence number (ISN)**.  
- Purpose: request connection and start sequence numbering.  

**SYN-ACK (Synchronize + Acknowledge):**  
- **Server → Client**  
- Server sends **SYN = 1** (its own ISN) and **ACK = client’s ISN + 1**.  
- Purpose: acknowledge client’s request and agree on its own sequence number.  

**ACK (Acknowledge):**  
- **Client → Server**  
- Client sends **ACK = server’s ISN + 1**.  
- Connection established → data transfer can begin.  

#### Analogy
- Client = person saying “Hi, can we talk?”  
- Server = replies “Hi, I’m ready, here’s my handshake.”  
- Client = “Great, let’s start talking!”  

---

### 2-Way Handshake (Conceptual / Non-standard TCP)

- Some protocols or textbooks mention **2-way handshake** for basic connections:  
  1. Client sends SYN (request)  
  2. Server responds with SYN+ACK (connection established)  

- Problem: Doesn’t handle lost or delayed SYNs reliably → why TCP uses 3-way handshake.  

**In short:**  
- **3-way handshake** = TCP standard → ensures both sides know each other’s ISN → reliable connection.  
- **2-way handshake** = conceptual / unreliable → faster but unsafe in real TCP.  


## Congestion control

**Definition:**  
Congestion control refers to mechanisms that **prevent too much data** from being injected into the network, which can overwhelm routers and links, causing **packet loss, long delays, and degraded performance**.  

---

### Causes of Congestion
- Too many sources sending data simultaneously → network capacity exceeded.  
- Routers have limited buffer space → queues overflow.  
- Sudden bursts of traffic → temporary overloads.  
- Slow links compared to fast senders → bottlenecks occur.  

---

### Costs of Congestion

**Packet Loss:**  
- Buffers overflow → packets are dropped.  
- Retransmissions add extra traffic → worsening congestion.  

**Increased Delay:**  
- Packets wait longer in queues → round-trip time increases.  

**Lower Throughput / Wasted Bandwidth:**  
- Some packets lost → bandwidth used for retransmissions is wasted.  

**Unfairness:**  
- Some flows may dominate the network, others starve.  

---

### Mechanisms of Congestion Control (TCP Example)
- **Window-based control:** Adjust sender’s window size according to network feedback.  
- **Slow Start:** Begin sending slowly, increase window gradually.  
- **Congestion Avoidance:** Detect congestion early (packet loss or delay) and reduce sending rate.  
- **Fast Retransmit / Fast Recovery:** Quickly retransmit lost packets without waiting for timeout.  

---

### Simple Analogy
Think of a **highway with many cars (packets)**:  
- Congestion occurs when too many cars enter too fast → traffic jam, accidents, delays.  
- **Congestion control** = traffic lights + speed limits → regulate flow, avoid jams, ensure fair travel.  

**In short:**  
- Congestion control = techniques to **avoid network overload**.  
- **Causes:** too many senders, limited buffers, sudden bursts, bottlenecks.  
- **Costs:** packet loss, delay, wasted bandwidth, unfairness.  
- Implemented via TCP mechanisms like **slow start, congestion avoidance, and window adjustment**.  

### TCP Congestion Control: AIMD

**Definition:**  
AIMD stands for **Additive Increase, Multiplicative Decrease**, a strategy TCP uses to adjust its **congestion window (cwnd)** to efficiently use network bandwidth while avoiding congestion.  

---

### Key Points

**Additive Increase (AI):**  
- TCP slowly increases the **congestion window** to probe for available bandwidth.  
- Usually increases **1 MSS (Maximum Segment Size) per RTT**.  
- Purpose: gradually find the network’s capacity without causing congestion.  

**Multiplicative Decrease (MD):**  
- When congestion is detected (packet loss or timeout), TCP reduces **cwnd** drastically.  
- Usually halves the **cwnd**.  
- Purpose: quickly relieve congestion in the network.  

---

### How it works (Timeline Example)
- Initial cwnd = 1 MSS.  
- No packet loss → cwnd increases linearly (1, 2, 3, …) → **Additive Increase**.  
- Packet loss detected → cwnd reduces by half → **Multiplicative Decrease**.  
- Repeat → cwnd grows again until next congestion.  

**Graphically:**  
- cwnd vs time = **sawtooth pattern**: slow linear growth + sharp drop on congestion.  

---

### Why AIMD?
- Ensures **fairness** among multiple TCP flows.  
- Efficiently uses network bandwidth without causing persistent congestion.  
- Balances **throughput vs stability**.  

---

### Simple Analogy
Imagine driving a car on a narrow road:  
- **Additive Increase** = slowly accelerate when road is clear.  
- **Multiplicative Decrease** = brake sharply when traffic jam appears.  
- Repeat → smooth flow without crashes.  

**In short:**  
- TCP congestion control uses **AIMD** →  
  - Increase slowly (**additive**) to utilize bandwidth.  
  - Decrease sharply (**multiplicative**) on congestion → stable and fair network use.  

# Network Layer (Part- 4)
- Assigns and uses IP addresses (IPv4/IPv6)
- Decides the best path for data to travel from source to destination.
- Breaks large packets into smaller fragments when needed
- Reassembles them at the destination.
- The Network Layer is like Google Maps for data: It gives addresses, finds the best path, and ensures packets reach across networks.

**Definition:**  
The **Network Layer** is responsible for moving packets (datagrams) from the sending host to the receiving host across multiple routers.  
It provides **host-to-host delivery**, deciding the packet’s path and forwarding it through the network.

---

### Key Points

#### Host Responsibilities (Sender & Receiver):

**Sender:**  
- Takes transport-layer segments.  
- Encapsulates them into **IP datagrams**.  
- Passes datagrams down to the link layer (data link layer) for transmission.  

**Receiver:**  
- Receives datagrams from the link layer.  
- Extracts the segment from the datagram.  
- Delivers the segment to the appropriate **transport-layer protocol (TCP/UDP)**.  

---

### Network Layer Protocols (Present in Every Device)
- Every host and router runs network-layer protocols like **IP, ICMP, routing protocols, ARP (indirectly)**.  
- Handles **addressing, routing, fragmentation, and forwarding**.  

---

### Router Responsibilities
- Routers operate **ONLY** in the network layer.  
- They:  
  - Examine IP header fields (destination address, TTL, checksum, etc.).  
  - Decide the output port to forward the packet.  
  - Move datagrams from **input interface → switching fabric → output interface**.  
- Routers **do not** look at transport layer (TCP/UDP) or application data.  

---

### Main Network Layer Functions

#### 1. Forwarding
- Moving a datagram from an **input link → correct output link**.  
- Happens per-router, very fast.  
- Uses **forwarding tables**.  

#### 2. Routing
- Deciding the **entire path** a packet should take from source to destination.  
- Uses algorithms like:  
  - **Link-State** (e.g., OSPF)  
  - **Distance-Vector** (e.g., RIP)  
  - **Path-Vector** (e.g., BGP)  

Routing = overall **“trip plan”**  
Forwarding = each **“turn”** along the way  

---

### Simple Analogy
Think of taking a road trip:  
- **Routing** = planning the full route from City A to City B using Google Maps.  
- **Forwarding** = at every intersection, choosing the correct road to stay on the planned route.  

Routing = the **big picture**  
Forwarding = **local decisions** at every router  

---

**In short:**  
- Network layer = moves packets **host-to-host** across the network.  
- **Sender:** encapsulates segment → datagram.  
- **Receiver:** delivers segment to transport layer.  
- **Routers:** examine headers, forward datagrams.  
- **Forwarding:** local per-router movement.  
- **Routing:** global path selection using routing algorithms.  

### Data Plane vs Control Plane

**Definition:**  
In the network layer, the **data plane** and **control plane** are two distinct functions inside routers and switches.  
- **Data Plane** → handles actual **packet forwarding**.  
- **Control Plane** → handles **route computation** and decision-making.  

---

### Key Points

#### Data Plane (Forwarding Plane)

**What it does:**  
- Moves packets from an **input port → correct output port**.  
- Implements forwarding based on the **forwarding table**.  
- Operates **locally** within each router.  
- Must be **fast**, often hardware-accelerated (**ASICs**).  

**Characteristics:**  
- Per-packet operation.  
- Uses forwarding table, **not** routing algorithms.  
- Happens in **microseconds**.  

**Examples:**  
- Looking at destination IP and sending packet out **port 3**.  
- Applying NAT, firewall rules, or queue scheduling.  


#### Control Plane

**What it does:**  
- Computes the **paths** packets should take across the network.  
- Builds and updates the **routing table** using routing algorithms.  
- Installs forwarding rules into the **data plane**.  

**Characteristics:**  
- Runs **network-wide algorithms** (OSPF, RIP, BGP).  
- Slower, CPU-driven → runs in **milliseconds to seconds**.  
- Determines the **big picture** of packet travel.  

**Two Types of Control Plane:**  
- **Traditional routers:** control plane runs inside each router.  
- **SDN (Software Defined Networking):** control plane is **centralized** in a controller (ONOS, OpenDaylight).  

---

### Simple Analogy

Think of a **city transportation system**:

- **Control Plane = City’s planning department**  
  - Decides routes, one-way roads, traffic rules.  
  - Determines how cars should move.  

- **Data Plane = Actual traffic on the roads**  
  - Cars move according to the rules.  
  - Each intersection (router) sends cars based on signs (forwarding table).  

Control plane = **planning**  
Data plane = **execution**  


**Note** - Each router has its own data plane and control plane (unless using SDN). This means that each router makes its own forwarding decisions based on its control plane's routing computations and maintains its own forwarding table for packet handling.
In short: each router has its own control plane and makes its own routing decisions.

**Note** - In Software-Defined Networking (SDN), the control plane is moved out of routers and placed in a central software controller. Routing decisions and network logic are controlled by a central software controller, instead of each router calculating paths individually.Routers become simple forwarding devices (also called switches), while the controller does the “thinking.”

## Network service model
A Network Service Model defines the type of services the network layer provides to the transport layer or to the end-hosts.

**In simple words:**

- It describes how data packets will be treated while traveling from sender to receiver.

**It answers questions like:**

- Will packets be delivered reliably?

- Will packets arrive in order?

- Will the network guarantee speed or bandwidth?

- Will packets be dropped or delayed?

## Switching fabric
A switching fabric is the internal network inside a router or switch that connects its input ports to its output ports. Think of it as the internal highway system that forwards packets from one port to another.

### Types of  Switching Fabrics:

1. **Memory-Based Switching Fabric:**
   - CPU copies packet from input port → memory → output port
   - Simple but can be slow due to memory access times.
   - Slowest, limited by memory speed
   - Used in old routers

2. **Bus-Based Switching Fabric:**
   - A shared bus (high-speed channel) connects all ports
   - Input port places packet on bus → output port picks it
   - Faster than memory-based
   - But only one packet can use bus at a time → bottleneck
   - Can become a bottleneck under heavy load.

3. **Interconnection Network Fabric:**
   - Uses a network of switches (like crossbar switches) to connect ports
   - A grid of paths connecting all input ports to all output ports
   - Multiple packets can be transferred in parallel
   - Very high speed
   - Scales better for high port counts
   - More complex and expensive
   - Used in high-performance routers and switches

## Input port queueing

Input Port Queueing (IPQ) occurs when incoming packets at a router/switch wait in a queue at the input port because the switching fabric or output port cannot handle them immediately.

**Why Does It Happen?**

When a packet arrives at an input port:

- The router must look up the forwarding table.

- Then the packet must move through the switching fabric to the correct output port.

**If:**

- the switching fabric is busy

- or the output port is congested

- or many packets want to go to the same output port

- The input port holds the packets in a queue.


### Head-of-Line (HOL) Blocking

The first packet in the queue blocks others behind it, even if those packets could go to free output ports. This reduces throughput and causes delays.

Example:

- First packet waiting for Output Port 2

- Packets behind it want Output Port 5 (which is free)

- But they cannot move until the first one moves → BLOCKED

Thus ultimately input port queueing can lead to HOL blocking, reducing overall router performance, packet loss, and increased delay.

## Output port queueing
Output Port Queuing (OPQ) occurs when packets are first transferred through the switching fabric and then wait in a queue at the output port before being transmitted on the outgoing link.

**Why Does Output Port Queuing Happen?**

A router/switch has:
- Fast switching fabric
- Slower output transmission line
- If multiple packets arrive at the same output port at the same time, the link can transmit only one packet at a time.

**So**:

- Extra packets accumulate in the output buffer → output queueing

So buffering is required at the output port when datagrams arrive from fabric faster than link transmission rate to hold packets waiting to be transmitted.

Now if this buffer gets full, new incoming packets will be dropped, leading to packet loss.

So advanced scheduling algorithms such as **FIFO, Priority Queuing, or Weighted Fair Queuing, Round Robin** are often used to manage output port queues effectively and ensure fair access to the output link.

### Buffer management
To prevent output port queue overflow and packet loss, routers implement buffer management techniques such as:

- **Tail Drop:** Simple method where packets arriving at a full buffer are dropped.
- **Prioritized Queuing:** Higher priority packets are transmitted first.
- **Random Early Detection (RED):** Proactively drops packets before the buffer is full to signal congestion.
- **Weighted Random Early Detection (WRED):** Similar to RED but considers packet priority for dropping decisions.
- **Explicit Congestion Notification (ECN):** Marks packets instead of dropping them to signal congestion to endpoints.

### Packet Scheduling
Routers use scheduling algorithms to determine the order in which packets are transmitted from the output port queue. Common algorithms include:
- **First-In-First-Out (FIFO):** Packets are transmitted in the order they arrive.
- **Priority Queuing:** Packets are classified into different priority levels, and higher priority packets are transmitted first.
- **Weighted Fair Queuing (WFQ):** Allocates bandwidth fairly among different flows based
- **Round Robin:** Cycles through queues to give each flow a chance to transmit.

**Network neutrality :**

Network neutrality is the principle that all internet traffic should be treated equally by Internet Service Providers (ISPs), without discrimination or preferential treatment based on content, user, platform, application, or type of device.

## The bigger picture of network layer- What ecactly happens

**The Two Main Jobs of the Network Layer**
1. **Forwarding** (Move packets from input port → output port inside a router)

   - This is a per-router operation.
   - Very fast. Hardware-based.

2. **Routing** (Selecting the path packets will take across networks)

   - This is a network-wide operation.
   - Slower. Algorithm-based.

**(A) Inside Each Router — What Happens?**

Routers run the Network Layer on all input/output ports.

**Step-by-step internal workflow:**
1. Packet Arrives at Input Port

   - Router receives an IP packet.

   - Performs error checks.

   - Removes Layer 2 header.

2. Lookup the Destination IP

   - Router checks forwarding table.

   - Matches destination IP → finds the correct output port.

3. Queueing

   - Based on congestion:

      - Input port queueing (if switching fabric is busy)

      - Output port queueing (if outgoing link is slow or busy)
4. Switching Fabric Transfers Packet

   - Moves the packet from input → output port using:

   - Memory-based switching

   - Bus-based switching

   - Crossbar switching (modern routers)
5. Add New Link-Layer Header

   - Output port adds a new Ethernet/PPP header for the next hop.

6. Packet Sent Out

   - Packet is transmitted on the outgoing link toward the next router.
  
**(B) Network-Wide — Routing Process**
Routing algorithms run in the background:

- OSPF (Link state)

- RIP (Distance vector)

- BGP (Between autonomous systems)

These build the routing tables, which then generate forwarding tables.

This gives the router a global or semi-global view of the network.

## IP Addressing
It is a 32-bit identifier associated with each host or router interface.

### Subnet
A subnet is a logically divided portion of an IP network, created by splitting a larger network into smaller subnetworks using a subnet mask.

A subnet is just a smaller network inside a bigger network.


Subnets are used to:

- Reduce network congestion
- Improve security by isolating departments
- Use IP addresses more efficiently
- Control broadcast traffic
- Organize large networks like campuses or enterprises

**Real Internet Example (College)**

A college has ONE big network, e.g.:

`10.0.0.0/8`


But they divide it into smaller groups:

`10.0.1.0/24` → CSE Dept

`10.0.2.0/24` → ECE Dept

`10.0.3.0/24` → Library

`10.0.4.0/24` → Hostels

These smaller groups are called subnets.

**Why?** 

To organize the network and reduce traffic.


### CIDR Notation
CIDR is a method of allocating IP addresses using variable-length subnet masks (VLSM), written in the format IP/prefix-length, which specifies how many bits represent the network part.

Examples:

- 192.168.1.0/24

- 10.0.0.0/8

- 172.16.5.0/27

The prefix length tells how many bits are for the network part.

#### What does 10.0.0.0/8 mean?

The format is:

**IP address / prefix length**

So **10.0.0.0** is the **network address**,  
and **/8** tells how many bits are used for the network part.


#### 1. What is the meaning of 10.0.0.0?

**10.0.0.0 is NOT a device IP.**  
It is the **starting base address** of a whole network.

Think of it like:

- Roll number **1** identifies a whole class,  
  not a specific student.

Similarly:

- **10.0.0.0** identifies the **entire network**, not a host.

It is called the **Network ID**.

#### 2. What does /8 mean?

**/8 means:**

- First **8 bits** → **network part**  
- Remaining **24 bits** → **host part**

IP addresses are 32 bits: `[ 8 bits: Network ][ 24 bits: Hosts ]`


So **/8** tells you:

- All addresses starting with **10.xxx.xxx.xxx**  
belong to this network.

---

#### How big is the network 10.0.0.0/8?

It includes all IPs from:

**10.0.0.0 to 10.255.255.255**

That is **16,777,216 IP addresses** (≈ 16 million).

This whole block belongs to **private IP range**,  
free to use inside any organization.

---

#### Why do colleges or companies use 10.0.0.0/8?

Because:

- /8 gives a **huge range** (16 million IPs)  
- They can split it into **thousands of smaller subnets**  
- It is **private**, so no ISP permission needed  

It’s like getting **a big land plot** → then dividing it into **houses**, then **rooms**.

---

#### Subnetting the /8 block

From the big block:

**10.0.0.0/8**

We divide it like:

- **10.0.1.0/24** → CSE Dept  
- **10.0.2.0/24** → ECE Dept  
- **10.0.3.0/24** → Library  
- **10.0.4.0/24** → Hostels  

Each one is a **smaller subnet** inside the big /8.

---

#### Why these are /24 and not /8?

Because:

- **/24 = 256 IPs**  
- Perfect size for a department  

So the large **/8** is cut into many **/24** subnets.

---

#### Summary

**Big network:** 10.0.0.0/8  
- 16 million IPs  
- Parent network  

**Small networks:** 10.0.x.0/24  
- 256 IPs each  
- Child networks (subnets)  




### **How does a host get an IP address within its network (host part)?**

A host gets its IP address through DHCP (Dynamic Host Configuration Protocol) or by manual configuration. DHCP automatically assigns the host part of the address from the network’s available pool.

### **How does a network get its IP address (network part)?**

A network gets its IP address block from its ISP or Internet registries (RIRs). Private networks use reserved private IP ranges without needing official allocation.

1. Assigned by ISP

- For public IP networks:

  - ISPs allocate a block of IP addresses (CIDR block) to organizations.

  - Example: ISP gives 203.0.113.0/24 to a company.

- The company can then subnet it internally.

2. Assigned by Regional Internet Registries (RIRs)

- If the organization is large (e.g., Google, Amazon, universities):

  - They request IP blocks from RIRs like:

    - APNIC (Asia Pacific — India)

    - ARIN (North America)

    - RIPE NCC (Europe)
    - AFRINIC (Africa)

    - LACNIC (Latin America)

    - RIR assigns network prefixes like /12, /16, /20, etc.

3. Private Networks Use Reserved Blocks (No ISP Required)

- Inside LANs (home or office), networks use private IP ranges defined by RFC1918:

  - 10.0.0.0/8

  - 172.16.0.0/12

  - 192.168.0.0/16

- Routers automatically use these without requesting from ISP.

### DHCP client server interaction
1. **DHCP Discover:** Client broadcasts a DHCP Discover message to find available DHCP servers.
2. **DHCP Offer:** DHCP servers respond with a DHCP Offer message, proposing an IP address and configuration.
3. **DHCP Request:** Client selects an offer and sends a DHCP Request message to the chosen server, requesting the offered IP address.
4. **DHCP Acknowledgment:** The DHCP server sends a DHCP Acknowledgment message, confirming the IP address assignment and providing additional configuration details.

![DHCP](/images/DHCP.png)


So basically DHCP assigns IP addresses dynamically to hosts within a private network, managing the host part of the IP address while the network part is assigned by ISPs or RIRs.

### Network Address Translation (NAT)

Network Address Translation (NAT) is a technique used by routers to translate private IP addresses inside a local network to a single public IP address before sending traffic to the Internet.

So exactly what NAT does (detailed explanation):

1. **All devices in your home/college use private IP addresses**

   - Examples of private ranges:

   - 10.0.0.0 – 10.255.255.255 → (10/8)

   - 172.16.0.0 – 172.31.255.255 → (172.16/12)

   - 192.168.0.0 – 192.168.255.255 → (192.168/16)

  - These IPs can only be used inside your local network (LAN).

  - **Example inside home:**

    - Laptop: 192.168.1.10  
    - Phone : 192.168.1.11  
    - TV    : 192.168.1.12


    - These cannot be used on the Internet.

  - **WHY?**

    - Because private IPs are not globally unique and are meant only for internal use.

2. **NAT allows ALL devices to share ONE public IP**

- Your ISP gives you one public IP, example:

  - `103.56.22.9`


- But you have many devices:

  - 192.168.1.10 (laptop)
  - 192.168.1.11 (phone)
  - 192.168.1.12 (TV)
  - 192.168.1.13 (tablet)

- NAT converts all their private IPs to the ONE public IP.

- This is called "**IP address sharing**".

**Advantages:**
- **Only ONE public IP needed**

  - Without NAT:
    - You would need public IP for each device → impossible + costly.

  - With NAT:
    - All private devices → share 1 public IP.

- **You can change private IPs anytime**

  - Example:

    - Change:

    - 192.168.1.10 → 192.168.1.50


  - Internet won’t know or care.

  - Why?

    - Because outside world only sees your public IP, not the private IP.

- **You can change ISP without changing internal IPs**

  - Your internal network:

    - 10.0.0.0/24


  - stays same even if your ISP changes your public IP from:

    - 103.88.20.5 → 49.36.112.7
  - Your laptop still stays 10.0.0.5 inside the network.
  - Only NAT maps it to the new public IP.

- **Security**

- **Devices inside your LAN cannot be directly accessed from the Internet.**

  - For example:
    - Your laptop: 192.168.1.10

  - Someone from outside cannot directly reach:

    - 192.168.1.10:80


  - Because this IP is not visible outside your home.

  - NAT protects your devices by hiding internal IPs.


## IPv6 and Tunneling

### Why IPv6?

IPv4 has only 32-bit addresses (about 4.3 billion). They got exhausted, so IPv6 was introduced.

### What is IPv6?

- 128-bit addresses  
- Example: `2001:0db8:85a3:0000:0000:8a2e:0370:7334`  
- Huge address space  
- No need for NAT  
- Faster routing, auto-configuration, IPSec built-in  

### IPv4 and IPv6 Compatibility Issue

- IPv4 and IPv6 are **incompatible**; many networks still support only IPv4.  
- So IPv6 packets cannot travel through IPv4 networks directly.

### What is IPv6 Tunneling?

**Tunneling = sending IPv6 packets inside IPv4 packets.**

This allows IPv6 networks to communicate across IPv4-only routers.

### Why Tunneling?

Because the world is transitioning from IPv4 → IPv6 slowly.  
Tunneling ensures compatibility without breaking existing networks.

### Types of Tunneling

1. **Manual Tunneling**:  Admin configures IPv4 endpoints and routes manually.

2. **6to4 Tunneling**:  Automatic tunneling using the `2002::/16` IPv6 prefix.

3. **Teredo**: Encapsulates IPv6 inside UDP over IPv4. Works through NAT.

4. **ISATAP**: Used inside enterprises. Treats IPv4 network as virtual IPv6 link.

### How Tunneling Works (Simple)

1. IPv6 host creates IPv6 packet  
2. Router wraps it inside an IPv4 header  
3. IPv4 network transports it  
4. Remote router unwraps it  
5. IPv6 packet reaches destination  

## OpenFlow vs Flow Table Abstraction

### Flow Table Abstraction (Concept)

Flow table abstraction is a **general SDN concept** where packet forwarding is defined using flow entries.

A flow entry consists of:
- **Match fields** (src IP, dst IP, MAC, TCP port, VLAN, etc.)
- **Actions** (forward, drop, modify, send to controller)
- **Counters** (packet/byte statistics)

It is an **abstraction**, meaning it describes *how* forwarding logic should work without defining the exact protocol.  
This concept exists even outside OpenFlow (e.g., P4, Cisco ACI, OVSDB).

### What is OpenFlow?

OpenFlow is a **specific protocol** used in SDN.  
It implements the **flow table abstraction** in a standardized way.

OpenFlow defines:
- Structure of flow tables  
- Allowed match fields  
- Allowed actions  
- Messages between controller ↔ switch (FlowMod, PacketIn, Stats, etc.)

OpenFlow = **the first and most widely known implementation** of the flow-table idea.


### Key Differences

| Feature | Flow Table Abstraction | OpenFlow |
|--------|-------------------------|----------|
| Type | Concept / idea | Real protocol / implementation |
| Purpose | Describe how flows should work | Allow controller to program switches |
| Where used | General SDN theory | SDN systems using OpenFlow |
| Defines match fields? | Conceptually | Precisely (OpenFlow spec) |
| Defines actions? | Conceptually | Strictly defined formats |
| Relationship | Parent idea | Child implementation |
| Device requirement | Any SDN model | Requires OpenFlow-capable switch |



### Simple Summary

- **Flow Table Abstraction** = the **idea** of using match + action rules for forwarding.  
- **OpenFlow** = the **protocol** that implements this idea in real networks.


## Routing Protocols: Distance Vector vs Link State

Routing protocols decide how routers discover paths and build routing tables.  
They fall into two main categories: **Distance Vector** and **Link State**.


### 1. Distance Vector Routing Protocols

#### **Idea**
Routers share routing information with **neighbors only**.  
They advertise the **distance (metric)** to each known network.

#### **Algorithm**
- Bellman–Ford algorithm

#### **How It Works**
- Router sends its full routing table to neighbors  
- Neighbors update their own tables  
- Updates occur periodically

#### **Examples**
- RIP  
- IGRP  

#### **Advantages**
- Simple  
- Low CPU and memory usage  

#### **Disadvantages**
- Slow convergence  
- Routing loops possible  
- Poor scalability



### 2. Link State Routing Protocols

#### **Idea**
Routers share **link-state information with all routers** in the network.  
Each builds a **complete network topology map**.

#### **Algorithm**
- Dijkstra’s SPF (Shortest Path First)

#### **How It Works**
- Routers measure link costs  
- Flood LSAs (Link State Advertisements)  
- Each router computes best paths using SPF  

#### **Examples**
- OSPF  
- IS-IS  

#### **Advantages**
- Fast convergence  
- Loop-free  
- Scalable for large networks  

#### **Disadvantages**
- Higher CPU and memory usage  
- More complex to implement  



### Difference Table

| Feature | Distance Vector | Link State |
|---------|------------------|------------|
| Algorithm | Bellman–Ford | Dijkstra (SPF) |
| Info shared | With neighbors | With all routers |
| View of network | Partial | Complete |
| Convergence | Slow | Fast |
| Routing loops | Possible | Rare |
| Examples | RIP, IGRP | OSPF, IS-IS |
| Resource usage | Low | High |
| Scalability | Small networks | Medium–large |
| Update type | Periodic table updates | Triggered LSAs |



### Summary
**Distance Vector = simple, slow, neighbor-based.**  
**Link State = fast, scalable, full-topology awareness.**

## OSPF (Open Shortest Path First)

OSPF is a **link-state Interior Gateway Protocol (IGP)** used for routing within an Autonomous System.  
It uses **Dijkstra’s SPF algorithm** and maintains a complete map of the network.

### Key Features
- Link-state protocol  
- Uses Dijkstra’s algorithm  
- Fast convergence  
- Supports hierarchical design with **areas**  
- Uses **cost** as metric  
- Open standard  
- Floods LSAs to all routers in an area  

### How OSPF Works
1. Routers discover neighbors  
2. Exchange link-state information  
3. Build Link-State Database (LSDB)  
4. Run Dijkstra’s SPF  
5. Install best routes in routing table  

### Advantages
- Fast and reliable  
- Highly scalable  
- Loop-free  
- Vendor-independent  

### Disadvantages
- More complex than RIP  
- Requires more CPU and memory  

### Summary
**OSPF = Link-state + Dijkstra + Fast + Scalable + Uses areas.**



# Link Layer (Part- 5)

The Link Layer is responsible for reliable data transfer across a single physical link in a network. It provides services such as framing, MAC addressing, error detection, flow control, and medium access control. Protocols like Ethernet and WiFi operate at this layer. It ensures **hop-by-hop** delivery by encapsulating IP packets into frames.

The Link Layer delivers data between two directly connected devices using frames and MAC addresses, not across the whole internet.

**Example-**

- Imagine your laptop is connected to your WiFi router.

- These two devices are directly connected via WiFi.

- You want to open google.com.

- Step-by-step (Link Layer’s Part Only)
  1. **Your laptop wants to send a packet to Google.**

  - But the packet must go through the router first.

  2. **Laptop asks: “What is my router’s MAC address?”**

  - It uses ARP to find the MAC address of the router.

    - **Imagine:**

      - Router’s MAC = AA:BB:CC:11:22:33
      - Laptop’s MAC = 88:99:AA:77:66:55

  3. **Laptop creates a FRAME**

     - **Frame contains:**

       - Destination MAC = Router MAC

       - Source MAC = Laptop MAC

       - Inside: the IP packet for Google

  4. **Laptop sends the frame → Router**

This is a local hop, so only MAC addresses are used.

The Internet is NOT involved yet.

**Important Point**

Even though the laptop wants to communicate with Google,
the Link Layer only helps the laptop communicate with the ROUTER,
because that is the next device in the path.

This is why Link Layer = hop-by-hop delivery only.


**Note**: In each and every host, the link layer is implementd on chip or Network Interface Card (NIC) to handle local delivery over physical links like Ethernet or WiFi.

## Feature

The Link Layer (Layer 2 of OSI model) is responsible for hop-by-hop delivery between directly connected devices. Here are its key functions:


### 1. Framing
Encapsulates network-layer packets (IP packets) into frames.  
A frame includes a header, payload, and trailer.


### 2. MAC Addressing
Uses 48-bit MAC addresses to deliver frames within the same LAN.  
Ensures local (hop-by-hop) communication between devices.


### 3. Error Detection
Detects corrupted frames using:
- CRC (Cyclic Redundancy Check)
- Checksums

Corrupted frames are discarded.


### 4. Error Correction (Optional)
Some link-layer technologies (like WiFi) correct small bit errors.



### 5. Flow Control (Optional)
Prevents a fast sender from overwhelming a slower receiver.  
Examples: Ethernet PAUSE frames, WiFi rate control.


### 6. Medium Access Control (MAC Protocols)
Controls how devices share the communication channel.  
Examples:
- Ethernet: CSMA/CD
- WiFi: CSMA/CA
- Token Ring: Token passing


### 7. Hop-by-Hop Delivery
Ensures frames move from one device to the next (e.g., Laptop → Router).

## Internet Checksum and Cyclic Redundancy Check (CRC)


### 1. Internet Checksum

#### **Purpose**
Detect simple bit errors in packets (used in TCP, UDP, IP).

#### **How It Works**
1. Split data into 16-bit words  
2. Add all words using 1’s complement addition  
3. Take 1’s complement → this becomes the checksum  
4. Receiver adds all words + checksum  
5. If result = all 1’s → no error; else → error detected

#### **Features**
- Simple  
- Low computation  
- Detects basic errors  
- Not very strong (cannot detect burst errors well)

#### **Used In**
- IPv4 header  
- TCP checksum  
- UDP checksum  


### 2. Cyclic Redundancy Check (CRC)

#### **Purpose**
Detect strong, complex, and burst errors in data frames.

#### **How It Works**
1. Treat data as a binary number  
2. Append zeros (equal to size of generator polynomial)  
3. Divide by generator polynomial using binary division  
4. Remainder = CRC bits → appended to frame  
5. Receiver divides again; if remainder = 0 → no error

#### **Features**
- Very strong error detection  
- Catches:
  - Single-bit errors  
  - Double-bit errors  
  - Odd number of bit errors  
  - Burst errors  
- Used in high-speed networks

#### **Used In**
- Ethernet  
- WiFi (802.11)  
- PPP, HDLC  


### Internet Checksum vs CRC

| Feature | Internet Checksum | CRC |
|--------|--------------------|-----|
| Type | Add + 1’s complement | Polynomial division |
| Strength | Weak | Very strong |
| Detects | Basic errors | Burst + complex errors |
| Layers Used | Network/Transport (IP, TCP, UDP) | Link layer (Ethernet, WiFi) |
| Hardware Needed | Very simple | Slightly complex |
| Error Correction | No | No |

## Multiple Access Protocols: Point-to-Point and Broadcast

Multiple access protocols define how nodes share a communication medium.  
There are two types of link settings: **point-to-point** and **broadcast**.


### 1. Point-to-Point Links

#### **Definition**
A point-to-point link connects **exactly two devices**.  
Since only two nodes use the channel, there is **no contention**.

#### **Examples**
- PPP (Point-to-Point Protocol)
- HDLC
- Direct fiber or serial links
- Router-to-router WAN link

#### **Features**
- No collisions  
- No need for CSMA/CD or CSMA/CA  
- Simple link access  
- Handles framing, error detection, and control efficiently  



### 2. Broadcast (Shared) Links

#### **Definition**
A single shared channel used by **multiple devices**.  
Nodes must coordinate who sends data, or collisions occur.

#### **Examples**
- Ethernet LAN
- WiFi (802.11)
- Cable networks
- Satellite networks


### Types of Broadcast Multiple Access Protocols

#### **A. Random Access Protocols**
Nodes transmit whenever they want → collisions may happen.

- ALOHA  
- Slotted ALOHA  
- CSMA (Carrier Sense Multiple Access)  
- CSMA/CD (Ethernet)  
- CSMA/CA (WiFi)


#### **B. Controlled Access Protocols**
Access is coordinated → no collisions.

- Token Ring  
- Token Bus  
- Polling  

#### **C. Channelization Protocols or Channel partitioning**
Channel is divided among users.

- FDMA (Frequency Division Multiple Access)  
- TDMA (Time Division Multiple Access)  
- CDMA (Code Division Multiple Access)  

---

### Point-to-Point vs Broadcast (Comparison)

| Feature | Point-to-Point | Broadcast |
|--------|----------------|-----------|
| Number of devices | 2 | Many |
| Collisions | No | Yes |
| Examples | PPP, HDLC | Ethernet, WiFi |
| Need for multiple access protocol | No | Yes |
| Complexity | Low | High |
| Access control method | Not required | CSMA/CD, CSMA/CA, TDMA, etc. |



### Summary

Point-to-point links connect two nodes and require no multiple access coordination.  
Broadcast links connect many nodes, so multiple access protocols such as ALOHA, CSMA/CD, CSMA/CA, TDMA, and FDMA are required to avoid collisions and manage shared channel access.


## Channel partitioning protocols
Channel partitioning protocols divide the communication channel into separate parts so multiple users can transmit simultaneously without interference. This is essential in broadcast networks where many devices share the same medium.


### 1. FDMA (Frequency Division Multiple Access)

#### **Definition**
The available channel bandwidth is divided into **multiple frequency bands**, and each user is assigned a **separate frequency**.

#### **How It Works**
Each user transmits **at a different frequency**, so signals do not interfere.

#### **Examples**
- Radio broadcasting  
- Analog cellular systems  
- Satellite communication  

#### **Features**
- No collisions  
- Requires guard bands  
- Simple but less efficient  
- Works well for continuous signals  



### 2. TDMA (Time Division Multiple Access)

#### **Definition**
The channel is divided into **time slots**, and each user gets a **specific time slot** to transmit.

#### **How It Works**
Users transmit **one at a time**, in repeated cycles.

`| A | B | C | A | B | C | ...`


#### **Examples**
- GSM (2G mobile network)  
- Digital wireless systems  

#### **Features**
- No collisions  
- Requires clock synchronization  
- Wastes time slots when a user has no data  
- Medium efficiency  



### 3. CDMA (Code Division Multiple Access)

#### **Definition**
All users transmit **at the same time** and **in the same frequency**, but each user is assigned a **unique code**.

#### **How It Works**
Signals are spread using unique orthogonal codes.  
Receiver uses the same code to extract the correct signal.

#### **Examples**
- 3G networks  
- GPS  
- Secure military communication  

#### **Features**
- Very high capacity  
- Resistant to interference  
- Secure (code-based separation)  
- Complex to implement  



---

### FDMA vs TDMA vs CDMA (Comparison)

| Feature | FDMA | TDMA | CDMA |
|--------|-------|-------|-------|
| How channel is shared | Frequency | Time slots | Codes |
| Collisions | No | No | No |
| Synchronization | Low | High | High (code sync) |
| Efficiency | Low | Medium | High |
| Used in | Analog phones, radio | GSM (2G) | 3G, GPS |

---

### Summary

FDMA divides the channel by **frequency**, TDMA divides it by **time**, and CDMA divides it by **codes**.  
All three allow multiple users to share the medium **without collisions**, but CDMA is the most efficient and advanced.

## Random Access Protocols

Random access protocols allow nodes to transmit **whenever they have data**, without prior coordination.  
However, this can lead to **collisions**, so different protocols define how to detect, avoid, or reduce them.


### 1. Pure ALOHA

#### **Definition**
Nodes transmit **immediately** when they have data, without sensing the channel.

#### **Collision Handling**
- Collisions can happen anytime.
- If collision → the node waits a random time and retransmits.

#### **Efficiency**
- Maximum efficiency: **18%**

#### **Features**
- Very simple  
- High collision rate  
- Used in early satellite networks  



### 2. Slotted ALOHA

#### **Definition**
The channel time is divided into **slots**, and nodes can transmit **only at the start of a slot**.

#### **Collision Handling**
- Collisions still occur, but only if two nodes transmit in the same slot.

#### **Efficiency**
- Maximum efficiency: **37%** (double Pure ALOHA)

#### **Features**
- Requires time synchronization  
- Reduces but does not remove collisions  



### 3. CSMA (Carrier Sense Multiple Access)

#### **Definition**
Before transmitting, a node **listens to the channel**.  
If the channel is idle → transmit  
If busy → wait

#### **Features**
- Reduces collisions  
- Still possible due to propagation delay  
- More efficient than ALOHA  

#### **Types**
- **1-persistent**  
- **Non-persistent**  
- **p-persistent**  



### 4. CSMA/CD (Carrier Sense Multiple Access with Collision Detection)

#### **Definition**
Nodes listen before and **during transmission**.  
If a collision is detected → stop immediately and send a **jam signal**.

#### **Used In**
- **Wired Ethernet** (Traditional shared Ethernet)

#### **Features**
- Minimizes time wasted during collisions  
- Not usable in wireless (cannot detect collisions while sending)  



### 5. CSMA/CA (Carrier Sense Multiple Access with Collision Avoidance)

#### **Definition**
Nodes try to **avoid collisions** before they happen using:
- RTS/CTS (Request to Send / Clear to Send)
- Random backoff timers
- Acknowledgments (ACKs)

#### **Used In**
- **WiFi (802.11)**

#### **Features**
- Collision avoidance instead of detection  
- Works well for wireless networks  
- Handles hidden terminal and exposed terminal problems  



---

### Comparison of Random Access Protocols

| Protocol | Sense Before Sending? | Detect Collision? | Avoid Collision? | Used In |
|----------|------------------------|----------------------------|-----------------------------|---------------|
| Pure ALOHA | No | No | No | Early satellite |
| Slotted ALOHA | No (but time-slotted) | No | No | RFID, wireless |
| CSMA | Yes | No | Partially | LAN, wired/wireless |
| CSMA/CD | Yes | Yes | No | Ethernet |
| CSMA/CA | Yes | No | Yes | WiFi (802.11) |

---

### Summary

Random access protocols let nodes transmit freely, but collisions must be handled.  
ALOHA is the simplest, CSMA reduces collisions, CSMA/CD detects them (Ethernet), and CSMA/CA avoids them (WiFi).


## Controlled Access Protocols

Controlled access protocols ensure that **only one node transmits at a time**, preventing collisions.  
These protocols coordinate transmission by giving **explicit permission** to each node.


### 1. Token Ring

#### **Definition**
Nodes are connected in a **logical ring**, and a special small frame called a **token** circulates around the ring.  
A node can transmit **only when it captures the token**.

#### **How It Works**
1. Token circulates from node to node.  
2. Node seizes the token → sends data.  
3. After sending, node releases the token back into the ring.  

#### **Features**
- Collision-free  
- Predictable access time  
- Requires maintaining the ring  
- Used in older LAN technologies (IEEE 802.5)  



### 2. Token Bus

#### **Definition**
Nodes are connected in a **physical bus**, but organized in a **logical ring**.  
The token is passed according to **logical order**, not physical position.

#### **How It Works**
- Token is sent following a predefined logical node sequence.
- Only the node holding the token can transmit.

#### **Features**
- No collisions  
- Good for industrial networks  
- More flexible topology than Token Ring  



### 3. Polling (Master–Slave)

#### **Definition**
A **central master** (controller) asks each node **one by one** if it has data to send.

#### **How It Works**
1. Master sends “poll” to a node  
2. If node has data → sends it  
3. Master polls the next node  
4. Repeats round-robin  

#### **Features**
- No collisions  
- Simple and predictable  
- Single point of failure (master)  
- Delay increases as number of nodes grows  



---

### Comparison of Controlled Access Protocols

| Protocol | Topology | Who Controls Access? | Collisions? | Used In |
|----------|-----------|---------------------------|----------------|------------------------------|
| Token Ring | Logical Ring | Token | No | Older LAN (IEEE 802.5) |
| Token Bus | Physical Bus / Logical Ring | Token | No | Industrial networks |
| Polling | Any | Central Master | No | Low-speed links, WiFi power-saving |

---

### Summary

Controlled access protocols eliminate collisions by giving explicit permission for transmission.  
Token Ring and Token Bus use circulating tokens, while Polling uses a central master to grant transmission rights.

## Summary of MAC (Medium Access Control) Protocols

MAC protocols determine how multiple devices share a communication channel.  
They are grouped into **three major categories**:


### 1. Random Access Protocols

Devices transmit **whenever they want**, so **collisions can occur**.

#### **Examples**
- Pure ALOHA  
- Slotted ALOHA  
- CSMA  
- CSMA/CD (Ethernet)  
- CSMA/CA (WiFi)

#### **Key Idea**
“Try to send — if collision happens, handle or avoid it.”

#### **Pros**
- Simple  
- Good for low traffic

#### **Cons**
- Collisions → wasted time  
- Efficiency reduces under high load



### 2. Channel Partitioning Protocols (Channelization)

The channel is **divided among users**, so **no collisions** occur.

#### **Examples**
- TDMA (Time Division)  
- FDMA (Frequency Division)  
- CDMA (Code Division)

#### **Key Idea**
“Give each user a fixed portion of the channel.”

#### **Pros**
- Collision-free  
- Fair and predictable

#### **Cons**
- Inefficient when few users are active  
- Requires synchronization or complex coding



### 3. Controlled Access Protocols (Taking Turns)

Devices **take turns** transmitting under coordination → **no collisions**.

#### **Examples**
- Token Ring  
- Token Bus  
- Polling (Master–Slave)

#### **Key Idea**
“Nodes transmit only when allowed.”

#### **Pros**
- Collision-free  
- Predictable access (good for real-time systems)

#### **Cons**
- Overhead (token passing, polling)  
- Slow if many nodes  
- Single point of failure in polling



---

### **One-Line Summary**

- **Random Access** → Send anytime; collisions possible  
- **Channel Partitioning** → Divide channel; no collisions  
- **Controlled Access** → Take turns; no collisions


## DOCSIS (Data Over Cable Service Interface Specification)

DOCSIS is a standard that enables **high-speed Internet over cable TV (CATV) networks**.  
It allows ISPs to deliver broadband using the same coaxial cables used for television.

### Key Points
- Used in cable Internet services  
- Communication happens between:
  - **Cable Modem** (home)
  - **CMTS** – Cable Modem Termination System (ISP)
- Works on Hybrid Fiber-Coaxial (HFC) networks  
- Supports both upstream and downstream data

### DOCSIS Versions (Speeds)
- **3.0:** Up to 1 Gbps  
- **3.1:** Up to 10 Gbps  

### Summary
DOCSIS makes it possible to provide fast Internet without replacing old cable TV infrastructure.


## Difference Between Switch and Router

| Feature | Switch | Router |
|---------|---------|---------|
| OSI Layer | Layer 2 (Data Link) | Layer 3 (Network) |
| Uses | MAC addresses | IP addresses |
| Purpose | Connects devices within a LAN | Connects different networks (LAN → WAN/Internet) |
| Forwarding Basis | MAC address table | Routing table |
| Collision Domains | Each port is a separate collision domain | Each interface is a separate collision domain |
| Broadcast Domains | One broadcast domain (unless VLANs) | Breaks broadcast domains |
| NAT Support | No | Yes |
| Routing Protocols | No | Yes (OSPF, RIP, BGP) |
| Packet Type | Forwards frames | Forwards packets |
| Speed | Very fast (hardware switching) | Slightly slower (routing logic) |
| Typical Use | LAN switching | Internet & inter-network communication |

## VLAN (Virtual Local Area Network)

A **VLAN (Virtual LAN)** is a method of logically dividing a physical LAN into multiple separate networks.  
Even if devices are connected to the same physical switch, VLANs keep their traffic isolated.

### **Key Features**
- Creates **separate broadcast domains**
- Improves **security** by isolating departments or groups
- Reduces **broadcast traffic**
- Allows **logical grouping** of users regardless of physical location
- Simplifies **network management**

### **How VLAN Works**
A managed switch assigns specific ports to specific VLANs.

Example:
- Ports 1–5 → VLAN 10  
- Ports 6–10 → VLAN 20  

Devices in different VLANs **cannot communicate** unless connected through a router or Layer-3 switch.

### **Summary**
VLANs divide a large physical network into smaller, isolated logical networks to increase security, reduce traffic, and simplify management.


## MPLS (Multiprotocol Label Switching)

MPLS is a high-speed packet forwarding technology that uses **short labels** instead of long IP address lookups.  
It operates between Layer 2 and Layer 3, often called **Layer 2.5**.

### **Key Features**
- Uses labels for fast forwarding  
- Predefined paths called **Label Switched Paths (LSPs)**  
- Supports traffic engineering and QoS  
- Works with multiple protocols (IP, Ethernet, PPP)

### **How MPLS Works**
1. The **ingress router** adds a label to the packet.  
2. **Label Switch Routers (LSRs)** forward the packet based only on the label.  
3. The **egress router** removes the label and sends the packet normally.

### **Benefits**
- Faster forwarding than IP routing  
- Supports MPLS VPNs  
- Enables traffic engineering  
- Provides high reliability and fast reroute  

### **Summary**
MPLS is a label-based forwarding system that improves speed, supports VPNs, and enhances traffic control in large networks.
