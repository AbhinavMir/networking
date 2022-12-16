## Sample questions

![](src/sample_dhcp.png)

*Answer*: For this problem, you can refer to [FAQ](dumb_questions.md) for clarification on what is a *frame*. Every point of communication here will emit a frame. Let’s divide the question into parts.

(a) Assuming this is the only traffic on both Ethernet and wireless LAN, and there are no packet errors or losses, how many frames will be transmitted in the process of DHCP exchange and TCP handshaking exchange over both wireless and Ethernet LAN?

*Answer*: For DHCP exchange, the router will hit the Access Point (AP) first with DHCP broadcast, then it’ll hit the Switch S, then it’ll hit both DHCP server and Router R (since it has no clue where the DHCP server is). The 4 message type request will ask for 4 frames. Since we traversed 4 links, the emitted frames will be 4*4 = 16 frames.

```mermaid
sequenceDiagram
X ->> Access Point: Broadcast (1)
Access Point->> Switch: Broadcast (2)
Switch ->> DHCP server: Broadcast (3)
Switch ->> Router R: Broadcast (4)

```





| higher layer protocol/data | number of frames transmitted | Links |
| -------------------------- | ---------------------------- | ----- |
|                            |                              |       |

