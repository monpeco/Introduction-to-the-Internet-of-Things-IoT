#### Module 3: Networking IoT   3.0 Introduction   How 'things' connect

### How 'things' connect

In this module we will explore how all the ‘things’ we looked at in Module 2 can send data and receive instructions through a network.

By the end of Module 3, you will be able to:

* describe how information/data travels through an IoT network;
* list the components of a basic network, and their properties;
* describe the types of connections in IoT networks;
* understand the role of Internet Protocols, and describe how their various properties make them suited to different types of IoT projects.

---

#### Module 3: Networking IoT   3.0 Introduction   Introduction to Module 3

IAIN MURRAY: Welcome back.
I'm Iain Murray.
And now we're going to have a look at the network.
This is how we communicate our information.
How we collect data from sensors.
And there's many different forms our network can take.
One of the most common-- and we're probably all familiar with it--
is UTP cable--
Unshielded Twisted Pair.
This is basically just a copper wire with two connectors on either end
that we use to join your computer to probably your modem or your switch
at home.
These cables carry the data, but that data has to get to its destination
somehow.
And that means we've got to look at how things are addressed,
how things are routed through your network
to reach their final destination.
So we have the cable to your modem.
The modem then makes a decision where we're going to send that on to.
Normally to your internet service provider.
At the internet service provider, the data that you're sending
has some information in front of it called the header.
The header has address information much like a letter that you would
send through the traditional mail.
And that states where it's going to next.
Your information's then passed from one device, a router,
to another device, another router, and so on through many, many routers
until it reaches the destination network where, again, it's extracted.
It's sent through to the switch back through probably
one of our ethernet cables to the end node itself.
That's the network.
As we're usually fairly familiar with, we
can think of it along the lines of the telephone network.
It's a way of communicating information from one point to another point.
Now, how does this fit in with the Internet of Things?
 Well, it's similar, but there are subtle differences.
We have different data requirements for the Internet of Things.
Usually lots of small bits of data, not large amounts of data like we
use when were streaming videos.
We've got different protocols because we want to deal with different distances.
With generally in the Internet of Things is not talking about transferring data
hundreds of kilometers.
We're talking about getting it from a close point on a person,
for example, to the device for transmission on to the data stores.
So we have a different distance.
We have different data rate, and therefore, we
have different requirements for the protocols.
So let's have a look at some of these.

---

#### Module 3: Networking IoT   3.1 Gateways and routing   Message in a network

In your home office you might have a computer and a printer. When you print something, the computer sends a message to the printer, and this message travels by either copper cable or wireless communication. This is your home network.

When you want to look at a web page or send an email, you need to connect your computer, smartphone, or other device, to the internet. The internet is a network of networks, or internetwork.

This simple network has several key components:

* Devices - includes the computers, printers, routers and servers.
* Media - includes the cabling or wireless connections.
* Services - includes the software that support operations, such as email hosting.

You should know that the Internet of Things adds many more devices (those ‘things’ we looked at in Module 1), as well as more services to networks (and we will take a closer look at services in Modules 4 and 5).

---

#### Module 3: Networking IoT   3.1 Gateways and routing   Gateways and routing


Communication in the network is carried through a medium – currently this means via either a cable (for example, metallic wires in copper cables, or glass or plastic fibres in fibre optic cables) or the air (wireless transmission).

The different media have different characteristics, which makes each better suited to different circumstances, taking into consideration factors such as:

* the distance a signal needs to travel
* the environment it is travelling in
* the amount and speed of the data
* the cost of the media and its installation.

The IoT adds even more circumstances and considerations for connectivity...making the ‘world wide web’ look more like a web than ever before.

---

####  Module 3: Networking IoT   3.1 Gateways and routing   Routing all the way

#### Module 3: Networking IoT   3.1 Gateways and routing   Trace the route

INSTRUCTIONS FOR PC USERS

type:

    cmd

Try a 'ping' to see if a computer on the network is there.
For example, type:

    ping edx.com

Now type:

    tracert edx.com

Sending a command to trace the route of a website request (Step 3) will show you the route in detail - you will see all the different routers and networks that the request travels through (up to a maximum of 30), and finally the destination site with its IP address.

But how does the data know where to go?

How do servers and intermediary devices all over the world communicate with each other?

That’s what we’ll be covering in the next section.

#### Module 3: Networking IoT   3.2 Protocols and standards   Internet protocol (IP) addresses

End devices are those that provide a way for users to interact with the network. Examples include computers, smartphones and sensors.

End devices are either the source or destination of data going over the network.

Every device has a unique Internet Protocol (IP) address, so it is distinguishable from all other devices. When sending a message, the IP address of the destination is used to specify where the message is being sent, similar to the address printed on the envelope of a letter.

Intermediary devices interconnect end devices; host to the network, and networks to other networks. Intermediary devices also manage the data through the network - they act like the 'post master' in mail delivery scenarios.

These devices take the destination host address and combine that with information about network connectedness to decide on the path that messages take through the network. Intermediary devices therefore need to maintain network information (frequently update the network map) and may also notify other devices of errors. This allows them to choose alternative pathways, or retransmit data, or even deny the flow of data based on security settings.

**IP addresses**
The addresses used to send data in networks are called Internet Protocol (IP) addresses. Ipv4 (version 4) is what is typically in use currently.

Ipv4 addresses consist of four sets of numbers separated by periods, and each number is between 0 - 255.

For example:
```
1.2.3.4
or
233.67.151.3
```

