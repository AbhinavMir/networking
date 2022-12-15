 ## CIDR 

> An IP (Internet Protocol) address consists of 32 bits and is typically represented as four sets of numbers separated by a period. For example, an IPv4 address may look like 192.168.0.1. Each of the four octets (groups of eight bits) represents a number ranging from 0 - 255, resulting in a total of 32 bits. The full representation of an IP with 32 bits would be a four-part numerical address, such as 192.168.0.1.

CIDR (Classless Inter-Domain Routing) is a way of allocating IP addresses that divides an IP address into two components: the network address and the host address. This allows for more efficient use of IP addresses as it allows for a single network address to be allocated to multiple hosts, allowing for more efficient use of IP address space.

CIDR is based on a hierarchical network addressing system where addresses are divided into blocks of fixed size. Each block is assigned a unique network address, and each address within the block is identified using a unique host address. The size of the block is indicated by a mask, which specifies the number of bits that are used for the network address. The mask is written in the form of a dotted decimal notation, with the number of bits used for the network address indicated in decimal notation.

For example, a CIDR address of 192.168.0.0/24 would indicate that the first 24 bits of the address are used for the network address and the remaining 8 (32-24) bits are used for the host address.

CIDR is used for routing in large networks, such as the Internet, and is becoming increasingly popular as a way of allocating IP addresses. It is also used for assigning IP addresses to hosts on a network.

## Sample Question

What are the CIDR addresses for a network if all its addresses start with 145.98? And if this network has exactly two subnets, what are the CIDR addresses for each of its subnets?

CIDR stands for Classless Inter-Domain Routing. It is a method for specifying a network address that includes both the network prefix and the network size. If the addresses in a network all start with 145.98, it is likely that the network prefix is 145.98.0.0/16. This means that the first 16 bits of the address are fixed and identify the network, and the remaining bits identify the host on that network.

To create two subnets from this network, you would need to split the remaining bits into two equal parts. This would give you two subnets with the prefixes 145.98.0.0/17 and 145.98.128.0/17. This means that the first 17 bits of each address identify the subnet, and the remaining bits identify the host on that subnet.

It is important to note that I am making some assumptions here based on the information you provided. The exact details of the network and its subnets would depend on how it was configured. It is always best to consult with the network administrator or documentation for accurate information about a network's addressing scheme.

>  What is `/17`?

In the context of network addressing, /17 is a CIDR notation that specifies the network prefix and size. In this case, /17 means that the first 17 bits of the address identify the network, and the remaining bits identify the host on that network.

CIDR notation is a way of specifying a network address that includes both the network prefix and the network size. It is often used in conjunction with the Internet Protocol (IP) to specify the routing of IP packets across a network. The notation consists of an IP address, followed by a slash (/) and the number of bits that make up the network prefix.