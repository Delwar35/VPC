
# What is CIDR

Meaning: *Classless inter-domain routing*
- A way for assigning IP addresses and IP routing.
- A collection of IP standards to be able to give unique identities to devices.

*Replaces the following class system*
### Classes include
- Class A address
	- from 1.x.x.x -> 126.x.x.x
-  Class B Address
	-  from 128.0.x.x -> 191.255.x.x
	-  Meaning the second bit can be allocated from the range of 0 to 255
- Class C
	- from 192.0.0.x -> 223.225.255.X
	- Appending to the Class B rules to the third point out of fourth, *notice* the **first** point sequentially getting bigger and bigger
- Class D
	- from 224.0.0.0 -> 239.255.255.255
	- used for multicasting, again appending to the last rule and again increasing the addresses for the first point
- Class E
	- Reserved class
	- 240.0.0.0 -> 255.255.255.254
	- For Research and development purposes


This block contains IP addresses. This block consists of 3 basic rules.

**Rule 1:** In the CIDR block, the IP addresses which are allocated to the hosts should be continuous. uu

**Rule 2:** The size of the block should be of power 2 and should be equal to the total number of IP addresses.

**Rule 3:** The size of the block must be divisible by the first IP address of the block.


# IPv4
The current standard of the internet, *internet protocol version 4* is currently forty years old, introduced in 1981.
Key points:
- 32 bit address system or four bytes
	- 4,294,967,296 ($2^{32}$)
	- Limiting
- Example
	- 255.255.255.1
		- Uses a Dot decimal notation for human readability, not for actual use
	- 11111111.11111111.11111111.00000001
		- Actual binary nuberi
# IPv6

The introduced and eventual replacement of IPv4, specifically made in *1995* to tackle the numbers issue imposed by IPv4.
![](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5e/IPv6_address_terminology-en.svg/1920px-IPv6_address_terminology-en.svg.png)
Key points
- total number of address
	- 128 bit system
	- 34,359,738,368

# Route Table (RT)
- Table used to determine a destination following a subnet mask and what kind of interface
- Used for all physical mediums

# Internet Gateway
![](https://cloudiofy.com/wp-content/uploads/2021/05/internet-gateway.png)

# Diagram

![image](https://user-images.githubusercontent.com/94615905/145081156-e368bd35-6a37-4008-9851-fa3ca62ae88e.png)

