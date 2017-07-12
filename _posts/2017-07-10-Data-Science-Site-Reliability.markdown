---
layout: post
title:  "Data Science for Site Reliability"
date:   2017-07-10 17:00:00
categories: Technology
---

First of all, if your sales and marketing infrastructure is not your very most important business infrastructure, don't read any further ... seriously ... this Salebarn technology blog post is definitely not for people who do not have to worry about the quality of the interaction with their customers.

Second of all, this Salebarn technology blog post is about absolutely RELYING on web, mobile, SMS communication IT in order to effect a MORE DIRECT, MORE PERSONAL, MORE CONTINUOUS, HIGHER QUALITY relationship with your customers ... this second warning is even more seriously than the first ... if you have already permanently decided that you will never be able to trust a technological communication channel, don't read any further ... this Salebarn technology blog post is definitely not for people who do not understand that their customers WANT to be engaged primarily over technological communication channels, so that they don't have to waste time driving around or doing things inefficiently in order to find interesting products, services, people.  

Finally and most seriously, this Salebarn technology blog post is NOT the solution to all of your problems in this topical realm ... if you are looking for either magic bullets or permanent lasting fixes, GO AWAY ... continuously updated, upgraded KNOWLEDGE is the solution to those problems and it will be necessary to continually upgrade and update that knowledge.  

If you find this blog post helpful, GREAT ... no need to thank us; as with ALL bloggers in the history of blogging -- we wrote this posting for ourselves -- it is part of our own training plan ... as all educators knows, it is the attempting to train others that trains us the best, ie no one can possibly learn more in any classroom than the teacher carefully, thoughtfully presenting the material in that classroom.  

This particular blog post is intended to be somewhat evergreen -- but, of course, a technology post obviously CANNOT POSSIBLY BE truly evergreen.  As with ALL podcasts, especially podcasts in the 'technology' category, this podcast will be dated even before it is saved, before it is published.

If you find our approach to problem solving and building knowledge useful and want us to apply our expertise to YOUR particular problem, we are available for hire ... although we are not particularly anxious to find more work, so our one-on-one user-specific consultations and training seminars are not free ... they will be worth several times more than what they cost you, but they not free.

# Site Reliability

This post is about making your most important infrastructure MORE RELIABLE ... it is about OWNING the part of your network that your customers see and depend upon ... even if you own NOTHING beneath the top surface of the skin of what customers see -- THAT is all that matters to the infrastructure of your customer interaction and your network of customers.  It will be absolutely necessary to build that trusted network from underlying components that you cannot depend upon in the future and and should never, ever, ever trust ... trust is like a hotel room -- you do not and cannot EVER own trust, you must RENT it and it is up to YOU to engineer and ensure its reliability.  Reliability is partly about REDUNDANCY, but it is about constant vigilance and SITUATIONAL AWARENESS of where the vulnerabilities and weaknesses are.  A watched pot never boils, but when it does, you immediately make a switch ... before the customer ever experiences a scalding spillover from that boiling pot.  

Increasingly ... sometimes, so much so that it makes me NERVOUS ... I find that I depend more and more upon the adult professionals who run AWS ... that does not exactly mean that there is nothing to learn about site reliability from Microsoft, IBM, Google or other cloud providers or the professionals who work for them, but it does mean that I will START by looking at how AWS and companies that use AWS, eg Netflix, when I want to think about the starting point for a set of best practices in site reliability. This will change -- currently, AWS dominates the world of cloud providers with approximately 1/3 of the market share [and still gaining share at the expense of others] because it is, hands down, the most reliable and dependable option ... but some day, someone else will assemble a team better than the one assembled by Werner Vogels at AWS and develop a more reliable and dependable mousetrap.   

First of all we should think about FUNDAMENTALS ... introductory site reliability concepts and general benefits of cloud computing along with an overview of Amazon Web Services and its overall platform.  For example, you should understand what things like "Zero Trust Networks" are about before dismissing terms like this as mere marketing buzzwords. It is necessary to be paranoid, to ASSUME some MF'er who hates you is going to make a point of taking your infrastructure DOWN ... build ONLY from the synthetic bedrock which you construct -- assume that you can trust nothing.  ## Certification. Never dismiss the importance of reviewing the fundamentals, getting the basics right ... a MASTER always returns to working on the fundamentals ... that is why certifications and bodies-of-knowledge studied to pass certification exams will continue to be important.  Even if you do not take the certification exam, at least learn the jargon, how to SPEAK THE LANGUAGE and USE THE TOOLS before ... LONG BEFORE ... you start down the road of making really, really expensive mistakes.  You WILL make mistakes ... and when you do, it will get really scary and REALLY EXPENSIVE in a hurry if you did not take the time to master the fundamentals.

