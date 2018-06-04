---
layout: post
title:  "IETF and The Internet Protocol Suite"
date:   2018-06-04 4:39:00
categories: Technology
---

Salebarn.com will primarily be an open source technology project ... and it is an EXTREMELY low-level, fundamental technology project ... that means working with the internet protocol suite.  When writing programs that communicate across any physical layer that resembles a computer network, one must first invent a protocol, an agreement on how those programs will communicate. Any client application or any server application may be thought of as communicating via a network protocol, but actually, multiple layers of network protocols are typically involved ... ALL of those layers can introduce errors; a mistake that most people make is to assume ideal behavior. In the real world, we MUST NEVER EVER EVER assume ideal behavior ... especially, if we are operating with things that typically, even predominantly error free.

In any real-world program, it is essential to check EVERY single last function call for an error return. Since terminating on an error is the common case, we can shorten our programs by defining a wrapper function that performs the actual function call, tests the return value, and terminates on an error. Termination is a GOOD thing; we can rapidly [within nanoseconds] can start over if there is a termination error and the rapid restart will give the appearance to even the most critical human that there was no disruption, no loss of latency. 