Ipv6 is being developed using six sets of numbers, colons and hexadecimal numbering to allow many more destination addresses. These will help to facilitate IoT, as well as adding features for improved routing, security and data flow.

Ipv4 has around 4 billion IP addresses (which ran out a few years back.) Ipv6 has around 340 undecillion IP addresses - that's 340,000,000,000,000,000,000,000,000,000,000,000,000, give or take a few billion.


---

#### Module 3: Networking IoT   3.2 Protocols and standards   Activity and Discussion: IP address lookup

You can look up IP addresses.
* Step 1: Open Command Prompt (PC) or Terminal (Mac) as described previously in the Trace the Route activity.
* Step 2: Type nslookup and press Enter/Return.
* Step 3: Type in the address of a web site you want to look up. Try looking up a website you use often.

---

#### Module 3: Networking IoT   3.2 Protocols and standards   Domain Name Servers (DNS)

When you 'look up' a website the way you just did, you are looking up its IP address in the Domain Name Service or DNS, which is the Internet equivalent of a telephone book. It matches a name (like facebook.com) to a number (like 157.240.8.35) - because humans prefer to deal with names and computers prefer numbers.

The DNS is a large database of computer names and their internet addresses, but it is spread out so that no server has all the information.

If a computer requests a domain name and that server doesn’t have it, it forwards the request to another DNS server. The Domain Name Service has a hierarchical structure, so requests get sent from the bottom up.

As you can see in the diagram below, at the top of the hierarchy are the most familiar domain roots: .com, .org, .gov, etc.

![host](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/a92bb19dbd7f11aa14054de4d385eb93/asset-v1:CurtinX+IOT1x+2T2018+type@asset+block/3_8.png)
When setting up an internet connection on a computer, it is usual to allocate a primary DNS server and one or more secondary servers. This information is generally provided by your ISP.

---

#### Module 3: Networking IoT   3.2 Protocols and standards   Playing at protocols

Internet Protocol (IP) addresses are one of many protocols that operate within the Internet. Combining IoT ‘things’ and applications increases the number of protocols required.

Having agreed protocols that operate at a set standard allows for computers on different sides of the world to communicate with each other.

A protocol is an agreed (or accepted) set of rules for a procedure. For example, there are many protocols in place across the world that help to determine how people interact with each other.

In the same way, the internet has many protocols to make sure computers can interact with each other in an agreed, standard way.

The internet operates on a layered structure. When data is sent from one place to another, the data passes through different layers. Each layer has a protocol determining what and how information passes through.

It is similar to when you go to the shops to buy groceries. We can break that trip down into layers of operation - and at each layer there is a procedure you need to follow for a successful shopping trip!

You leave the house – you need to remember to take your keys, wallet and shopping bag.
You get transport to (and from) the shop – you either need to find the right public transport, or follow traffic laws while driving/riding and find a parking spot.
In the shop, you locate and select your groceries – you follow a system of aisles and a way to choose your items.
You check out of the shop – you need to use a payment method and have a way to carry your groceries home.
There is a set of ‘rules’ for each stage which must be followed in order for you to successfully complete your shopping trip. Failure to take a payment method, or failure to find a parking spot or the item you want in the shop, for example, may result in an unsuccessful trip.

The Internet Engineering Task Force (IETF) is the premier Internet standards body. They define the TCP/IP model (Transmission Control Protocol/Internet Protocol) which is the most common networking protocol suite.

TCP/IP: a set of rules that governs the connection of computer systems to the Internet

Standards and protocols exist so that messages can get through and miscommunication is minimised.

It helps to remember that communication between machines and communication between people fit the same model.

---

#### Module 3: Networking IoT   3.3 IoT Connecting   IoT connecting

Connecting everyday things to the internet brings with it a host of different situations that are more varied and problematic than a computer at a desk, or even a smart phone on the move. To address these complexities, IoT solutions need to use various protocols, depending on the situation. IoT makes use of existing technology for physical connections, and their corresponding protocols, such as Ethernet or 4G mobile.

There are also newer protocols and connectivity types being developed specifically for IoT.

Curtin University is trialling the use of an IoT protocol, LoRa WAN network. LoRa stands for Long Range Radio. It is a wireless technology targeting M2M (Machine to Machine) and IoT networks. This technology will enable public or multi-tenanted networks to connect multiple applications running in the same network. LoRa technology could be used in a smart city set up, along with LoRa sensors and automated products and applications.

LoRa is a type of Narrowband RF technology. Narrowband RF technologies operate over longer distances and at lower power levels, but their trade-off is that they only offer smaller bandwidth connectivity, limiting their use to restricted data and bandwidth applications. Examples include alarm systems, critical sensor arrays, and many M2M applications.

The main advantage of Narrowband RF technologies is that they are low cost to set up and operate, and the devices that they support use minimal power. This means they can be operated in an autonomous manner for long periods. Other examples of Narrowband RF are SIGFOX (Ultra Narrow Band) and NB-IoT (Narrow-Band IoT.)

At Curtin University, the LoRa runs alongside the WiFi. WiFi is utilised by people using their mobile devices and potentially needing a high bandwidth, while the LoRa can be used for IoT. Below is a map showing the expected coverage of Curtin University’s LoRa WAN footprint (uplink), from two antennae on two campus buildings.

 ---
 
 #### Module 3: Networking IoT   3.3 IoT Connecting   Video: Case study: Networking devices
 
 