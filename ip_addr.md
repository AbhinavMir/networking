 ## CIDR 

CIDR (Classless Inter-Domain Routing) is a way of allocating IP addresses that divides an IP address into two components: the network address and the host address. This allows for more efficient use of IP addresses as it allows for a single network address to be allocated to multiple hosts, allowing for more efficient use of IP address space.

CIDR is based on a hierarchical network addressing system where addresses are divided into blocks of fixed size. Each block is assigned a unique network address, and each address within the block is identified using a unique host address. The size of the block is indicated by a mask, which specifies the number of bits that are used for the network address. The mask is written in the form of a dotted decimal notation, with the number of bits used for the network address indicated in decimal notation.

For example, a CIDR address of 192.168.0.0/24 would indicate that the first 24 bits of the address are used for the network address and the remaining 8 (32-24) bits are used for the host address.

CIDR is used for routing in large networks, such as the Internet, and is becoming increasingly popular as a way of allocating IP addresses. It is also used for assigning IP addresses to hosts on a network.