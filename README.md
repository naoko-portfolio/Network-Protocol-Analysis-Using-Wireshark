# Network Protocol Analysis Using Wireshark

## Overview

This project analyzes what happens behind the scenes when I open google.com.
Using Wireshark, I captured and analyzed DNS, TCP, TLS, and HTTPS-related traffic.

## Environment

- Windows 11
- Microsoft Edge
- Wireshark 4.6.6

## Goal

The goal of this project was to learn how to use Wireshark and understand what it is used for.

At the same time, I wanted to learn how network communication works behind the scenes when I open a website.


## Why I Started This Project

When I first learned Wireshark in class, I did not fully understand what it was or how it worked.

Recently, I watched a YouTube video about Wireshark, and it made me interested in learning more about it.

So, I decided to start this project to better understand Wireshark and real network traffic by capturing and analyzing packets while opening google.com.


## Steps

1. Start packet capture
2. DNS Analysis
3. TCP Analysis
4. TLS Analysis
5. HTTPS Analysis

## Step 1. Start Packet Capture
- Closed all web sites
- 


I started capturing traffic on my Wi-Fi interface using Wireshark.

### Questions I Had

**Q. Why are the packets displayed in different colors?**

Wireshark uses colors to distinguish different protocols and packet types, making network traffic easier to analyze.

## Step 2 - DNS Analysis

The computer first sent a DNS query to look up the IP address of www.google.com.

After receiving the DNS response, it was able to connect to Google's server.

DNS translates a domain name into an IP address before the browser connects to the web server.

## Step 3 - TCP Analysis

The computer established a TCP connection with the web server using the three-way handshake.

The connection was established through the sequence **SYN → SYN, ACK → ACK**.

After the TCP connection was established, the client and the server were ready to exchange data reliably.

## Step 4 - TLS Analysis

After the TCP connection was established, the client and server started the TLS handshake.

The client asked to use TLS, and the server agreed.

After key exchange information was shared, the communication became encrypted.

## Step 5 - HTTPS Analysis

HTTPS traffic appeared as TLS Application Data in Wireshark.

The HTTP content was not readable because it was encrypted by TLS.

## Reflection

Before this project, I thought opening a website involved one simple connection.

By analyzing the packets, I learned that opening one website involves DNS queries, TCP connections, TLS handshakes, and encrypted application data.

This project helped me understand how web browsers communicate securely with servers.
