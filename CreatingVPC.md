# Week 4 VPC and CICD


![image](https://user-images.githubusercontent.com/14828358/144827863-ddaba37f-9d3e-4eb1-b0e4-bdfd8f9afb0f.png)





![image](https://user-images.githubusercontent.com/14828358/144831914-f1084794-2c5e-48b0-9234-91d4669ea713.png)




## Network Access Control Layer (NACL)

  * An optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets 

## Route Tables

  * A route table contains a set of rules, called routes, that are used to determine where network traffic from your subnet or gateway is directed.


## Tutorial

https://www.youtube.com/watch?v=GrfOsWUVCfg&ab_channel=LinuxAcademy

https://www.youtube.com/watch?v=yCl8wkdSHA8&ab_channel=AOSNotes



## Step 1: Create VPC

![image](https://user-images.githubusercontent.com/14828358/144840323-1f9e2b09-df56-4b13-8407-e36f99f61d00.png)


![image](https://user-images.githubusercontent.com/14828358/144840500-f9d4342f-f335-423d-a030-e2658ec21c0f.png)




## Step 2: Internet Gateway

![image](https://user-images.githubusercontent.com/14828358/144841478-6b7d42d3-bef3-42fa-afa9-68d3d51c2d6a.png)

![image](https://user-images.githubusercontent.com/14828358/144841550-ccbe215b-e849-45ff-9e5b-dd874074182c.png)


### Attach IG to VPC

![image](https://user-images.githubusercontent.com/14828358/144841674-5650a013-ed3c-479a-a46a-b60795647613.png)

![image](https://user-images.githubusercontent.com/14828358/144841701-bbe605ff-db6c-463f-9d2c-615ee3c599b2.png)

![image](https://user-images.githubusercontent.com/14828358/144841790-926324ba-8efe-4f51-95a7-62ee8ada10eb.png)

## Step 3: Public Subnet for our App

![image](https://user-images.githubusercontent.com/14828358/144841843-33517f17-11c3-4289-895f-d8b5ae6be6aa.png)

![image](https://user-images.githubusercontent.com/14828358/144841886-741e1587-251f-4f7a-a343-132022b8a72d.png)

![image](https://user-images.githubusercontent.com/14828358/144842150-d54fe3b0-844e-45ba-8c21-6a54e5ad9e40.png)

Click Create


## Step 4: Create Routing Table with Routes and Rules

![image](https://user-images.githubusercontent.com/14828358/144842227-5aa0a09c-dbf7-4f7b-9094-02d5692084fb.png)

![image](https://user-images.githubusercontent.com/14828358/144842356-199499aa-4d85-4b9a-a8ad-f20524691950.png)

### Edit Routes to allow IG and VPC

![image](https://user-images.githubusercontent.com/14828358/144842649-3e252b02-7b5c-4f06-a70d-4b76a5bf024f.png)


![image](https://user-images.githubusercontent.com/14828358/144842744-e351fe97-05b3-404d-a575-89a8b3ba04c7.png)


![image](https://user-images.githubusercontent.com/14828358/144842902-0b4b8fef-25b1-46d0-9b9a-b79ad0bbcf1d.png)



### Associate our RT to our public subnet

![image](https://user-images.githubusercontent.com/14828358/144842991-89c03648-3051-416a-bf2c-914d19fc9aa2.png)

![image](https://user-images.githubusercontent.com/14828358/144843039-020aa940-23a0-443b-ba3e-e4ec00e06eea.png)


ip range: 10.0.10.0/16

- Create security group now or when app is launched
- port 22 from my_ip
- port 3000
- port 80 HTTP with cert for security
- HTTP - SSL cert




- Security groups work on instance level and by default outbound rules allow all
- Network Access Control Layer adds and extra layer of security


~Tell me about your self


What is DevOps and what are they key benefits of DevOps


what is the diff between monolith and 2 tier architecture


~what is a VPC networking


explain how to deploy 2tier architecture with private and public subnets


 ![image](https://user-images.githubusercontent.com/14828358/145018656-3a8b777e-133c-47e5-97be-a350e63b892f.png)


![image](https://user-images.githubusercontent.com/14828358/145082448-d921be94-d165-4a5d-a3b1-62534bcfa00a.png)


## Associate private subnet (with database) to the private routing table

![image](https://user-images.githubusercontent.com/14828358/145082694-1d1f13ef-481a-4c4b-af2b-cbd17d9ac9b9.png)


## In Routes, input the route to the instance


![image](https://user-images.githubusercontent.com/14828358/145082742-72f9b48e-b4ec-4dad-94f3-4f31c26ccdc3.png)


![image](https://user-images.githubusercontent.com/14828358/145083396-95721b5f-722f-45f7-9b13-f657fc64d139.png)





