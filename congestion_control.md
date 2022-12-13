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

## TCP Reno

TCP Reno is a congestion control algorithm used in TCP to manage network congestion. It is based on the standard TCP algorithm, but with a few modifications. TCP Reno uses the same Slow Start and Congestion Avoidance algorithms as regular TCP, but also implements fast retransmission and fast recovery. Fast retransmission is used to detect and recover from lost packets quickly, while fast recovery allows the sender to increase the congestion window size quickly after a packet loss. This helps to reduce the amount of time needed to recover from packet losses and helps to reduce the overall impact of congestion on the network.

## How does fast retransmission work?

Fast retransmission is a technique used in TCP to detect and recover from lost packets quickly. It works by having the sender continuously monitor the acknowledgments it receives from the receiver. If the sender does not receive an acknowledgment within a certain time period, it will assume that the packet was lost and retransmit it. This allows the sender to quickly detect and recover from packet losses, reducing the overall impact of congestion on the network.

The congestion window size for TCP Reno is given by the equation: 

$W = min(2W_{last}, W_{max}, W_{last}+\alpha \times MSS)$

where W_{last} is the congestion window size in the last RTT, W_{max} is the maximum congestion window size, MSS is the Maximum Segment Size, and \alpha is a scaling factor.