A network protocol is a set of established rules that dictate how to format, transmit and receive data so that computer network devices -- from servers and routers to endpoints -- can communicate, regardless of the differences in their underlying infrastructures, designs or standards.

To successfully send and receive information, devices on both sides of a communication exchange must accept and follow protocol conventions. In networking, support for protocols can be built into software, hardware or both.

Without computing protocols, computers and other devices would not know how to engage with each other. As a result, except for specialty networks built around a specific architecture, few networks would be able to function, and the internet as we know it wouldn't exist. Virtually all network end users rely on network protocols for connectivity.
How network protocols work

Network protocols break larger processes into discrete, narrowly defined functions and tasks across every level of the network. In the standard model, known as the Open Systems Interconnection (OSI) model, one or more network protocols govern activities at each layer in the telecommunication exchange. Lower layers deal with data transport, while the upper layers in the OSI model deal with software and applications.

A set of cooperating network protocols is called a protocol suite. The Transmission Control Protocol/Internet Protocol (TCP/IP) suite, which is typically used in client-server models, includes numerous protocols across layers -- such as the data, network, transport and application layers -- working together to enable internet connectivity. These include the following:

    TCP, which uses a set of rules to exchange messages with other internet points at the information packet level;
    User Datagram Protocol, or UDP, which acts as an alternative communication protocol to TCP and is used to establish low-latency and loss-tolerating connections between applications and the internet;
    IP, which uses a set of rules to send and receive messages at the level of IP addresses; and
    additional network protocols, including Hypertext Transfer Protocol (HTTP) and File Transfer Protocol (FTP), each of which has defined sets of rules to exchange and display information.

Every packet transmitted and received over a network contains binary data. Most computing protocols will add a header at the beginning of each packet in order to store information about the sender and the message's intended destination. Some protocols may also include a footer at the end with additional information. Network protocols process these headers and footers as part of the data moving among devices in order to identify messages of their own kind.
Every machine on a network has a unique identifier. Just as you would address a letter to send in the mail, computers use the unique identifier to send data to specific computers on a network. Most networks today, including all computers on the internet, use the TCP/IP protocol as the standard for how to communicate on the network. In the TCP/IP protocol, the unique identifier for a computer is called its IP address.

There are two standards for IP addresses: IP Version 4 (IPv4) and IP Version 6 (IPv6). All computers with IP addresses have an IPv4 address, and most use the new IPv6 address system as well. Here are the differences between the two address types:


    IPv4 uses 32 binary bits to create a single unique address on the network. An IPv4 address is expressed by four numbers separated by dots. Each number is the decimal (base-10) representation for an eight-digit binary (base-2) number, also called an octet. For example: 216.27.61.137
    IPv6 uses 128 binary bits to create a single unique address on the network. An IPv6 address is expressed by eight groups of hexadecimal (base-16) numbers separated by colons, as in 2001:cdba:0000:0000:0000:0000:3257:9652. Groups of numbers that contain all zeros are often omitted to save space, leaving a colon separator to mark the gap (as in 2001:cdba::3257:9652).

TCP/IP
What is TCP/IP? TCP/IP stands for Transmission Control Protocol/Internet Protocol and is a suite of communication...
