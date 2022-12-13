## Congestion window size in networks

In computer networking, the congestion window size is a parameter used in network congestion control. It is the maximum amount of data that can be sent over a network connection without receiving an acknowledgment that the data has been received on the other end. The window size is adjusted during the course of data transfers to properly balance the rate at which data is sent and received. This helps to avoid network congestion. The window size is typically adjusted by the sender and is constrained by the size of the network's receive window. The congestion window size is important for ensuring timely data delivery and efficient use of network resources.

Congestion Control protocols in TCP

1. Slow Start
2. Congestion Avoidance
3. Fast Retransmit
4. Fast Recovery
5. Explicit Congestion Notification
6. Selective Acknowledgment (SACK)
7. Time-Based Congestion Control
8. TCP Veno
9. TCP Cubic 
10. BIC-TCP

### Overall categories of congestion control

1. AIMD (Additive Increase Multiplicative Decrease): AIMD is the most commonly used congestion control protocol, and it is the basis of the TCP congestion control algorithm. Additive Increase means that the sender increases its transmission rate by a fixed amount each RTT, while Multiplicative Decrease means that the sender reduces its transmission rate by a fixed factor when it detects congestion. 

2. Window-based Congestion Control: Window-based congestion control protocols use the size of the congestion window as the primary mechanism for controlling the rate of data transmission. This allows the sender to control the rate at which data is sent, depending on the size of the congestion window. 

3. Rate-based Congestion Control: Rate-based congestion control protocols use the rate of data transmission as the primary mechanism for controlling the rate of data transmission. This allows the sender to adjust its transmission rate depending on the current network conditions. 

4. Loss-based Congestion Control: Loss-based congestion control protocols use packet loss as the primary mechanism for controlling the rate of data transmission. This allows the sender to adjust its transmission rate depending on the amount of packet loss that is experienced.

5. Delay-Based Congestion Control: Delay-based congestion control protocols use packet delay as the primary mechanism for controlling the rate of data transmission. This allows the sender to adjust its transmission rate depending on the amount of packet delay that is experienced. 

6. Network-Aware Congestion Control: Network-aware congestion control protocols use information about the network conditions as the primary mechanism for controlling the rate of data transmission. This allows the sender to adjust its transmission rate depending on the overall network conditions.

## Basics: Slow Start

Slow start is a congestion control algorithm used in TCP to gradually increase the amount of data that can be sent over a network in order to prevent congestion. The algorithm works by starting with a small congestion window size, and then doubling that size each Round Trip Time (RTT) until it reaches a predetermined maximum. This allows the sender to gradually increase the amount of data it sends, while giving the network time to adjust to the increased load. Once the congestion window reaches the maximum, the sender will use the congestion avoidance algorithm to maintain the current rate of data transmission.

## Basics: AIMD

AIMD (Additive Increase/Multiplicative Decrease) is a congestion control algorithm used by transport layer protocols such as TCP. The algorithm works by increasing the transmission rate of the sender (additive increase) until a packet loss is detected, which indicates congestion. At this point, the sender decreases the rate (multiplicative decrease) to try and avoid further losses. This process then repeats until the sender finds a rate that allows the packets to be sent without any packet loss. This rate is then the equilibrium rate at which the sender will continue to send packets.

## How does fast retransmission work?

Fast retransmission is a technique used in TCP to detect and recover from lost packets quickly. It works by having the sender continuously monitor the acknowledgments it receives from the receiver. If the sender does not receive an acknowledgment within a certain time period, it will assume that the packet was lost and retransmit it. This allows the sender to quickly detect and recover from packet losses, reducing the overall impact of congestion on the network.

## TCP Reno

TCP Reno is a congestion control algorithm used in TCP to manage network congestion. It is based on the standard TCP algorithm, but with a few modifications. TCP Reno uses the same Slow Start and Congestion Avoidance algorithms as regular TCP, but also implements fast retransmission and fast recovery. Fast retransmission is used to detect and recover from lost packets quickly, while fast recovery allows the sender to increase the congestion window size quickly after a packet loss. This helps to reduce the amount of time needed to recover from packet losses and helps to reduce the overall impact of congestion on the network.

The congestion window size for TCP Reno is given by the equation: 

$W = min(2W_{last}, W_{max}, W_{last}+\alpha \times MSS)$

where $W_{last}$ is the congestion window size in the last RTT, $W_{max}$ is the maximum congestion window size, MSS is the Maximum Segment Size, and $\alpha$ is a scaling factor.

### How widely is TCP Reno used?

TCP Reno is widely used as the default congestion control protocol for the Transmission Control Protocol (TCP) in the Internet. It is the most commonly used implementation of the TCP protocol, and is used by the majority of the world's Internet service providers. It is also used by many applications, such as web browsers and file transfer programs, to ensure reliable data transmission over the Internet.

## Sample Question

Consider sending a large file from one host to another over a TCP-Reno connection. Assume that the connection has reached steady state, and its congestion window is now oscillating between 8 and 16 segments in AIMD (without slow start, i.e. a loss event at congestion window = 16 is always detected by triple duplicate acknowledgments). Assume the TCP source is not limited by flow control.

(a) Assuming approximately constant round-trip times (RTT), where RTT = 100ms, in steady state, how long does it take between two consecutive loss events? Assume that it takes roughly one RTT to detect loss.

*Answer*: 

(b) What is the average sending rate for this connection?

*Answer*: The average sending rate for this connection is 12 segments per round trip time (RTT). This is calculated by taking the average of the congestion window size (8 + 16) / 2. Since the congestion window size oscillates between 8 and 16 segments, the average sending rate is 12 segments per RTT.

(c) Now suppose this connection shares the bottleneck link with another long-lived TCP-Reno connection. What would be the average sending rate of each connection? Assume that both connections have the same RTT and are synchronized in their updates of their congestion windows.

*Answer:* 