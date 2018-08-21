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
