# BGP - Border Gateway Protocol

- BGP is a routing protocol
- this is dominant for Inter-AS , there are lots of alternatives for intra AS.
- Used to control how data flows from point A to point B
- BGP is made up from a lot of self managing networks know as Autonomous Systems (AS)
- AS could be a large network, collection of routes etc. and is viewed as a black box from BGP perspective
- Each AS is allocated a number by IANA, named ASN
- ASNs are 16 bit in length and range from 0 to 65535, the range from 64512 to 65534 is private
- We can get 32 bit ASN numbers as well (this is out of scope for this exam)
- ASNs are used by the BGP to identify different entities on the network
- BGP is designed to be reliable and distributed, and it operates of TCP/179
- It is not automatic, the communication between to AS should be done manually
- Autonomous Systems do exchange network topology information between them
- BGP is a path-vector protocol: it exchanges the best path to a destination between peers, the path is called **ASPATH** (Autonomous System Path)
- Shorter Path as preferred path - ( not faster- but since shorter path : are mostly faster)
- BGP does not take into account link speed or condition, it focuses on path only
- iBGP - internal BGP, routing within an AS
- eBGP - external BGP, routing between AS's
- BGP example:
    ![BGP 101](images/BorderGatewayProtocol101.png)
- BGP always choses the shortest path. There are ways to influence the path by artificially expending the path (prepending itself to the path)
- https://www.youtube.com/watch?v=1pyp0gvhRuM summary below
  1. BGP allows network routers to exchange information of every router it carries
  2. Routers collect all the routing advertisements they get , and create routing table 
