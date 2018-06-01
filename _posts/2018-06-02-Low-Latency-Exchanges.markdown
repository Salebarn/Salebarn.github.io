---
layout: post
title:  "The Low Latency Exchange Infrastructure of Salebarn.com"
date:   2018-06-02 4:39:00
categories: Technology
---

Salebarn.com will primarily be an open source technology project ... we'll see if the technology of the project can  develop into a business ... first, before we can even really contemplate that, we have to see if we can develop the technology into a working prototype of what the business might look like or do for people.

At this early point, any discussion of the NEED for Salebarn or ruminations on a business plan are only for the purposes of describing the target use case for the open source technology project.  The PRIMARY or core technology of Salebarn is DISRUPTION and its disruptive engine AI deep learning tool which will utilize data obtained from the Salebarn messaging infrastructure.  The Salebarn messaging infrastructure will be an adaptation of ZeroMQ or Nanomsg or NNG.

# How the world arrived at NNG

There's a lot to learn from the ZeroMQ archives ... not just Pieter Hintgens discussions and interviews, but those TOO.  In particular, we need to remember the initial impetus of ZeroMQ ... [metaphorically] it's all about getting down to sub-atomic level and understanding the physics of people and how/why people interact with one another. This is sorta important for trivial bs like Facebook or Reddit or messaging channels ... but it is DREADFULLY important when it's about REAL stuff and when people have legit skin in the game on making a purchase or investment because people will literally and figuratively EAT those products and FEED those products to their families for their loved ones to EAT. So we have to think about the physics of people ... not just yakking about things ... but about assuring the quality of FOOD that they EAT ... Salebarn messaging is about the biophysics of people ... because ultimately it's about people ingesting things that can KILL them. Salebarn.com is not like a throwaway app like Facebook ... Salebarn.com is about SAFETY-critical exchanges of information.

Why did Martin Suskirk rewrite ZeroMQ as Nanomsg?  Why did Garrett D'Amore morph Nanomsg into NNG?  The history of NNG is not trivial and is worth exploring.

# How Salebarn will use NNG

The main technology of Salebarn.com is disruption ... ultimately that DEMANDS low-latency communication for product exchanges and the marketing negotiations that drive the Salebarn.com business.       
