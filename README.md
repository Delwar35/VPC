# VPC

**What is CIDR (Classless Inter-Domain Routing) Block**

CIDR block a method for allocating IP addresses and IP routing in the VPC. The IP can be IPv4 or IPv6 format. 

When you create a VPC, you assign it an IPv4/IPv6 CIDR block (a range of private and public IPv4/ipv6 addresses), or both (dual-stack). Private IPv4/IPv6 addresses are not reachable over the internet while public addresses are. To connect to your instance over the internet, or to enable communication between your instances and other AWS services that have public endpoints, you can assign a public IPv4/IPv6 address to your instance. 

**What is IPv 4 and 6**

An Internet Protocol address (IP address) is a label such as 192.0.2.1 that is connected to a computer network that uses the Internet Protocol for communication. An IP address serves two main functions: network interface identification and location addressing.

IPv4 is a protocol for use on packet-switched Link Layer networks (e.g. Ethernet).IPv4 provides an addressing capability of approximately 4.3 billion addresses.

IPv6 is more advanced and has better features compared to IPv4.  It has the capability to provide more addresses the IPv6.  It is replacing IPv4 to accommodate the growing number of networks worldwide and help solve the IP address exhaustion problem.

One of the differences between IPv4 and IPv6 is the appearance of the IP addresses.  IPv4 uses four 1 byte (8-bits) decimal numbers (range 0-255), separated by a dot (i.e. 192.168.1.1), while IPv6 uses hexadecimal numbers that are separated by colons (i.e. fe80::d4a8:6435:d2d8:d9f3b11).  

**What is Route Table (RT)**

A route table contains a set of rules, called routes, that are used to determine where network traffic from your subnet or gateway is directed.

**What is Internet Gateway (IG)**

An internet gateway serves two purposes: to provide a target in your VPC route tables for internet-routable traffic, and to perform network address translation (NAT) for instances that have been assigned public IPv4 addresses.

An internet gateway supports IPv4 and IPv6 traffic. It does not cause availability risks or bandwidth constraints on your network traffic. There's no additional charge for having an internet gateway in your account.

**VPC and Subnets Range**
A virtual private cloud (VPC) is a virtual network dedicated to your AWS account. It is logically isolated from other virtual networks in the AWS Cloud. You can launch your AWS resources, such as Amazon EC2 instances, into your VPC.

When you create a VPC, you must specify a range of IPv4 addresses for the VPC in the form of a Classless Inter-Domain Routing (CIDR) block; for example, 10.0.0.0/16. This is the primary CIDR block for your VPC.

A subnet is a range of IP addresses in your VPC. You can launch AWS resources, such as EC2 instances, into a specific subnet. When you create a subnet, you specify the IPv4 CIDR block for the subnet, which is a subset of the VPC CIDR block. Each subnet must reside entirely within one Availability Zone and cannot span zones. By launching instances in separate Availability Zones, you can protect your applications from the failure of a single zone.

When you create a VPC, you must specify an IPv4 CIDR block for the VPC. The allowed block size is between a /16 netmask (65,536 IP addresses) and /28 netmask (16 IP addresses). After you've created your VPC, you can associate secondary CIDR blocks with the VPC.

A VPC can have  upto 200 subnets.

**What is NACLs**

A network access control list (NACL) is an optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets. You might set up NACLs with rules similar to your security groups in order to add an additional layer of security to your VPC

**Difference between statless and stateful (NACLs vs Security Groups)**
![image](https://user-images.githubusercontent.com/94615905/144837456-d20d14fc-98f7-493b-ac28-e2413d3ffa83.png)