Next, it is necessary to think about security and access management and how to best achieve it using an AWS core service known as Identity and Access Management (IAM). Conceptually, you really need to START with an understanding of the rationale behind correctly executing the steps required to create and administer AWS users, groups, as well as how to create and assign permissions and policies to them.

LONG after the fundamentals are mastered ... and after security and access management is also mastered ... we can start getting some hands-on knowledge about EC2 instances and images, and how you can create and manage them using both the AWS Management Console as well as the AWS CLI before we get into providing added, more specific security for your applications and instances. This means understanding at an in-depth level things like Simple Storage Service or Amazon's infinitely scalable and durable object storage known as Amazon S3 as well as Amazon's Database-as-a-Service options and EC2 instance storage as well as networking options and what experienced professionals recommend as a starting point for your best practices.  Moving on from this, we can think about building your own private clouds Using Amazon VPC including another in-depth look at various VPC deployment strategies and how people have best leveraged that capability for their own [somewhat] unique environments.

It is impossible to build an impenetrable fortress that is never attacked or never goes down ... even if your little fortress never does anything with anyone or interacts with anyone else and is thus basically unworthy of any attackers time, there is still the question of hardware and software reliability as well as changes in environment that you would not expect to effect your system.  AWS's primary monitoring service, CloudWatch, is important for effectively creating and managing alerts, loggings, and notifications for your EC2 instances, as well as the AWS environment those instances run in. It is also necessary to manage at scale or to manage your applications with auto scaling and elastic load balancing and to utilize AWS services and EXTENDED AWS services [from AWS as well as independent software vendors] which allow you to leverage to create a dynamically scalable and highly available web application. Understand the BASICS, but before you complain about the limits in those basic services or hack your own infrastructure-as-code to improve on them, take a brief look at the add-on AWS services that you can leverage for enhancing your applications' performance and availability, ie the real value of going with the dominant provider is that ecosystem is large enough that someone else has probably already solved that problem.


## Data Science For Security Professionals
*TBD*

*TBD TBD TBD TBD TBD  and much more TBD ... the following ruminations, currently in-process will be from what I gain preparing to take part in a class that I am excited about ... maybe you want to sign up for that class [Data Science for Security Professionals](https://www.safaribooksonline.com/live-training/courses/data-science-for-security-professionals/0636920095781/)

Introduction: Data Preparation with Pandas (15 Min)
What is Pandas and why use it?
The Series, DataFrame, and Panel objects
The Pandas ecosystem: Scikit-learn, Seaborn, Bokeh
Vectorized Computing in One Dimension: The Series Object (90 Min)
Creating a series
Describing data
Filtering data
Other operations on data
Activity: Worksheet
Vectorized Computing in Two Dimensions: The DataFrame (90 min)
Creating a DataFrame
Reading logfiles, APIs and other sources
Manipulating data in data frames
Applying functions to data frames
Aggregating data in data frames
Activity: DataFrame Worksheet
Homework: You’ll receive a series of data sources to prepare for analysis
DAY 2—EXPLORE YOUR DATA

On day two, you’ll learn the concepts and techniques behind exploratory data analysis as well as practical data visualization techniques.
Statistical Summaries (90 Min)
5-Number summaries
Normalizing data
Understanding Distributions
Correlations
Confidence Intervals and P-Values
Exercise: Complete EDA Worksheet
Concepts of Data Visualization (30 Min)
Creating effective visualizations
Choosing the correct visualization
Using visualization to explore data
Practical Data Visualization (90 Min)
Using Matplotlib to create basic charts
Overview of advanced charts with Seaborn
Creating dashboards with Superset
Homework: Complete visualization worksheet
DAY 3—LEARN FROM IT

Day three will introduce the machine learning process. We will cover model selection, feature engineering, and model evaluation.
Machine Learning Concepts (60 Min)
Machine learning process
Machine learning problem types
Supervised vs Unsupervised machine learning
Unsupervised Machine Learning in Practice (60 Min)
Distance measures
Nearest Neighbors
K-Means
Exercise: K-Means Worksheet
Supervised Machine Learning: Classification (60 Min)
Feature engineering
Modeling with Decision Trees and Support Vector Machines
Model evaluation
Case Study: Classifier to identify SQL Injection
Final Project: DGA Classifier
