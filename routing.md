## What is routing in networking? 

Routing is the process of selecting paths in a network along which to send network data. Routers create an overlay network by using the routing information exchanged via routing protocols. This information is used to construct a logical map of the network, which can then be used to determine the best path for data to travel from its source to its destination.

### Reviewing old topics

→ Subnetting is the process of dividing a network into smaller subnets. All the subnets are connected and communicate with each other through routers. Each subnet has its own routing table, which is used to route the traffic within the subnet. Routers are used to route the traffic between different subnets. Ref. [subnetting](https://github.com/AbhinavMir/network_grad_notes/blob/main/subnetting.md). 

 ## Distance Vector Routing

Distance-vector routing is a routing protocol that uses a distance vector algorithm to determine the best path for a packet to traverse through a network. A distance vector algorithm calculates the distance (in hops) between the source node and all other nodes in the network. Each node then updates its own routing table to reflect the distances between itself and all other nodes.

**Loops**: Main issue with distance-vector routing is that it can cause routing loops. A routing loop occurs when two or more nodes have incorrect information in their routing tables, causing them to continuously route packets back and forth between each other without ever reaching their intended destination. This results in wasted bandwidth and can lead to network congestion. To prevent routing loops, distance-vector routing protocols use a variety of techniques such as split horizon, route poisoning, and triggered updates.

## Next Hop Routing

Next hop routing is a routing technique used in computer networks. It is a method of determining the next network node to which a packet should be forwarded on its way to its destination. In next hop routing, each router determines the optimal next stop on the packet's journey to its destination. This is done by examining the routing table and choosing the best route based on criteria such as the shortest path, the least amount of hops, or the lowest cost. The router then forwards the packet to the next hop, which is the next router in the path.

### Sample Question



## D-V routing vs NH Routing

Distance Vector routing and Next hop routing are two different types of routing protocols. Distance Vector routing (also known as Bellman-Ford or RIP) is a routing protocol that uses the distance to a destination to determine the best path to take. It sends information about a network's topology to its neighbors, who then use the information to update their own routing tables. Next hop routing is a more efficient routing protocol that sends packets directly to their destination without waiting for information from its neighbors. It uses the concept of a next hop address to determine the best path to take. It is often used in large networks because of its speed and efficiency.

