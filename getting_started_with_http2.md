## Getting Started With HTTP2 
March 21st, 2015
<br /><br />
[Akash Mahajan](https://twitter.com/makash)  
<br /><br />
![The App Sec Lab](images/theappseclab-logo-small.png)

#

## Introduction
> Lets see what we need to know to get started with `HTTP2`

<aside class="notes">
Will try to get you upto speed quickly on getting started with HTTP2
</aside>

# 

## Agenda

1. Demo a web server which is running with HTTP2 and a client that supports it
2. Show how to intercept HTTP2 traffic
3. Background of HTTP2
4. Differences between HTTP1.x and HTTP2
5. References and how can you play around with HTTP2

# 

## Demo of HTTP2 
- All the instructions to setup the VM will be posted.

## Demo of Twitter 
- Did you know Twitter already supports and serves HTTP2 if you have a combatible client.

## Demo of HTTP2 no TLS

## Demo of HTTP2 with TLS (Self Signed Certificate)

## Demo of Intercepting HTTP2 Traffic
- Right now you really can't intercept because it is *binary*
- You can see the traffic in Wireshark for now
- No Burp!!

#

## Differences between HTTP1.1 and HTTP2 

## HTTP2 is binary and not textual
- Binary protocols are more efficient to parse and more compact(less error-prone)    

## HTTP2 uses Header Compression
- Every asset that a client needs to load a complete page, has headers

## Allows servers to **push** responses 
- Allows servers to **push** responses proactively into client caches
- Servers need not wait for a slow client to download, parse and realise it needs something else from the server
   
# 

## Background of HTTP2 
From [HTTP2 Explained](http://http2-explained.readthedocs.org/en/latest/src/httptoday.html) by [Daniel Stenberg](https://twitter.com/bagder)

## Main Reasons for HTTP2
- In other words **Pain points of HTTP1.1**

## Limitations of HTTP1.1
 - Even though HTTP1.0 started out to be a small 60 page specification it grew to become 176 pages in 1999 for HTTP1.1 and now a family of RFCs 7230
- Inadequate use of TCP
    
## Expanding on inadequate use of TCP
- Modern sites can load upto 100 objects and 1.5 MB of data for their home page
- On an average 37 TCP connections are required to load the home page completely

## Latency Issues
- Large percentage of users don't use HTTP Pipelining even after it being present in HTTP1.1
- High latency links(think mobile devices), make it hard to get good and fast web experience inspite of high speed connections
- Video and gaming content requires low latency connections to work

## Head of line blocking
> HTTP Pipelining is a way to send another request already while waiting for the response to a previous request

## Head line blocking (Real World)
<ul align="left">
<li class="fragment">Imagine you are getting late for a movie but you want to buy popcorn before you go in</li>
<li class="fragment">There are two lines and you need to pick one</li>
<li class="fragment grow">You just don’t know if the person in front of you is a quick customer or that annoying one that will take forever before he/she is done</li>
</ul>

## Avoiding Head of line blocking
- Picking a line you think will get over quickly
- You might get lucky but once decided you can't easily switch lines!

#

## HTTP2 Origin Story
![](images/an_origin_story_is_coming.jpg)


## IETF and HTTPbis Working Group
- Internet Engineering Task Force is an organisation that develops and promoted internet standards
- Within IETF dedicated "working groups" are formed
- HTTPbis working group was formed during summer of 2007 and was meant to update HTTP1.1
    - bis comes from the Latin adverb for *two*
    - This was meant to be a second take on HTTP1.1
    
## http2 started from SPDY
- SPDY is a protocol developed and spearheaded by Google 
- When HTTPbis group started SPDY was a working concept and well proven in the real world
- So HTTP2 draft-00 was basically SPDY/3 draft! 

# 

## References 
<ul align="left">
<li class="fragment highlight-red">Start with the [Home Page of HTTP2](http://http2.github.io/)</li>
<li class="fragment highlight-red">Focus on the [implementations](https://github.com/http2/http2-spec/wiki/Implementations)</li>
<li class="fragment highlight-red">Nghttp2 an [implementation of HTTP2 in C](https://nghttp2.org/)</li>
<li class="fragment highlight-red">HTTP2 [frequently asked questions](https://http2.github.io/faq/)</li>
<li class="fragment highlight-red">Wireshark [HTTP2 plugin](https://wiki.wireshark.org/HTTP2)</li>
<li class="fragment highlight-red">Stack Overflow on [Curl with HTTP2](http://stackoverflow.com/questions/20116949/using-http2-0-option-with-curl-7-33-0-gives-unsupported-protocol)</li>
<li class="fragment highlight-red">curl page on [http2 explained](http://curl.haxx.se/dev/readme-http2.html)</li>
</ul>


# 

## QnA
- [Akash Mahajan](https://twitter.com/makash)
- [aka@null.co.in](mailto:aka@null.co.in)


