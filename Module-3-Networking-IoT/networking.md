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