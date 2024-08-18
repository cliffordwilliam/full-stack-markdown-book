---
layout: post
title:  "How Does the Web Work?"
---

Lesson contents:

* TOC
{:toc}

## Introduction

To know how to make a website you need to know how the internet works.

## Lesson overview

- Describe what the internet is.
- Describe what packets are and how they are used to transfer data.
- Understand the difference between a web page, web server, web browser and serach engine.
- Briefly explain what a client is.
- Briefly explain what a server is.
- Explain what IP addresses are.
- Explain what DNS servers are.

## Outside sources

Sections from here on out are from outside sources.

## Overview of how the internet works

This section reference is [here](https://www.youtube.com/watch?v=eHp1l73ztB8)

4 million hours worth of video data is uploaded to youtube daily, we send 682 millions tweets everyday, instagram has 67 millions posts everyday. 4.4 billion of us uses the internet. We all created 2.5 exabytes, 2.5 million terrabytes everyday.

Servers all store this data. There are buildings in London and other countries that stores these servers.

1969, American defense department decided that they needed a network from inter university to accelerate research. First design is called arbinet, packet switch network. on 1969 we had 2 nodes and soon it grows to millions of connections. Now we have 1.2 million km of sea cables, as deep as mount everest, that connects server buildings and smaller cables connects to individual computers. It is called the internet.

Take note that internet is not the world wide web. World wide web is an invention that sits on top of the internet, the internet is the hardware.

This is how it works in a nutshell. Your request shoots from your browser, to regional network and then across the globe to where the server is physically, sending the whole video in one go in one route will take too much time and risky too, so the video is turned into small packets and each one makes it way back to you via different routes. When they arrive they assemble themselves for you to see. This is how information spreads accross the world.

## Mozilla article on "How does the internet work?"

This section reference is [here](https://developer.mozilla.org/en-US/Learn/Common_questions/How_does_the_Internet_work)

This section discusses on what the internet is and how it works. You learn the difference between the Web and the Internet.

### Summary

Internet is the technical infrastructure, that allows the Web service to work. The internet is just the hardware for a computer network.

[The internet history is obscure](https://en.wikipedia.org/wiki/Internet#History). It began in 1960s as a US-army-funded research project, that became a public infrastructure in 1080s with the support of many universities and private companies. The way internet works to this day remains the same.

### Active Learning

[How the internet Works in 5 minutes](https://www.youtube.com/watch?v=7_LPdttKXPc)

Here is a summary. The internet is not a cloud, this is made by people who needs job security to create a barier so that only few knows what it is. The internet is a wire burried in the ground, connects 2 computer that lets them communicate. Servers are directly connected to the internet, server harddrives store the webpages. Every server or any computer connected to the internet has a unique internet protocol address or IP address. Just like any address it is used for computers to find each other. 72.13.205.100 is hard to remember so we add a label to them like google.com. Your computer at home is not a server because it is not connected directly to the internet, these are called clients. Clients are connected indirectly to the internet via internet service provider.

If you want to send an email. You first request access to gmail.com to access your data there. When you send, it is the gmail server that sends the mail over to the target email server. When the target person request data to their email server that person should see the sent message just now.

When resources are sent over the internet, they are never sent all at once. They are sent in packages. When it reaches the destination, they are assembled together there.

What keeps request packages from going to the wrong places? Solution is IP and routers. This is because anything that is connected directly or indirectly all have IP addresses. Routers have IP addresses to, when connection in the internet intersects, there are routers. Routers direct the packages to the right place, this is how they do it. Imagine 1 package is like a candy wrappen in layers, the first layer is your computer IP, when it hits a router or anything else in between that has an IP address, it will add that new IP as a new wrapping to the candy. When it reaches the server, that is where the final added wrapping happens. When the server sends a response, it will use the same wrapping that your request had before. As it makes its way back, it will use the wrapping to go to the correct place, each time it reaches the correct place it removes one wrapping. Until it reaches your computer. And that is it.

[How does the Internet work](https://www.youtube.com/watch?v=x3c1ih2NJEg)

How does the internet works? Data you request may come from data centers, a building filled with servers. Like Google data center. An easy way to transfer data from a server to your commputer is to use sattellites, signal can be sent to satellites via antenae, then satellite send signal to your machine via another antenna near to you. This is not a good idea, this is because. 22000 miles above the Earth equator, so data have to cover 44000 miles. This long distance causes long delay, which is not suitable for everyday uses. So instead of satellites data travel via optical fiber cables. These cables are underground and connects server together. Clients are connected to either router or cellular data towers. But either one of those are connected to the optical fibre cables. Any resources like pages or videos are all stored in server solid-state device SSD as the server internal memory. Now how to transfer data in server SSD to your computer using the complex netweork of optic fiber cable? We need to know that any device that is connected to the internet has an IP address. Like a home address, it is unique to each home, that is how letters reach your home correctly. IP is how data reaches correct places. ISP decides on your machine IP address, you can see it in your machine settings. Server also has IP address, so to request a page or video from a server, you just need to know the server IP address, since the addresses are hard to remember we use domain names, these names corresponds to the IP addresses. 1 server can store multiple websites, so 1 IP address for that server is not enough to distinguish between the websites, we need to access them with host headers to uniquely identify the sites. But huge websites like youtube will dedicate 1 data center infrastructure, one building and all of its server inside of it to host youtube website only. To access the internet we use domain name and not the IP addresses, where did the domain gets translated into the correct IP? There are special servers in the internet called DNS server. It is like a phone book, it maps domain to IP. ISP or other organizations manages the DNS server. This is how the whole thing works. You request a domain name to the browser, the browser now sends a request to the DNS to get the right IP. Then the browser forwards the request to the data center that has the mapped IP. Data is sent back from server via optical fiber cables, light pulses, 1000 miles to reach destination, mountains and under the sea, there are companies that maintain these cable networks. The cables are laid down with ships, they use a plow that both creates the trench and places the cable in it. This light is carried into phone towers or router and then to your machines. Router and phone cell tower converts the light into electrical signals. You can use ethernet cable to get the data or wirelessly. Cell tower converts the light pulse into electromagnetic waves that your phone then receives. There are organizations that takes care of IP address assignments, domain names registrations, these are all managed by ICAAN in USA. Internet Corporation for Assigned Names and Number. Internet hardware is faster in comparison to cellular and landline communication technologies. When data is transfered, data in forms of 0 and 1 are chopped into packages. Assuming we chop the whole 1 and 0 into 3 15 rows of 6 bits. Each packages has the sequence number and IP addresses. Each packages takes different path and they all take the best route in real time. When it reaches your phone the packages are re-assebled using their sequence number. If some packages failed to reach your phone then an awknowledgement is sent from phone to server to resend that lost package. In order for every server to send data the same way in the whole world, to ensure that it reaches the right destination using the internet hardware, we have a protocol. It is the rules for how data to packets are converted, and how and what are the metadata needed for the source and destination needed to be included in the packages. TCP/IP, http/https, RTP for transport data, web access and live video respectively. This also includes the rules for how the routers manage the packages and where to route them to. Different app different protocols based on what resources they are trying to send.

## Deeper dive

### A simple network

TODO
