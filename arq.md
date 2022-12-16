## ARQ protocols

ARQ, or Automatic Repeat Request, is a protocol that is used in data transmission to ensure reliable data transfer. It works by having the receiver send back an acknowledgement (ACK) message to the sender, which indicates that the data was received successfully. If the sender does not receive an ACK, it will automatically retransmit the data until an ACK is received. ARQ protocols are used in many communication systems, including cellular networks, satellite communications, and VoIP systems.

The automatic repeat request (ARQ) protocols such as stop and wait, go back N, and selective repeat, operate at the data link layer of the OSI model. The data link layer is responsible for detecting and correcting errors that occur during the transmission of data packets. The ARQ protocols help to ensure reliable data transmission by sending acknowledgements and requesting for retransmission of missing or corrupted packets.

## Types of ARQ

There are several types of ARQ protocols, including Stop-and-Wait, Go-Back-N, Selective-Repeat, and Hybrid ARQ. Stop-and-Wait is the simplest type of ARQ protocol, where the sender sends a single frame of data, and waits for an acknowledgement before sending the next frame. Go-Back-N is an improvement on the Stop-and-Wait protocol, where the sender can send multiple frames before waiting for an acknowledgement. Selective-Repeat is an advanced version of ARQ, where the receiver can request retransmission of specific frames. Finally, Hybrid ARQ is a combination of the other ARQ protocols, allowing for both retransmissions and selective acknowledgements.

## Stop and wait

Stop and wait is a type of automatic repeat request (ARQ) protocol used in computer networks. It is a very simple protocol whereby the sender sends a packet and then waits for an acknowledgement (ACK) from the receiver before sending the next packet. If the ACK is not received within a certain time period, the packet is retransmitted. This protocol ensures that data is reliably transmitted over the network, but it is very inefficient as only one packet can be transmitted at a time.

## Go Back N

Go back N is a type of automatic repeat request (ARQ) protocol used in computer networks. It is a sliding window protocol that allows a sender to resend lost data packets and a receiver to recognize and request for retransmission of missing or corrupted data packets. It can be used as a data link layer protocol in a network with unreliable communications lines. It is a more efficient protocol than stop and wait.

## Selective Repeat

Selective repeat is a type of automatic repeat request (ARQ) protocol used in computer networks. It is an improvement over the Go Back N protocol as it allows multiple packets to be transmitted at once. The sender maintains a sliding window of packets that have yet to be acknowledged. The receiver can selectively request for the retransmission of any missing packets, rather than having to wait for all missing packets to be resent. This protocol is more efficient than both the stop and wait and Go Back N protocol, as it reduces the amount of time spent retransmitting packets.

## Sample Problems

1) A 3000-km long, 1-Mbps link is used to transmit 1000-bit data packets using the Go-Back-N protocol (where the receiver does not buffer out-of-order data packets). The propagation speed is 5 $\mu$sec/km. What is the minimum number of bits that you need for the sequence number, assuming sequence numbers refer to packets (not bytes)? Assume no buffering limitation at the receiver, the channel should be fully utilized, and negligible transmission and processing times for acknowledgments. Take 1M = 1000,000, and note that 1 $\mu$ = 10-6 ! Show your work.

*Answer*: First, let’s calculate RTT of each packet = time to put packet on line + time to send data + time to return data = (1000 bits / 1 Mbps) + 2*(2)(3000)(5$\mu$)=31ms.
Capacity of link = 1Mbps/1000bits = 1000 packets/sec (This is the bandwidth)
*Bandwidth-Delay product = (1000)*(31ms) = 31 packets. 

Ideal Sender Window Size = BD product = 31 packets
Reciever Window Size = 1 (in GBN)
Number of bits needed to represent the sequence number = $log_2(SWS+RWS= 32)$

*Why*? “In practice, a packet’s sequence number is carried in a fixed-length field in the packet header. If k is the number of bits in the packet sequence number field, the range of sequence numbers is thus With a finite range of sequence numbers, all arithmetic involving sequence numbers must then be done using modulo 2 arithmetic. (That is, the sequence number space can be thought of as a ring of size 2 , where sequence number is immediately followed by sequence number 0.) Recall that rdt3.0 had a 1-bit sequence number and a range of sequence numbers of [0,1].”