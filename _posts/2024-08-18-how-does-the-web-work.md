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

### Deeper dive

#### A simple network

For modern computers to communicate to each other they need to be linked physically with [ethernet cable](https://en.wikipedia.org/wiki/Ethernet_crossover_cable) or wirelessly with [Wi-Fi](https://en.wikipedia.org/wiki/WiFi) or [Bluetooth](https://en.wikipedia.org/wiki/Bluetooth):

- Ethernet: connect two devices of the same type.
- Wi-Fi: family of wireless network protocols based on the IEEE 802.11 family of standards, which are commonly used for local area networking.
- Bluetooth: short-range wireless technology standard that is used for exchanging data between fixed and mobile devices over short distances and building personal area networks (PANs)

You can use any of the above to connect more than 2 computers.

![how_does_the_web_work_one_to_one_connection]({{ "/assets/images/how-does-the-web-work-one-to-one-connection.png" | relative_url }})

But it gets complicated when you try to connect more than 10 computers that way.

![how_does_the_web_work_too_many_connections]({{ "/assets/images/how-does-the-web-work-too-many-connections.png" | relative_url }})

#### A network of networks

To solve the above, we use a tiny computer called a router. All computers are now connected to this router, and the router only job is to make sure that data sent from 1 computer reaches the correct target. This increases scalability, if the router gets over populated we can introduce another router and then just connect 1 router to another router.

![how_does_the_web_work_router_to_more_router]({{ "/assets/images/how-does-the-web-work-router-to-more-router.png" | relative_url }})

This scales infinitely.

![how_does_the_web_work_router_to_router]({{ "/assets/images/how-does-the-web-work-router-to-router.png" | relative_url }})

But the above works for 1 building, like your home. So how to connect this to your friends home? We use existing cable infrastructures like the telephone infrastructure, since it already connects your house with anyone in the world. So connect your router network to it we use modem. Modem converts your router network data format to telephone data format.

After connecting to the telephone infrastructure, we connect to Internet Service Provider (ISP) network, companies that have special routers that connects to other ISP routers.

The above explains what the Internet is, an infrastructure of networks, from your home network, to phone network then to ISP.

![how_does_the_web_work_internet_infrastructure]({{ "/assets/images/how-does-the-web-work-internet-infrastructure.png" | relative_url }})

#### Finding computers

Any computer linked to a network, including the internet network, has a unique IP address, Internet Protocol address. Its bits separated by dots, like hex color. `192.0.2.172`.

To remember the IP easier, we have alias for IP addresses called domain name. So `google.com` is the domain name **used on top of** `142.250.190.78` IP address. (IP address may change as time goes by so that may not be accurate at the time of reading this)

### Internet and the web

Internet is the physical infrastructure hardware, where the Web is the service software that uses it. The Web comprises of the Web browser that lets you make request and receive data from other computer connected to the hardware Internet. The Web also comprises of the Web servers computer software that lets it understand your request and be able to respond accordingly. There are many parts to it but Internet and the Web are not the same thing.

There are other services on top of the Internet other than just the Web, such as email and [IRC](https://developer.mozilla.org/en-US/docs/Glossary/IRC).

### Intranets and Extranets

Intranets are private network, like a company may host resources for their employees only. Hosted things may be web pages, drives data, discussion boards like forums.

While extranets only difference is its limitation scope, it can allow access for multiple organizations, clients, stakeholders and so on.

Both uses the same infrastructure that the internet uses, same protocols too. So even if you are not physically nearby, as long as you are authorized you can access it.

## Differences between a web page, a web server, and a serach engine

This section reference is [here](https://developer.mozilla.org/en-US/Learn/Common_questions/Pages_sites_servers_and_search_engines)

Here we discuss what web pages are, websites, web servers and search engines. Here are the right ways to use the terms / jargons.

### Summary

Here are the [glossary](https://developer.mozilla.org/en-US/docs/Glossary) for the rest of the jargons. Here are the common ones that you need to know, do not mix them up. Most people including the media tends to use them incorrectly.

- **Web page**  
  This is also knows as pages, it refers to HTML, CSS and JS. Those 3 are instruction for the browser to draw the page on the browser window.

- **Website**  
  This is like a book, a book is made out of many pages. You can navigate around the book pages by links inside the page. Website is also known as site. You know a page belong to a certain book if they share the same domain. If you request for the domain name alone in the URL, it will usually give you the homepage.

- **Web server**  
  This is a type of computer that sole purpose is to store data and serve data. Also known as server. It stores both the logic and the resources. A server may host multiple sites. For example, later when you host your website on Vercel, you are actually sharing the same free rent server space with other people. Each app in there are isolated from one another and given a unique header that specify the unique domain to uniquely identify each app. So other make requests to the same infrastructure but different apps.

- **Search engine**  
  Browser is a software, clients uses this. This software is like your Microsoft Word, it can open document. But the document / instruction that it opens are webpages which are made with HTML, CSS and JS (it can also open other things like images and pdf but that is not considered a webpage). But it has an added feature where it can make request over the internet to other server for their stored pages too. There are special websites that is part of the Web service called Search engine. These have a page with a search input where you can request for other pages and it will list it for you in another page. Like an assistant that finds book for you in the receptionist table instead having you to go find the books yourself. Google, Bing, Yahoo, or DuckDuckGo. So think of it like a webapp like wikipedia, in there you can search different wiki pages since the app stores all of its wiki pages. But search engines stores indexes of all websites and is able to do the same search on that instead. Read on the details yourself. So when you open a browser it is possible for it to render nothing, but modern ones will immediately request for the default search engine for convenience. Use [this](https://www.whatsmybrowser.org/) to find out what web browser you are using.

Do take note that URL is called Uniform Resource Locator. This is the unique address for resources like pages. So when you request a page like this `https:/example.com/page`, `https` is the protocol, `example.com` is the domain, `/page` is the resource path.

HTTPS is mostly uses because it has secure rules for communication between client and servers. HTTPS is **Hypertext Transfer Protocol Secure**, secure version of HTTP (data exchange protocol the Web uses). HTTPS encrypts your data during transfer, uses **SSL/TLS**, so even if someone taps into the phone line they cannot read the data without the right encryption key. There are other details about this you can read yourself later. But know that **SSL/TLS certificates** is used for ensuring that you are who you said you are, to prevent someone else from pretending to be you and let others know if an impostor has been responding in your place as a server.

## How different parts of the web interacts with each other

The reference for this section is [here](https://developer.mozilla.org/en-US/Learn/Getting_started_with_the_web/How_the_Web_works#Clients_and_servers)

This is a simplified view of what happens when you view a page in a browser. This knowledge is good for fundamental understanding.

### Clients and servers

Computers in the Internet network falls under 2 category. Clients and Servers.

- **Clients**  
  This refers to the computer or softwares that makes requests over the Web to servers.

- **Servers**  
  This refers to computers that stores resources and the one that sends a copy of these resources to clients that made the request.

### The other parts of the toolbox

There are other parts involved in data transfer. Imagine the Web is a road, on one end is the client and on the other is server. Your house and the store. Here are what between the two:

- **Internet connection**  
  The fibre optic cable, this is the road, the medium that lets you move.

- **TCP/IP**  
  Transmission Control Protocol and Internet Protocol, these are communication rules or how you should cross the road. It defines **how** data and you should travel. The data format rules, collection of these rules are called a protocol. Handles low-level data transmission and network communication, like establish connection before data transfer or acknowledgement to re-send broken packages or a rule to always use IP addresses.

- **DNS**  
  This is the address book, you know what the name is but where exactly it is? Its address? You use this book to map the name to the address. Browser will use the nearby DNS server to map the domain name you have typed to its correct IP address before sending request. It needs to know the IP to send request.

- **HTTP**  
  Typertext Transfer Protocol is the rule to how data is sent over the Web. Like what language you use to order the food. This degine web content delivery rules, like how it should not carry over previous request metadata or it is the client that sends requests not server or there can only be 5 methods like GET POST PUT DELETE PATCH and status codes like 200 and so on.

- **Component files**  
  A page can be rendered by browser with sets of instructions sent from server. It has code files like HTML, CSS and JavaScript. There are also static assets like images, music and videos.

### So what happens, exactly?

When you make a request in your browser:

1. Browser first checks DNS to map domain to IP address, you need IP address first before making a request.
2. Browser sends request with a protocol (what protocol is used is determined by what you type or what the server and individual host configuration is). The request translate to asking if the server can send a copy of the resource to your client using TCP/IP or other protocol (how it decides it the same, based on what you type and machine configuration on either end).
3. If the server approve your request, it sends 200 OK code first as header before sending the resource in packets as the response body.
4. Then the browser assembles the small packets into a complete page and render it to you.

### Order in which component files are parsed

It is important to know the order at which the browser parse HTML, CSS and JavaScript:

1. **DOM Construction**:
   - The browser begins parsing the HTML document from top to bottom to build the DOM (Document Object Model) tree.

2. **CSS Handling**:
   - As the browser encounters CSS (`<link>` or `<style>` tags), it starts building the CSSOM (CSS Object Model). 
     - **Inline CSS** is applied immediately as it is encountered.
     - **External CSS** is requested and downloaded asynchronously. Once downloaded, it is parsed to build the CSSOM.

3. **JavaScript Execution**:
   - **Inline JavaScript**: Executes immediately as it is encountered during HTML parsing. This blocks further parsing of HTML until the script is executed.
   - **Async JavaScript**:
     - **Download**: The script is downloaded asynchronously, which does not block HTML parsing.
     - **Execution**: Executes as soon as it is downloaded. This can happen at any time during the parsing process, potentially interrupting the HTML parsing and affecting the DOM and CSSOM before they are fully constructed.
   - **Defer JavaScript**:
     - **Download**: The script is downloaded asynchronously, allowing HTML parsing to continue.
     - **Execution**: Executes only after the entire HTML document has been fully parsed and the DOM is complete. Deferred scripts are executed in the order they appear in the document.

4. **Rendering**:
   - **Reflow (Layout)**: Once the DOM and CSSOM are combined into the Render Tree, the browser calculates the layout of elements. This includes determining sizes, positions, and visual properties.
   - **Repaint**: After layout calculations are complete, the browser paints the visual representation of the page, reflecting the final styles and layout.

### DNS explained

IP addresses is like an address but not neccessarily a unique location, it needs it to make request. They are written like hex code, binary like this `192.0.2.172`, hard to remember so people made the Domain Name System, special server called DNS servers are used to map domain to IP. Use this [webapp](https://www.nslookup.io/website-to-ip-lookup/) to find IP for any site.

### Packets explained

When data is sent from server to clients, they are sent in small chunks. So that when a small piece is dropped along the way, it is easier to resend that small chunk. Each chunk takes different path, path are choosen in real time for the most efficient one, allowing fast response time and allow for many people can access the same resource. If it was sent as a whole, 1 big chunk, then only one user can download it one at a time. Which is inconvenient.

## What is a Domain Name?

The reference for this section is [here](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/What_is_a_domain_name#how_does_a_dns_request_work)

You need to learn what URL are first.

### Prerequisite, URL

The reference for this section is [here](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/What_is_a_URL)

Uniform Resource Locator. It is the address of a unique resource, browser use this to request resources, from pages to images and so on. URL points to a unique resource but it can also point to a non existing resource, may have been moved or deleted. URL is defined by the server app.

Here are some examples of URL:

```
https://developer.mozilla.org
https://developer.mozilla.org/en-US/docs/Learn/
https://developer.mozilla.org/en-US/search?q=URL
```

You can use URL in browser's address bar to request the resource.

URL is made of different parts, some are required.

IMG HERE

URL is like postal mail address.

- **Scheme**:
   - Postal service you want to use.
   - IMG HERE
   - This is the request protocol, the rules to adhere. It is usually HTTP or HTTPS for web pages. There are other protocols like mailto and so on.
   - Take note that not all URL are shaped exactly like this, mailto scheme can look like this and works just fine `mailto:foobar`, it has no domain or port after the scheme.

- **Domain name**:
   - City or town.
   - IMG HERE
   - This is after the `://`, the colon marks the end of the scheme while the double forward slashes indicates that the next part is the authority. The domain and port is part of the authority. The port is after this one after `:`. Domain points to a server, you can use IP here too.

- **Port**:
   - Zip code.
   - IMG HERE
   - This is after the `:`, this is the gate to access the resource inside the server, computer has many ports. Usually ommited when using HTTP or HTTPS. Standard ports for HTTP is 80 and HTTPS is 443.

- **Path**:
   - Building where the mail should arrive to.
   - IMG HERE
   - This is the path to the resource. Back then this is the server file path but now it is just a writing convention abstraction, no physical attachment to anything.
 
- **Parameters**:
   - Extra information like the number of the apartment building.
   - IMG HERE
   - There are parameters for the server. Key value pairs that starts with ? and & delimiters. Certain resources are like machines, they may or may not have input settings that affect what they produce. Web developer makes these and should provide a documentation to tell you in detail.

- **Anchor**:
   - The actual person that receives the mail.
   - This is a bookmark inside the resouce, so a browser may scroll down to the bookmark in a page or go to a time in a video.
   - Note that the part after the `#` is never sent to the server with the request, that part is called the **fragment indentifier**

There are extra rules with URL but is not relevant for regular users or Web developers. No need to know those ones to make and use fully functional URLs.

You can make request in browser address bar but you can also make request from inside the html page itself. You can use the tags:

- Anchor: request a page
- Link / Script: request a document with its content resource
- Img / Video / Audio: Display medias
- IFrame : Display another page inside this page

Take note that for the above, use HTTP or HTTPS. There is exception with the data url but it is not convered here.

Everything above is called absolute URL. There is also something called relative URL. These are called absolute or relative URL strings to distinguish them from URL objects, not discussed here.

When you use URL in browser`s address bar, it does not have context so you need to use absolute. You do not need to add the protocol as default is HTTP and port since you only want to add that if the server uses odd port number.

When you use URL in a document / page. When that page is read by browser, that browser should have the page URL right, so inside the page you can use relative and have the browser fill in the gaps. So if the path starts with `/` in page then the browser will fetch that resource from the top root of the server. Example, say you have a page in this URL `https://developer.mozilla.org/en-US/docs/Learn`. That URL is absolute since it points to domain and path and so on. So in that page you can use the following relative URL that the browser will resolve into absolute.

- **Scheme-relative URL: `//developer.mozilla.org/en-US/docs/Learn`**:
   - Browser fills in the missing protocol with the one used to get this page.

- **Domain-relative URL: `/en-US/docs/Learn`**:
   - Browser fills in the missing protocol and domain with the one used to get this page.

- **Sub-resources: `Common_questions/Web_mechanics/What_is_a_URL`**:
   - Same like above but it does not start with `/`. Browser will use the current resource directory as the reference and look into its sub directory.
 So it is the same as `US/docs/Learn/Common_questions/Web_mechanics/What_is_a_URL`

- **Going back in the directory tree: `../CSS/display`**:
   - Same like above, this uses the same UNIX file system convention, so it goes up 1 level. Same as `https://developer.mozilla.org/en-US/docs/Learn/../CSS/display` or `https://developer.mozilla.org/en-US/docs/CSS/display`.

- **Anchor-only: `#semantic_urls`**:
   - Browser will use the current URL and replace or append the anchor to it. Use this to go to a specific part of the current page.

URL is human readable, it is best that you use semantic URL. Meaning you use words with meaning that everyone can understand, why you want to do this:

- It is easier for you to manipulate them. Easy for you to maintain.
- It clarifies things for users in terms of where they are, what they're doing, what they're reading or interacting with on the Web. User friendly context.
- Some search engines can use those semantics to improve the classification of the associated pages. Better SEO.

Okay now we can discuss DNS.

Domain names are addresses to Web servers. Part of Internet infrastructure.

Any machine in the Web network has IP Address, either IPv4 or IPv6. Like `192.0.2.172` and `2001:db8:8b73:0000:0000:8a2e:0370:1337` respectively.

Hard to remember numbers that also may change, so people create human-readable addresses called domain names.

### Deeper dive

#### Structure of domain names

Made of parts with dots as delimiters. There can be more than 3 parts.

IMG HERE

Each part represent information.

##### TLD (Top-Level Domain)

Tell uses domain purpose. `.com`, `.org`, `.net` are most common and does not have a clear purpose, however there are other ones with stricter policies so that it enforces clear purpose.

- Local TLDs like `.us`, `.fr` or `.se` require the service to be in the given language or hosted in that country, to indicate resources language and country.
- `.gov` are for government departments only.
- `.edu` are for educational and academic institutions only.

TLD can have special and latin characters, max is 63 characters, most use 2 to 3 characters.

All TLDs are maintained by [ICANN](https://www.icann.org/resources/pages/tlds-2012-02-25-en).

##### Label / Component

This is what follows the TLD, label.tld. This is case sensitive, 63 characters max. Contain A to Z, 0 to 9 and dash `-`. Dash cannot be the first or last character. Valid examples are `a`, `97`, `hello-strange-person-16-how-are-you`.

The label that is next to the TLD is known as the SLD, Secondary Level Domain.

You can have many lables, you do not always need 3 labels. Like this one is okay `informatics.ed.ac.uk` and for domains that you have you can create subdomains for different contents. So for this domain `mozilla.org`, you can have these subdomains. `developer.mozilla.org`, `support.mozilla.org`, or `bugzilla.mozilla.org`.

#### Buying a domain name

##### Who owns a domain name?

You cannot buy, if you can buy then unused domain will pile up and thus will be locked up from being used by others. So instead unused ones are available again to be used by someone else. Like reuse.

So you pay the right to use a domain name for 1 or more years. You can renew the right and your renewal is taken of higher priority over others who applied for the right. So no one owns the domain, its like renting cars. New cars can be made but no one owns it, we all rent.

Companies called registrars use domain name registries to keep track of technical and administrative information to map individual to their domain name. Registrar is not always the one managing domain names, `.fire` domain name is managed by Amazon.

##### Finding an available domain name

TODO

##### Getting a domain name

TODO

##### DNS refreshing

TODO

#### How does a DNS request work?

TODO

## Additional resources

TODO
